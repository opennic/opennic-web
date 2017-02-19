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

## My message to the Mailing List

```
Hi!

I've been working on a new design and system for the homepage, and I wanted to gather some opinions on what works, what doesn't, and what you think about replacing our current WordPress site (at https://www.opennicproject.org/). You can check out my design at https://jonaharagon.github.io/opennic.org/.

Some background:

The WordPress site currently host a simple homepage, a basic membership system (essentially providing a profile frontend for the LDAP system), and a blog that's rarely been used. WordPress creates a lot of load on the servers and is just in general bloated. MySQL databases, dynamically generated pages, none of this is needed for our homepage, especially if we try to move everything to the wiki. In addition, the website (mainly the aforementioned login system) is susceptible to XSS attacks, among other vulnerabilities. Coupled with the massive amount of security holes that just appear to show up in WordPress all the time (https://www.cvedetails.com/vulnerability-list/vendor_id-2337/product_id-4096/), I'm honestly surprised we haven't migrated to anything else already.

My site (code at https://github.com/JonahAragon/opennic.org) is complete static HTML (which is compiled with Jekyll) homepage. It includes all the important features of our current site, even the closest servers information, with a cleaner, simpler design and setup. It places more emphasis on our top level domains, and it still includes a blogging system for future Press Releases and updates (which I think we should utilize more): https://jonaharagon.github.io/opennic.org/press/.

Because it's a static site, the security risks are nonexistent and it can be hosted anywhere. If this were to gather relatively good opinions from all of you, I'd push it to our organization at https://github.com/OpenNIC so anybody would be able to edit it (via Pull Requests). Ideally we could setup a system to automatically pull (from GitHub) and build the site on our webservers behind some lightweight server like Nginx. That way we'd be able to keep the existing servers and TLS functionality (which GH Pages does not support with custom domains) everything is just more open, compared with random WordPress administrators who as far as I can gather fall between the "not having enough time to update the site" and the "have no idea how to operate WordPress" categories.

Anyways, this was a really long email about a really simple topic. Sorry about that.

Hopefully all of you are on board,

Jonah

P.S. Also this would be the perfect time to switch to our opennic.org domain for the homepage and add some 301 redirects when we move, that'll just look nicer in general (and there'd be no need to move all the sites to that domain, at least not right away).
```
