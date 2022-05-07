---
title: Version control. Git.
subtitle: Hi! 👋 Today I will tell you about the git version control system. Let's get started!

# Summary for listings and search engines
summary: Hi! 👋 Today I will tell you about the git version control system. Let's get started!
# Link this post with a project
projects: []

# Date published
date: '2022-05-07T00:00:00Z'

# Date updated
lastmod: '2022-05-07T00:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/CpkOjOcXdUY)'
  focal_point: ''
  placement: 2
  preview_only: false

authors:
  - admin
  - 吳恩達

tags:
  - Academic
  - 开源

categories:
  - Demo
  - 教程
---

# About the version control system

What is a "version control system" and why is it important? A version control system is a system that records changes to a file or set of files over time and allows you to return later to a specific version. For file version control, this book will use the source code of the software as an example, although in fact you can use version control for almost any type of file.

If you are a graphic or web designer and you want to save every version of an image or layout (most likely you will), the version control system (hereinafter referred to as SLE) — just what you need. It allows you to return files to the state they were in before the changes, return the project to its original state, see the changes, see who last changed something and caused the problem, who set the task and when, and much more. Using SLE also means in general that if you have broken something or lost files, you can safely fix everything. In addition to everything, you will get it all without any extra effort.

# Local version control systems
Many people use copying files to a separate directory as a version control method (perhaps even a directory with a time stamp, if they are smart enough). This approach is very common because of its simplicity, but it is incredibly prone to errors. You can easily forget which directory you are in and accidentally change the wrong file or copy the wrong files that you wanted.

In order to solve this problem, programmers have long ago developed local SLE with a simple database that stores records of all changes in files, thereby monitoring revisions.

One of the most popular SLE was the RCS system, which is still distributed with many computers today. RCS stores on disk sets of patches (differences between files) in a special format, using which it can recreate the state of each file at a given time.

# Centralized version control systems
The next major problem that people face is the need to interact with other developers. In order to deal with it, centralized version control systems (CSCs) were developed. Systems such as CVS, Subversion, and Perforce use a single server containing all versions of files, and a number of clients that receive files from this centralized repository. The use of CSCS has been the standard for many years.

This approach has many advantages, especially over local SLE. For example, all project developers know to a certain extent what each of them is doing. Administrators have full control over who can do what, and it is much easier to administer the CSCS than to operate local databases on each client.

Despite this, this approach also has serious disadvantages. The most obvious disadvantage is a single point of failure represented by a centralized server. If this server goes down for an hour, then during this time no one will be able to use version control to save the changes they are working on, and no one will be able to share these changes with other developers. If the hard disk on which the central database is stored is damaged, and there are no timely backups, you will lose everything — the entire history of the project, not counting single repository snapshots that have been saved on local developer machines. Local SLE suffer from the same problem: when the entire project history is stored in one place, you risk losing everything.

# Distributed version control systems
This is where distributed version control systems (RCS) come into play. In RSKV (such as Git, Mercurial, Bazaar or Darcs), clients do not just download a snapshot of all files (the state of files at a certain point in time) — they completely copy the repository. In this case, if one of the servers through which the developers exchanged data dies, any client repository can be copied to another server to continue working. Each copy of the repository is a complete backup of all data.

Moreover, many RSCs can simultaneously interact with several remote repositories, thanks to this you can work with different groups of people using different approaches at the same time within the same project. This allows you to apply several approaches to development at once, for example, hierarchical models, which is completely impossible in centralized systems.

{{< figure src="https://raw.githubusercontent.com/wowchemy/wowchemy-hugo-modules/master/academic.png" title="The template is mobile first with a responsive design to ensure that your site looks stunning on every device." >}}

## Get Started

- 👉 [**Create a new site**](https://wowchemy.com/templates/)
- 📚 [**Personalize your site**](https://wowchemy.com/docs/)
- 💬 [Chat with the **Wowchemy community**](https://discord.gg/z8wNYzb) or [**Hugo community**](https://discourse.gohugo.io)
- 🐦 Twitter: [@wowchemy](https://twitter.com/wowchemy) [@GeorgeCushen](https://twitter.com/GeorgeCushen) [#MadeWithWowchemy](https://twitter.com/search?q=%23MadeWithWowchemy&src=typed_query)
- 💡 [Request a **feature** or report a **bug** for _Wowchemy_](https://github.com/wowchemy/wowchemy-hugo-modules/issues)
- ⬆️ **Updating Wowchemy?** View the [Update Tutorial](https://wowchemy.com/docs/hugo-tutorials/update/) and [Release Notes](https://wowchemy.com/updates/)

## Crowd-funded open-source software

To help us develop this template and software sustainably under the MIT license, we ask all individuals and businesses that use it to help support its ongoing maintenance and development via sponsorship.

### [❤️ Click here to become a sponsor and help support Wowchemy's future ❤️](https://wowchemy.com/plans/)

As a token of appreciation for sponsoring, you can **unlock [these](https://wowchemy.com/plans/) awesome rewards and extra features 🦄✨**

## Ecosystem

- **[Hugo Academic CLI](https://github.com/wowchemy/hugo-academic-cli):** Automatically import publications from BibTeX

## Inspiration

[Check out the latest **demo**](https://academic-demo.netlify.com/) of what you'll get in less than 10 minutes, or [view the **showcase**](https://wowchemy.com/user-stories/) of personal, project, and business sites.

## Features

- **Page builder** - Create _anything_ with [**widgets**](https://wowchemy.com/docs/page-builder/) and [**elements**](https://wowchemy.com/docs/content/writing-markdown-latex/)
- **Edit any type of content** - Blog posts, publications, talks, slides, projects, and more!
- **Create content** in [**Markdown**](https://wowchemy.com/docs/content/writing-markdown-latex/), [**Jupyter**](https://wowchemy.com/docs/import/jupyter/), or [**RStudio**](https://wowchemy.com/docs/install-locally/)
- **Plugin System** - Fully customizable [**color** and **font themes**](https://wowchemy.com/docs/customization/)
- **Display Code and Math** - Code highlighting and [LaTeX math](https://en.wikibooks.org/wiki/LaTeX/Mathematics) supported
- **Integrations** - [Google Analytics](https://analytics.google.com), [Disqus commenting](https://disqus.com), Maps, Contact Forms, and more!
- **Beautiful Site** - Simple and refreshing one page design
- **Industry-Leading SEO** - Help get your website found on search engines and social media
- **Media Galleries** - Display your images and videos with captions in a customizable gallery
- **Mobile Friendly** - Look amazing on every screen with a mobile friendly version of your site
- **Multi-language** - 34+ language packs including English, 中文, and Português
- **Multi-user** - Each author gets their own profile page
- **Privacy Pack** - Assists with GDPR
- **Stand Out** - Bring your site to life with animation, parallax backgrounds, and scroll effects
- **One-Click Deployment** - No servers. No databases. Only files.

## Themes

Wowchemy and its templates come with **automatic day (light) and night (dark) mode** built-in. Alternatively, visitors can choose their preferred mode - click the moon icon in the top right of the [Demo](https://academic-demo.netlify.com/) to see it in action! Day/night mode can also be disabled by the site admin in `params.toml`.

[Choose a stunning **theme** and **font**](https://wowchemy.com/docs/customization) for your site. Themes are fully customizable.

## License

Copyright 2016-present [George Cushen](https://georgecushen.com).

Released under the [MIT](https://github.com/wowchemy/wowchemy-hugo-modules/blob/master/LICENSE.md) license.
