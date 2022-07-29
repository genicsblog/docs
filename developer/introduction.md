---
layout: default
title: Introduction
parent: Developer Docs
nav_order: 1
description: "Introduction to the infrastructure related details at the Genics Blog"
permalink: /developer/introduction
---

# Introduction

A quick insight into the codebase at genics.

## Exploring repositories

These are the major repositories that form the entire base of [genicsblog.com](https://genicsblog.com){:target="_blank"}

- [`genicsblog.com`](https://github.com/genicsblog/genicsblog.com){:target="_blank"}: Referred to as the "main" repository most of the time. This holds the actual articles, posts, site pages, author data: basically everything "content" related.

- [`theme-files`](https://github.com/genicsblog/theme-files){:target="_blank"}: Abstraction of theme related code from the main repository. Considering that the main repository became hard to navigate for authors who didn't have anything to do with the code, we created a separate infrastructure for maintaining the theme code.

- [`comments`](https://github.com/genicsblog/comments){:target="_blank"}: The repository that hosts comments and discussions from the readers.

- [`genics-bot`](https://github.com/genicsblog/genics-bot){:target="_blank"}: A discord bot that does quite a few things to help run our [discord server](https://discord.genicsblog.com){:target="_blank"}.

- [`docs`](https://github.com/genicsblog/docs){:target="_blank"}: Hosts this documentation website.

---

**Note**: This developer docs will focus mainly on the [`theme-files`](https://github.com/genicsblog/theme-files){:target="_blank"} repo and explain the infrastructure related details.

---

## Technical details

- [`genicsblog.com`](https://genicsblog.com){:target="_blank"} is a static site built with [Jekyll](https://jekyllrb.com){:target="_blank"}.
- The production website is hosted on [GitHub Pages](https://pages.github.com){:target="_blank"} and the [staging](https://staging.genicsblog.com){:target="_blank"} environment (to preview changes before they go live) is hosted on [Vercel](https://vercel.com){:target="_blank"}.
- The tech stack for the website includes `HTML` template files, `TailwindCSS` and `JavaScript` for styling and functionality, and `Ruby` for custom plugins to alter the Jekyll build process according to needs.
- Other languages/tools used are `Python` and `Bash` scripts for custom workflows and dev environments, `YAML` and `Markdown` for data files and posts.
