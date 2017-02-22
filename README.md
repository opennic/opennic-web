# opennic.org

My take on a new homepage for [OpenNIC](https://github.com/OpenNIC).

## Building the site

This outlines how to build the site manually on your webserver, not necessary with GitHub pages.

Requirements:

 - [Jekyll installed](https://jekyllrb.com/docs/installation/) on the webserver.

Run `jekyll build` in the working directory. This will build the site into `/_site` which can be served by any webserver.

## Creating Pages

Simply create a markdown (`.md`) file in the root directory with the following information at the beginning:

```
---
layout: page
title: Page Title
permalink: /link/to/page/
---
```

The rest can be written in GitHub Flavored Markdown and will be automatically converted upon building the website. [Example](/irc.md).

## Writing Posts

Create a markdown file in `/_posts` named similarly to `YYYY-MM-DD-Title-of-Post.md` (ex. [`2015-09-29-Recent-T2-Updates.md`](/_posts/2015-09-29-Recent-T2-Updates.md)) with the following information at the beginning:

```
---
layout: post
title: "Title of Post"
date: YYYY-MM-DD
category: News
author: FirstName
---
```

Like pages, the rest of the post is written in GitHub Flavored Markdown.

## This site

...was built by [Jonah Aragon](https://github.com/JonahAragon) for [OpenNIC](https://www.opennicproject.org). The theme is loosely based on [this theme](https://github.com/ModernTLD/site-theme) by ModernTLD.
