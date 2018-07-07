---
layout: post
title: "Announcements Page"
date: 2018-06-29
category:
  - Meta
  - a.sks.jda.mn
author: Jonah Aragon
---
<div id="posting"></div>
We have renamed the "Press Releases" page to a more general "Announcements" section. This change is intended to open up posting to all DNS server operators, to have a web and RSS based platform to inform users of potential planned or unplanned downtime, announcing servers in new locations, or announcing the removal of servers.

### Posting new announcements

The "Server Announcement" section is open to any Tier 1 or 2 operator to post server operation related announcements, such as maintenance or downtime. Posting is simple via the GitHub web interface, requiring only a GitHub account and basic [Markdown](https://guides.github.com/features/mastering-markdown/) knowledge.

To create a new post, [click here](https://github.com/opennic/opennic-web/new/master/_i18n/en/_posts).

After logging into GitHub, you'll see a text box entitled "Name your file". Enter a filename in the following format:

```
YYYY-MM-DD-Name-of-your-post.md
```

For example, I could enter `2018-06-29-ns11.opennic.org-maintenance.md`:

![](/assets/images/git-filename.png)

Next, in the area below, at the very top of the file, include the following section:

```
---
layout: post
title: "Name of your post"
date: 2016-06-29
category:
  - Server Announcement
  - nsXX.XXX.XX.dns.opennic.glue
author: Your Name
---
```

Replacing, of course, the title, date, server hostname (as a category), and author name (which can be either your real name or username).

![](/assets/images/git-frontmatter.png)

Now, below that "front matter", you can write your post. Even just a simple post noting details like expected downtime will go a long way towards achieving communication between our users and operators. At the bottom of this post will be sample templates you can use. If you use a template, feel free to add or remove any details as necessary.

Next, scroll to the bottom of that page and click the green "Propose new file" button. You don't have to fill in all the text boxes above necessarily.

![](/assets/images/git-pr.png)

This will bring you to a "Comparing changes" window. Ensure `base: master` is selected in the first dropdown, then click the green "Create pull request" button:

![](/assets/images/git-comparing-changes.png)

**Finally**, on the next page click the green "Create pull request" button.

![](/assets/images/git-pr-confirm.png)

At this point, an organization administrator (likely either `@JonahAragon` or `@Fusl`) will approve your post as soon as possible. If your post is urgent, ping somebody on IRC and we can take a look at it faster. At that point, your post will be pushed to the website and RSS feeds.

#### Template: Planned Maintenance

```
Hello,

I am taking nsXX.dns.opennic.glue down for maintenance.

The server will be down for the next 24 hours.

**Notable Changes**

- Bug fixes
- Removed logging
- Something else?
```

#### Template: Unplanned Maintenance

Note: I would refrain from posting announcements such as these unless you believe the server may be down for a significant amount of time (perhaps a reflection attack?).

```
The server nsXX.dns.opennic.glue is currently offline due to unplanned circumstances. We are working on a solution, in the meantime, consider switching your DNS servers to maintain stable DNS resolution.

Potential Alternative Servers:

- Feel free to offer alternative servers your users could use, either other servers you operate or other servers nearby.
```

#### Template: Phasing Out

```
Hello,

I am planning on shutting down nsXX.dns.opennic.glue in 14 days. All users of this server should switch to an alternative as soon as possible. They are currently listed as "Disabled" on the servers page.
```
