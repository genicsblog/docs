---
layout: default
title: Local setup
parent: Theme docs
grand_parent: Developer Docs
nav_order: 1
description: "Guide to setting up the development environment to build genic's theme for local previews."
permalink: /developer/theme/setup-env
---

# Local setup instructions

This document will guide you through setting up the local development environment for the [`theme-files`](http://github.com/genicsblog/theme-files){:target="_blank"} repo.

## Pre-requisites

Please install [Ruby](https://www.ruby-lang.org/en/downloads/){:target="_blank"} (preferrably 3.x) and [Node.js](https://nodejs.org/en/download/){:target="_blank"} (preferrably 16.x) before you proceed.

## Background

There is an abstraction of theme files from the content files. This means that theme's code is stored in a different repository than the content's repository. This is done so as to avoid authors having to deal with messy theme code and developers having to deal with content.

A quick thought would lead to a solution using [git submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules){:target="_blank"}. But since jekyll requires all the relevant paths both for theme and content to be in the root folder, we can't use git submodules [even if the content is symlinked](https://github.com/jekyll/jekyll/issues/233#issuecomment-560871){:target="_blank"}.

## Using the `dev` script

To tackle this issue in the easiest way possible, we created a [`dev.sh`](https://github.com/genicsblog/theme-files/blob/a71d34c06797b3b0dec71dcd336cbffbe89b6353/dev.sh){:target="_blank"} script that can handle merging the content of the main repository with that of theme files repository behind the scenes, inside a hidden folder.

To build and run the theme code locally, execute the `dev.sh` script in your terminal:

```shell
./dev.sh
```

The first build would take a few minutes. Once done, you can preview the site at [localhost:4000](http://localhost:4000){:target="_blank"}. Subsequent builds should be faster.

If any problem persists, try providing the correct permissions to the bash script by running:

```shell
chmod +x dev.sh
```

Now you should be able to run the `./dev.sh` command.

## Explanation

As of now, the content of the `dev.sh` script is as follows:

```bash
#!/bin/sh

# move out of the .content folder once script is closed
function cleanup() {
  cd ..
}

trap "cleanup" 2

if [ ! -d ".content" ]
then
  echo "No cached '.content' directory found. Fetching the latest data..."
  git clone https://github.com/genicsblog/genicsblog.com .content -q
fi

rsync -r --exclude '.content' . .content/
cd .content

if [ ! -d "node_modules" ]
then
  echo "Installing node dependencies..."
  npm i --silent
fi

if [ ! -d "vendor" ]
then
  echo "Installing gem dependencies..."
  bundle config set --local path 'vendor'
  bundle install --quiet
fi

bundle exec jekyll serve
```

The script works by:

- Creating a `.content` hidden folder and cloning the main repository inside it, if it doesn't already exist.
- Moving the content of the theme from the current folder inside the `.content` folder to move the local changes to the hidden folder.
- Move inside the `.content` folder and install dependencies if local cache (inside `vender/` and `node_modules/`) doesn't exist.
- Finally serve the static site by running `bundler exec jekyll serve`.
- The `cleanup()` function is responsible for moving out of the `.content` folder once the script is closed, as there is a `cd .content` step in the script which needs to be undone.

## [Deprecated] Using Dockerfile

This is the old method that was used to run local env for the theme code.

Although it doesn't require you to install Ruby and Node.js as a pre-requisite, it is no longer recommended because of high resource usage for relatively simple task.

If you are still willing to understand the build process, [here's the old `Dockerfile`](https://github.com/genicsblog/theme-files/blob/f775397895b568eeb40019d503c0c1f382cbfd7a/Dockerfile){:target="_blank"} used to run the containers.

You may paste the file at the root of the folder and use these commands to run the container:

```bash
docker build -t genics-theme .
docker run -p 4000:4000 genics-theme
```

The container bsically installs required software, clones and merges the main repository with the content from the local theme code and executes the `bundle exec jekyll serve` command while exposing the port `4000`.

You will still be able to access the built site from [localhost:4000](http://localhost:4000){:target="_blank"}.
