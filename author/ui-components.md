---
layout: default
title: UI Components
parent: Author Docs
nav_order: 3
description: "Documentation on how to add various UI elements such as images, links buttons and more to your blog posts at Genics Blog."
permalink: /author/ui-components
---

# UI Elements Guide

This guide explains how to add various UI elements such as images, links, code blocks and more to your blog posts.

**NOTE**: If you are stuck at any step, create an issue on github and we'll help you out, or [join our discord server](https://discord.gg/qQEsNkF7F6){:target="_blank"} to get help faster.

---

## Italics

To italicize text, wrap it inside single asterisks: `*like this*` or inside single underscore `_like this_`. Which will render to: *like this* and _like this_ (both produce same result).

## Bold Text

To make some text bold, wrap it inside double asterisks: `**like this**`. Which will render to: **like this**.

## Bold and Italics together

Doing something `***like this***` or `_**like this**_` or `**_like this_**` will render ***like this***, _**like this**_ and **_like this_** in similar way.

You can mix the syntax too: `*This **should** work too*` produces *This **should** work too*.

## Strikethrough

Strikes to text can be added: `~~like this~~`(produces: ~~like this~~). This can be mixed with other formattings too: `**_~~like this~~_**`(renders: **_~~like this~~_**).

## Headings

Genics Blog supports 6 levels of headings. They can be added using the following syntax:

```
# Heading Level 1
## Heading Level 2
### Heading Level 3
#### Heading Level 4
##### Heading Level 5
###### Heading Level 6
```

## Hyperlinks

Hyperlinks are used to link to other pages on/outside the website. To add a link to some text in the article use this syntax:

```
[link text](link url)
```

For example, writing this:

```
[Genics Blog](https://genicsblog.com)
```

will render: [Genics Blog](https://genicsblog.com)

## Media content

Images and GIFs work similar to hyperlink syntax. Add them using this:

```
![alt text for the media](image/gif url)
```

For example:

```
![Genics Blog Logo](https://genicsblog.com/assets/images/genicsblog.png)
```

Produces:

![Genics Blog Logo](https://genicsblog.com/assets/images/genicsblog.png)

You can control the height and width of the image using this syntax (replace 100px with the size you wish):

```
![Genics Blog Logo](https://genicsblog.com/assets/images/genicsblog.png){:width="100px" height="100px"}
```

Example:

![Genics Blog Logo](https://genicsblog.com/assets/images/genicsblog.png){:width="100px" height="100px"}

GIF:

![cringe gif lmao](https://i.ibb.co/qD9xK8W/gif.gif)

**Media content like Images and GIFs are automatically centered to the screen in the actual post.**

## Inline Code

Inline code can be added by wrapping it inside single backtick `` `This is inline code` `` renders to `This is inline code`. If you need to escape backtick, use double backtick ``` `` Double backticks (`) `` ``` renders to `` Double backticks (`) ``. Similarly, to escape double backticks wrap them inside tripple backticks.

## Code Blocks
