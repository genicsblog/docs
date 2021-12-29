---
layout: default
title: Getting Started
parent: Author Docs
nav_order: 1
description: "Getting started as an Author at the Genics Blog."
permalink: /docs/author/getting-started
---

# Getting started

## Make a contributor profile

The very first step to get started at Genics Blog would be to get yourself a contributor profile. The contributor profile page would contain with your bio, social media links and all the articles written by you.

Creating a profile is really simple:

- Open the [`contributors.yml`](https://github.com/genicsblog/genicsblog.github.io/blob/main/_data/contributors.yml) file and press the edit button on the top right.
    ![image](https://user-images.githubusercontent.com/46792249/147688574-f3e743a8-a406-42f5-8503-b666ca9b7601.png)

- Copy this piece of text to the end of the existing content:
    ```yml
    gouravkhunger:
        name: "Gourav Khunger"
        role: "Founder @ Genics Blog"
        avatar: "https://avatars.githubusercontent.com/u/46792249"
        bio: "16 year old passionate App developer. I have interests in web development too."
        links:
            stackoverflow: "9819031" # just the user id
            github: "gouravkhunger" # just the user id
            linkedin: "in/gourav-khunger-584351216/" # <locale>/<user-id>
            twitter: "gourav_khunger" # just the user id
            instagram: "_gourav.khunger_"  # just the user id
            youtube: "channel/UCkv-J_D8jK2N02nBcyM92mQ"  # <channel or c>/<channel-id>
    ```

    Here, replace `gouravkhunger` with your desired username(no special characters please) and other information. You can use any avatar hosted anywhere online, until it is copyright free.

    Ensure that no whitespace is before your user name, and all the text under it is whitespaced with tabs.

- Commit your changes and make a pull request. 

We'll merge your PR as soon as possible and your profile would be visible after about 10 minutes past the merge time.