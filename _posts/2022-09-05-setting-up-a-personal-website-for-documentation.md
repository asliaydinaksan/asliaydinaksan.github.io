---
layout: post
title: Setting Up a Personal Website for Documentation
date: 2022-09-05
description:
tags: [github, jekyll, howto]
---
Following is a step-by-step explanation of how I set up this website. This is a static website which runs on **GitHub** and **Jekyll**.

## GitHub

Your GitHub account keeps the files/folders necessary to run your website.

Open a [GitHub](https://github.com/) account.

Create a repository for your site on GitHub. [Here](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll) is a useful explanation on how to do it for a website.

Download [GitBash](https://gitforwindows.org/). GitBash is provides a local emulation for your website. You can see changes you make on your website locally, before pushing it on GitHub.

Download [GitHub Desktop](https://desktop.github.com/). GitHub Desktop is an app which communicates between local and remote GitHub repositories.
- Link your local repository to your remote repository.

## Jekyll

Jekyll is a static site generator. It takes text written in your favorite markup language and uses layouts to create a static website.

Follow the step on this [website](https://jekyllrb.com/docs/) to run Jekyll on your computer.
- Open Terminal and install the jekyll and bundler gems: <code>gem install jekyll bundler</code>

## Visual Studio Code

Visual Studio Code is a source-code editor where you will write/modify your website on your computer.

Download [Visual Studio Code](https://code.visualstudio.com/)

Open your GitHub repository in Visual Studio Code (you can do this via GitHub Desktop).

---
Find a theme you would like to use as a starting template for your website. You can browse for themes on [Jekyl's website](https://jekyllrb.com/resources/).
You can fork or clone the GitHub repository of the chosen template to your repository.

If you would like to preview the website locally, on GitBash:
- <code>cd</code> into the local repository's directory
- Add webrick to your dependencies (if you are using Ruby version 3.0.0 or higher): <code>bundle add webrick</code>
- Run <code>script/bootstrap</code> to install the necessary dependencies (not necessary depending on the theme)
- Run <code>bundle exec jekyll serve</code> to start the preview server
- Visit [localhost:4000](localhost:4000) in your browser to preview the theme