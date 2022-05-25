---
layout: default
title: Configure your profile
parent: Author Docs
nav_order: 1
description: "The procedure to make an author profile at Genics Blog."
permalink: /author/configure-your-profile
---

# Configure your profile

The very first step to get started at Genics Blog would be to get yourself an author profile. The profile page would contain with your bio, social media links and all the articles written by you.

---

Creating a profile is really simple:

- Open the [`authors.yml`](https://github.com/genicsblog/genicsblog.com/blob/main/_data/authors.yml){:target="_blank"} file and press the edit button on the top right.
    ![image](https://user-images.githubusercontent.com/46792249/147688574-f3e743a8-a406-42f5-8503-b666ca9b7601.png){:height="300"}{:width="400"}

- Copy this piece of text to the end of the existing content:
```yml
gouravkhunger: # replace gouravkhunger with the username you want
    name: "Gourav Khunger" # the display name you want
    role: "Founder @ Genics Blog" # anything you want to be known for, ex: Full stack dev, Intern @ Company, etc.
    avatar: "https://avatars.githubusercontent.com/u/46792249"
    bio: "16 year old passionate App developer. I have interests in web development too." # your about me, max 200 chars
    links: # links to your social media
        github: "gouravkhunger" # (GITHUB PROFILE IS REQUIRED) Format: just the username
        stackoverflow: "9819031" # Format: just the user id
        linkedin: "in/gourav-khunger-584351216/" # Format: <locale>/<user-id>
        twitter: "gourav_khunger" # Format: just the username
        instagram: "_gourav.khunger_"  # Format: just the username
        youtube: "channel/UCkv-J_D8jK2N02nBcyM92mQ"  # Format: <channel or c>/<channel-id> Depends on if your channel is verified or not
```

    It is recommended to take a look at other's profile declarations to get a gist of how this process works. Please keep these points in mind:

    - Replace `gouravkhunger` with your desired username (no special characters please) and fill in the other information.
    
    - You can use a link to the image file for any avatar hosted online, until it is copyright free.

    - Include only those social media links which you want to include in your profile.

    - Ensure that no whitespace is present to the left of your user name, and all the text under it is whitespaced with tabs. If you need help with yaml syntax, [check out this document](https://docs.ansible.com/ansible/latest/reference_appendices/YAMLSyntax.html){:target="_blank"}.

- After your are done, **Remove all the comments** (the `#`s and the text after them)

- Commit the changes and make a pull request. 

We'll merge your PR as soon as possible and your profile would be visible after about 10 minutes past the merge time, at `https://genicsblog.com/author/<your-username>/`: [example](https://genicsblog.com/author/gouravkhunger/){:target="_blank"}.