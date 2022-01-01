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
- [Get a contributor profile](/getting-started#make-a-contributor-profile).
- Fork the blog repository to your github profile.
- Get a gist of how to add [UI elements](/ui-components) to your post.

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
languages: ["kotlin", "xml"]
category: content-writing
tags: ["writing-skills", "tips"]
author: gouravkhunger
---
```

**Omit any of the variables if you don't want to use them!**

- `layout` defines what kind of page it will be (here, a `post`).

- `title` is the title of the post that will be shown in bold at the blog.

- `excerpt` is a short sentence - a summary of the artilce.

- `image` is the image url where the thumbnail of this post is hosted. We do not host images, so you need to drag and drop your preferred thumbnail to the GitHub editor and it will automatically generate a URL for the hosted image.

- `languages` is a list of programming languages that this post contains snippets of. If your post doens't require snippets, simply remove this variable. Only add the **lowerrcase names** of the programming language to this array.

- `category` defines what topic the post is about. Please use only one category per post.

- `tag` defines what smaller topics the post is about. Please use a maximmum of 3 tags per post. Exceptions can be made, [contact us](https://genicsblog.com/contact) in that case.

- `author` is the username of the author of the post. It was defined when you made a [contributor profile](/author/getting-started#make-a-contributor-profile).

### Optional Values

Here are some optional values you can define for your post:

```yml
---
# Other variables here
original: "https://docs.genicsblog.com/author/writing-the-article"
notice: "**Markdown** is supported in this _one_ so you could do [such things](https://genicsblog.com)!"
---
```

- `original` is used to define the original URL of the post(only applicable if you are cross-posting.)

- `notice` is a notice that will be shown at the top of the post. You could add some note about the prerequisites for a tutorial, or any other info you want to show.

## Write the content

After you are done with the frontmatter, you can start writing the content of your post. You can take a look at [other drafts](https://github.com/genicsblog/genicsblog.github.io/tree/main/_drafts) or [published posts](https://github.com/genicsblog/genicsblog.github.io/tree/main/_posts) to take a look at how the content is written.

## ALERT!

Please **DO NOT** edit any file outside the drafts folder while you are writing your draft, and **DO NOT** change with other author's drafts. This will cause the Pull request checks to fail and your draft won't be automatically published.

Repeated attempts to bypass/hack the check system will result in a permanent ban from the site, the discord community and will result in deletion of your profile.

## Previewing the draft

At this point, you'll want to preview how the draft would look like on the site. To do so, commit your finalised changes and make a Pull Request to immediately publish the draft article to the blog. The draft will be published to a private page that is not indexed by search engines.

**A draft is accessible only if someone has its link**. This feature is for the authors to preview their posts before they are published and to share with only those whom they want to.

Once your PR is successfully merged, the draft will appear to a link similar too this:

```
https://genicsblog.com/draft/how-to-write-a-draft
```

The slug is defined by the file name you made. You can preview your changes here, and if needed create new pull requests to publish your changes.

## Next Steps

Read [this guide](/author/publishing-the-post) to get your draft published as a public post!
