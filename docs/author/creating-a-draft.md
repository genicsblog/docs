---
layout: default
title: Creating a Draft
parent: Author Docs
nav_order: 3
description: "The procedure to create a draft post at the Genics Blog."
permalink: /author/writing-the-article
---

# Creating a Draft post

Every post at Genics Blog starts as a draft. In this section you'll learn how to create a draft post.

Prerequisites:
- [Get a contributor profile](/author/getting-started#make-a-contributor-profile).
- Fork the blog repository to your github profile.
- Get a gist of [how to add ui elements](/ui-components) to your post.

---

The content at genicsblog.com is written in [Markdown](https://en.wikipedia.org/wiki/Markdown). This means that you can write your content in plain text and it will be rendered HTML automatically. Let's create a draft post in markdown!

## Create a new file in `_drafts` folder

Once you fork the repository, you can start writing your post. For drafts, even editing on the GitHub interface works fine.

Open the `_drafts` folder in the editor of your choice. To create a new draft, press the **Create a new file** button on the right hand side.

![Create a new file from GitHub GUI](https://user-images.githubusercontent.com/46792249/147846679-b9c5b35b-f9e5-4cfc-9d20-e2a028df750f.png){:width="400"}

## Define a name for the draft file

In the editor, give your file a name. Let's say you want to create a draft titled **How to write a draft**, the file name for this post would become: `how-to-write-a-draft.md`.

![Defining a file name for the new file on GitHub GUI](https://user-images.githubusercontent.com/46792249/147846741-19007d50-9fb3-47f0-b52b-e8997da109e7.png)

**Important**:
- All the alphabets in the file name must be lowercase.
- All the blank spaces and special characters should be avoided, replace with `-` to seperate words.
- File must end in extension `.md` to specifiy a markdown file.

## Add the frontmatter

Genics Blog requires each post/draft to have a frontmatter that defines the title, description, and other metadata. This is declared at the very top of the file within `---` quotations.

Here's an example of a minimal valid frontmatter that Genics Blog understands:

```yml
---
layout: post
title:  "How to write a draft"
excerpt: "The complete guide you'll need to refer to create mind blowing drafts."
image: "https://cdn.hashnode.com/res/hashnode/image/upload/v1631596605889/xCcnwfFVk.png"
category: content-writing
tags: ["writing-skills", "tips"]
author: gouravkhunger
---
```

- The `layout` defines what kind of page it will be (here, a `post`).

- The `title` is the title of the post that will be shown in bold at the blog.

- The `excerpt` is a short sentence - a summary of the artilce.

- The `image` is the image url where the thumbnail of this post is hosted. We do not host images, so you need to drag and drop your preferred thumbnail to the GitHub editor and it will automatically generate a URL for the hosted image.

- The `category` defines what topic the post is about. Please use only one category per post.

- The `tag` defines what smaller topics the post is about. Please use a maximmum of 3 tags per post. Exceptions can be made, [contact us](https://genicsblog.com/contact) in that case.

- The `author` is the username of the author of the post. It was defined when you made a [contributor profile](/author/getting-started#make-a-contributor-profile).
