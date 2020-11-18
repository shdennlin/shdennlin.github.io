+++
title = "Hugo and org-mode"
author = ["Shawn Dennis Lin"]
date = 2020-11-15T00:00:00+08:00
lastmod = 2020-11-19T00:31:34+08:00
tags = ["Hugo", "org-mode"]
categories = ["Blog"]
draft = false
hero = "/posts/Blog/Hugo/images/Hugo.png"
[menu.sidebar]
  parent = "blog"
  weight = "auto"
  identifier = "blog-hugo-and-org-mode"
  name = "Hugo and org-mode"
+++

This is my note for Hugo

<!--more-->


## Install {#install}

To see [Official Website](https://gohugo.io/getting-started/installing/)


## Tutorials {#tutorials}

-   [Getting Started](https://toha-guides.netlify.app/posts/getting-started/prepare-site/)(theme with Toha)


## Common command {#common-command}


### Create Site {#create-site}

```shell
hugo new site ./ -f=yaml --force
```


### Add theme {#add-theme}

```shell
git submodule add https://github.com/hugo-toha/toha.git themes/toha
```


### Run Site Locally {#run-site-locally}

```shell
hugo server -t toha -w
```

If you navigate to <http://localhost:1313>, you should see a basic site with Toha theme. In the next section, we are going to configure the site to look like the hugo-toha.github.io. As we have run the server in watch mode, any changes we make to the site will be instantly visible in the browser.


## Theme {#theme}

You can find the theme from [themes.gohugo.io](https://themes.gohugo.io/), these is my recommended theme:

1.  [Toha](https://themes.gohugo.io/toha/)(Download) [hugo-toha/toha](https://github.com/hugo-toha/toha)(GitHub) [hugo-toha/guides](https://github.com/hugo-toha/guides)(GitHub)


## org-mode + Hugo {#org-mode-plus-hugo}

-   [ox-hugo](https://ox-hugo.scripter.co/)
-   [博客写作流程之工具篇： emacs, orgmode, hugo & ox-hugo](https://www.xianmin.org/post/ox-hugo/)
-   [Blogging with org-mode and ox-hugo](https://www.shanesveller.com/blog/2018/02/13/blogging-with-org-mode-and-ox-hugo/)
