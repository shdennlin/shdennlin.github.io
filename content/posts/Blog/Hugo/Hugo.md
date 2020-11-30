+++
title = "Hugo and Org-mode"
author = ["Shawn Dennis Lin"]
date = 2020-11-15T00:00:00+08:00
lastmod = 2020-11-30T18:44:52+08:00
tags = ["Hugo", "org-mode"]
categories = ["Blog"]
draft = false
hero = "/posts/blog/hugo/images/hugo.png"
[menu.sidebar]
  parent = "blog"
  weight = "auto"
  identifier = "blog-hugo-and-org-mode"
  name = "Hugo and Org-mode"
+++

This is my note for Hugo + Emacs.  

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


### useful plugins in emacs {#useful-plugins-in-emacs}

1.  [ox-hugo](https://github.com/kaushalmodi/ox-hugo/tree/f24c9bd522ae22bee2327c2b53858d0a5066707d)(Github)  
    
    `ox-hugo` is an Org exporter backend that exports Org to Hugo-compatible Markdown (Blackfriday) and also generates the front-matter (in TOML or YAML format).  
    
    If you use spacemacs, you can use `, e e H` or `SPC m e e H` to export org file to markdown.  
    For More information about spacemacs , please see [spacemacs/org](https://github.com/syl20bnr/spacemacs/tree/develop/layers/%2Bemacs/org).

2.  [eaxy-hugo](https://github.com/masasam/emacs-easy-hugo/tree/dffe165de354c2e6dc16510edad09839e69fdd35)(Github)
3.  [prodigy](https://github.com/rejeep/prodigy.el/tree/6ae71f27b09b172f03fb55b9eeef001206baacd3)(Github)  
    
    Manage external services from within Emacs.  
    If you use spacemacs, you can use `<SPC> a t p` to see a list of all defined services.  
    For More information about spacemacs , please see [spacemacs/prodigy](https://github.com/syl20bnr/spacemacs/tree/develop/layers/%2Btools/prodigy).
