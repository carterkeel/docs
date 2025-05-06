---
title: Adding New Post To Blog
date: 2025-05-06
author: Carter Keel
description:
isStarred: false
---

# Adding a New Post

Follow these steps to add a new post to the documentation website.

## 1. Pull the Repository

Clone or pull the latest version of the documentation repository from GitHub:

`git pull origin main`

## 2. Add a Markdown File

Create a new Markdown (`.md`) file in the following directory:

`content/posts/`

This file will contain the content of the new post. Use standard Markdown formatting. Include front matter at the top of the file, for example:

`--- title: "My New Post" date: 2025-05-01 draft: false ---`

## 3. Add Images (Optional)

If the post includes images, place the image files in the `static` directory. For example:

`static/images/my-image.png`

Then, reference the image in the Markdown post using a relative path:

`![Alt text](/images/my-image.png)`

## 4. Commit and Push Changes

After adding the post and any images, commit the changes and push them to GitHub:

`git add . git commit -m "Add new post" git push origin main`