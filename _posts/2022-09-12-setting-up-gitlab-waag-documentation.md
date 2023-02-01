---
layout: post
title: Setting up Gitlab Waag Documentation
date: 2022-09-12
description:
tags: [gitlab, mkdocs, howto]
---
Following is a step-by-step explanation of how I set up **Gitlab** with **MkDocs** to work on Waag documentation.

## Gitlab

The Waag Gitlab account keeps the files/folders necessary to run the website.

Open [Waag Gitlab](https://gitlab.waag.org/)

Go to the repository you would like to work on/you have been granted access to.

Hit **Clone** and copy the HTPPS address.

Open **GitHub Desktop** (see more about GitHub Desktop [here](/setting-up-a-personal-website-for-documentation/))

Hit the **down arrow** next to Current Repository. Click **add** and paste the HTPPS link copied from Gitlab. You will be directed to enter your Gitlab username and password, do so and clone remote repository to a local folder.

## MkDocs

MkDocs is an SSG (static site generator). For Waag Documentation, we use MkDocs.

Download MkDocs following the steps on their [website](https://www.mkdocs.org/user-guide/installation/) (notice, you need Python to run MkDocs. So if you do not have Python, download it too.)

You need to download MkDocs Material with a version older than 5. So I downloaded version 4 following the steps [here](https://squidfunk.github.io/mkdocs-material/getting-started/). I typed command:

<code>pip install mkdocs-material=="4.*" </code>

---

Start running your repository locally:

<code>cd "path to your repository" <code>

<code>mkdocs build<code>

<code>mkdocs serve<code>

On your browser go to [http://localhost:4000/](http://localhost:4000/)