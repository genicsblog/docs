---
layout: default
title: Project structure
parent: Theme docs
grand_parent: Developer Docs
nav_order: 2
description: "Understanding the project structure of the theme-files repository at Genics Blog"
permalink: /developer/theme/project-structure
---

# Project structure

Understanding the project structure of the theme-files repository.

---

These are the files and folders relevant to the theme/code aspect of the site:

- [`_includes`](https://github.com/genicsblog/theme-files/tree/main/_includes){:target="_blank"}: This folder holds small code files whose content can be retreived and placed inside another file during the build step. Read more about [Jekyll includes](https://jekyllrb.com/docs/includes/){:target="_blank"}.

- [`_layouts`](https://github.com/genicsblog/theme-files/tree/main/_layouts){:target="_blank"}: This is the folder that contains template files for different types of pages. Read more about [Jekyll layouts](https://jekyllrb.com/docs/step-by-step/04-layouts/).

  - [`default.html`](https://github.com/genicsblog/theme-files/blob/main/_layouts/default.html){:target="_blank"}: The base layout that each other template inherits. This provides the flexibility to create a base layout for other layout types.

  - [`archive.html`](https://github.com/genicsblog/theme-files/blob/main/_layouts/archive.html){:target="_blank"}: The template for category and tag pages. For example: [category #web](https://genicsblog.com/category/web){:target="_blank"}.

  - [`page.html`](https://github.com/genicsblog/theme-files/blob/main/_layouts/page.html){:target="_blank"}: The template for generic pages. For example: [About page](https://genicsblog.com/about){:target="_blank"}.

  - [`post.html`](https://github.com/genicsblog/theme-files/blob/main/_layouts/post.html){:target="_blank"}: The template used by article pages.

  - [`series.html`](https://github.com/genicsblog/theme-files/blob/main/_layouts/series.html){:target="_blank"}: The template used by series pages. For example: The [Android development series](https://genicsblog.com/series/android-development){:target="_blank"}.

  - [`tool.html`](https://github.com/genicsblog/theme-files/blob/main/_layouts/tool.html){:target="_blank"}: The template used by tools pages. For example, [frontmatter generator](https://genicsblog.com/tool/frontmatter-generator){:target="_blank"} tool.

- [`plugins`](https://github.com/genicsblog/theme-files/tree/main/_plugins){:target="_blank"}: Contains custom ruby plugins that extends the jekyll build process to achieve required behavior. Read more about [Jekyll plugins](https://jekyllrb.com/docs/plugins/){:target="_blank"}.

- [`_scripts`](https://github.com/genicsblog/theme-files/tree/main/_scripts){:target="_blank"}: This folder contains external python scripts that are mostly used in GitHub Actions to validate certain things.

- [`_tools`](https://github.com/genicsblog/theme-files/tree/main/_tools){:target="_blank"}: This folder contains code for the various tools that are helpful to authors while writing articles.

- [`assets`](https://github.com/genicsblog/theme-files/tree/main/assets){:target="_blank"}: Contains static assets like stylesheets, images and javascript code for the site.

- Other important files:

  - [`_config.yml`](https://github.com/genicsblog/theme-files/blob/main/_config.yml){:target="_blank"}: Jekyll configuration file. Read more about [Jekyll configuration](https://jekyllrb.com/docs/configuration/){:target="_blank"}.

  - [`manifest.json`](https://github.com/genicsblog/theme-files/blob/main/manifest.json){:target="_blank"}: Manifest data needed for PWA support.

  - [`search.json`](https://github.com/genicsblog/theme-files/blob/main/search.json){:target="_blank"} & [`sitemap.xml`](https://github.com/genicsblog/theme-files/blob/main/sitemap.xml){:target="_blank"}: Data for search across the site functionality & xml sitemap file respectively.

  - [`postcss.config.js`](https://github.com/genicsblog/theme-files/blob/main/postcss.config.js){:target="_blank"} & [`tailwind.config.js`](https://github.com/genicsblog/theme-files/blob/main/tailwind.config.js){:target="_blank"}: TailwindCSS configuration files.

  - [`Gemfile`](https://github.com/genicsblog/theme-files/blob/main/Gemfile){:target="_blank"} & [`package.json`](https://github.com/genicsblog/theme-files/blob/main/package.json){:target="_blank"}: Declarations for Ruby and Node dependencies required by the theme.
