+++
title = "EMACS"
author = ["Shawn Dennis Lin"]
date = 2020-11-24T00:00:00+08:00
lastmod = 2020-11-30T19:08:08+08:00
tags = ["emacs"]
categories = ["Editor", "tool"]
draft = false
hero = "/posts/emacs/images/emacs.png"
[menu.sidebar]
  weight = "auto"
  identifier = "emacs"
  name = "Emacs"
+++

My Emacs note.  

<!--more-->


## org mode {#org-mode}


### fundamental {#fundamental}

-   [Org-mode Frequently Asked Questions](https://mattduck.github.io/generic-css/demo/org-demo.html#Tables)(very useful)
-   [Org-mode基本功能](https://www.johneyzheng.top/2019/01/Org%5Fmode/)
-   [org-mode入門教程](http://fuzihao.org/blog/2015/02/19/org-mode%E6%95%99%E7%A8%8B/)
-   [emacs org-mode 的使用](https://www.wenhui.space/docs/02-emacs/emacs%5Forg%5Fmode/)
-   add date  
    -   use `C-c .` or `<SPC> d t` (Spacemacs) to insert date like [%Y-%m-%d %a]
    -   use `C-c !` or `<SPC> d T` (Spacemacs) to insert date like <%Y-%m-%d %a>
-   [Structure of Code Blocks](https://orgmode.org/manual/Structure-of-Code-Blocks.html)  
    -   [Code Blocks Languages](https://orgmode.org/manual/Languages.html#Languages)


### table {#table}

-   In spacemacs, you can use `, t t o` or `M-x org-table-toggle-coordinate-overlays` to toggle table coordinate.


### [Summary of In-Buffer Settings](https://orgmode.org/manual/In%5F002dbuffer-Settings.html) {#summary-of-in-buffer-settings}


#### `#+OPTIONS: num:t` {#plus-options-num-t}

在 github 上會顯示標號，如1 1 1.1 1.2 1.1.1等  


#### `#+STARTUP:` {#plus-startup}

|                |                           |
|----------------|---------------------------|
| overview       | top-level headlines only  |
| content        | all headlines             |
| showall        | no folding of any entries |
| showeverything | show even drawer contents |
