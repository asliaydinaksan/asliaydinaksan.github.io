---
layout: post
title: Working with Jekyll and MkDocs
date: 2022-09-12
description:
tags: [mkdocs, jekyll, howto]
---
After installing both Jekyll and MkDocs, I realized that MkDocs server does not stop working. So I had to figure out a workaround to make my local server listen to Jekyll for my personal webpage. I found out that you can specify the port of the server. To do that, simply start your jekyll server with the command:

<code>bundle exec jekyll serve --port 4001<code>

Now, you can see your webpage on

[http://localhost:4001/](http://localhost:4001/)