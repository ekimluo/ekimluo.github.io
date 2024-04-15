---
layout: post
title: An overview of how to build a free website hosted by Github pages
date: 2024-04-15
description: Here is a bird's-eye view, advanced quick-start guide to building a sophisticated website hosted by Github Pages.
tags:
  - coding
  - productivity
categories: tutorial
---
### Basics
I'm assuming a basic working knowledge of using `git` and Github. This short guide provides the general big-picture steps you should take to building your own website hosted by [Github Pages](https://jekyllrb.com/docs/github-pages/).

A website hosted by Github Pages typically uses [jekyll](https://jekyllrb.com/), a static site generator that is ideal for blogs and portfolio sites (like this one). Once deployed, your website should be in the default `<your-domain-name>.github.io` URL format.

I used the [al-folio](https://github.com/alshedivat/al-folio) template, which is a very popular one for academics. This theme also has great documentation and set-up instructions, so I recommend it. **This article is based on using the al-folio** theme. You can check out the [thousands of free Jekyll themes](https://jekyllthemes.io/free) if you want. Each theme has a slightly different configuration, so make sure to follow the setup instructions provided by the theme creator. However the general steps should be similar if not identical to the ones outlines below. 

#### What is required
##### Linux
I'm using Ubuntu 22.04.4 Jammy Jellyfish. Setting up the site via command line is relatively easy and straightforward *if you already have working knowledge of `git`*.

If you don't already have `git` installed, [do that first](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git). If you are also using a Debian-based distro, run the following:

```bash
sudo apt install git-all
git --version
```

- [ ] Obviously, you need to install `git` and have a Github account.
- [ ] [Install Ruby](https://www.ruby-lang.org/en/documentation/installation/). Note that your ruby version shouldn't be too old. I'm using `ruby 3.2.2`. For Debian-based distributions, run:

```bash
sudo apt-get install ruby-full
ruby -v
```

- [ ] You also need to install `bundler`. This is the Ruby gem manager, and you will need it to install all the gems required for your site. I'm using Bunder version 2.5.8. In command line, run:

```bash
gem install bundler
bundle -v
```

##### Windows
Follow [this article](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) to install `git` on Windows. I use [`git bash`](https://gitforwindows.org/) to manage everything via command line, though you can do this in whatever terminal of your choice. I installed ruby via command line too, but I'm sure you can download the latest version online.

### Basics steps of setting it up using a template
1. Create a remote repository using the `al-folio` theme. Follow the [setup instructions](https://github.com/alshedivat/al-folio/blob/master/INSTALL.md#installing-and-deploying) on how to do this.
2. Clone the repository to your local machine.
3. Run `bundle install` to install the necessary gems.
4. Run `bundle exec jekyll serve` to serve the site locally.
5. [Customize the repository](https://github.com/alshedivat/al-folio/blob/master/CUSTOMIZE.md) locally. Note that changes aren't reflected until you refresh the page. If you update the `_config.yml` file, you will need to restart the server.
6. Push changes to the remote repository.
7. The site should be live at `<your-domain-name>.github.io`. It usually takes a few minutes for the changes to be reflected.
8. Help Google index your site. Submit a sitemap to Google. The sitemap file should be located in the `_site` folder and called `site.xml`. The `url` format should be `<your-domain>.github.io/site.xml`.
9. [Claim your site in Google Search Console](https://support.google.com/webmasters/answer/9008080?hl=en). This will help you track the performance of your site in Google Search results.

### Tips
- Read the instructions carefully. Don't deviate from steps unless necessary.
- Always serve locally to preview website before pushing changes to remote.
- Learn about the folder and file structure. You will need to refer to the chart repeatedly.
- To ensure successful indexing, submit a sitemap to Google. The sitemap file should be located in the `_site` folder and called `site.xml`. The `url` format should be `<your-domain>.github.io/site.xml`.
- One annoying thing is that at the time of writing this, [Github Pages doesn't seem to be compatible with `mermaid` diagrams](https://github.com/orgs/community/discussions/13761). Since I like to write all my `markdown` notes in Obsidian and tend to diagram a lot, this wasn't ideal. However, a longer route is to use the [Mermaid live editor](https://mermaid.live/) and download the diagram as a `png` or `jpg` file, then upload it to your repository's image folder. 