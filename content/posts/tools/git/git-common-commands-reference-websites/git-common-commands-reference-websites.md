+++
title = "Git Common Commands Reference Websites"
author = ["Shawn Dennis Lin"]
date = 2020-11-30T00:00:00+08:00
lastmod = 2021-01-05T14:13:16+08:00
tags = ["git"]
categories = ["Tools"]
draft = false
hero = "/posts/tools/git/git-common-commands-reference-websites/images/git.jpg"
[menu.sidebar]
  parent = "git"
  weight = "auto"
  identifier = "git-commmands-websites"
  name = "Git Common Commands and Reference Websites"
+++

My note for git, there have many useful site to explain git command.  

<!--more-->


## Tutorial website {#tutorial-website}

-   [為你自己學 Git](https://gitbook.tw/)
-   [30天精通Git版本控管](https://ithelp.ithome.com.tw/users/20004901/ironman/525)
-   [Useful Git commands](https://docs.gitlab.com/ee/topics/git/useful%5Fgit%5Fcommands.html)


## Git configuration {#git-configuration}

-   [更新成符合 .gitignore 設定的追蹤狀態](https://blog.poychang.net/gitignore-and-delete-untracked-files/)
-   [auto save username and password in Git](https://stackoverflow.com/questions/35942754/how-to-save-username-and-password-in-git)
-   [Git 多平台换行符问题(LF or CRLF)](https://kuanghy.github.io/2017/03/19/git-lf-or-crlf)
-   [關於檔名的大小寫](https://gitbook.tw/posts/2018-06-05-case-sensitive)


## Common Command Reference Websites {#common-command-reference-websites}

| Command   | Ref1                                                                                                                                                                                                                                                    |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| branch    | [git远程删除分支](https://blog.csdn.net/qq%5F16885135/article/details/52777871)                                                                                                                                                                         |
| merge     | [分支和合併的基本用法](https://git-scm.com/book/zh-tw/v2/%E4%BD%BF%E7%94%A8-Git-%E5%88%86%E6%94%AF-%E5%88%86%E6%94%AF%E5%92%8C%E5%90%88%E4%BD%B5%E7%9A%84%E5%9F%BA%E6%9C%AC%E7%94%A8%E6%B3%95)                                                          |
| rebase    | [合併多個Commit](https://gitbook.tw/chapters/rewrite-history/merge-multiple-commits-to-one-commit.html)                                                                                                                                                 |
| submodule | [Git Submodule 的認識與正確使用](https://jhjguxin.github.io/blog/2012/04/19/git-submodule-de-ren-shi-yu-zheng-que-shi-yong-!/)                                                                                                                          |
| reset     | [利用 git reset 恢復檔案](https://blog.wu-boy.com/2010/08/git-%E7%89%88%E6%9C%AC%E6%8E%A7%E5%88%B6%EF%BC%9A%E5%88%A9%E7%94%A8-git-reset-%E6%81%A2%E5%BE%A9%E6%AA%94%E6%A1%88%E3%80%81%E6%9A%AB%E5%AD%98%E7%8B%80%E6%85%8B%E3%80%81commit-%E8%A8%8A%E6%81%AF/) |
| revert    | [git reset 與 git revert 的用處](https://bigboys-me.medium.com/%E8%AE%93%E4%BD%A0%E7%9A%84%E4%BB%A3%E7%A2%BC%E5%9B%9E%E5%88%B0%E9%81%8E%E5%8E%BB-git-reset-%E8%88%87-git-revert-%E7%9A%84%E7%94%A8%E8%99%95-6ba4b7545690)                               |


## Common Problem {#common-problem}

1.  When you try to change branches and get error with:  
    `error: The following untracked working tree files would be overwritten by checkout`  
    You may be able to solve your problem with [.gitignore and “The following untracked working tree files would be overwritten by checkout”](https://stackoverflow.com/questions/4858047/gitignore-and-the-following-untracked-working-tree-files-would-be-overwritten/14228841#14228841?newreg=7b0ffcab0a8e43eb9ad7c49c16295f14)
2.  Resolve git submodule conflict if submodule is not initialized  
    
    ```shell
    $ git diff sub
    diff --cc sub
    index 533da4e,ab2af77..0000000
    --- a/sub
    +++ b/sub
    @@@ -1,1 -1,1 +1,1 @@@
    ​- Subproject commit 533da4ea00703f4ad6d5518e1ce81d20261c40c0
     -Subproject commit ab2af775ec467ebb328a7374653f247920f258f3
    ++Subproject commit 0000000000000000000000000000000000000000
    ```
    
    You may be able to solve your problem with [How to resolve git submodule conflict if submodule is not initialized](https://stackoverflow.com/questions/26617838/how-to-resolve-git-submodule-conflict-if-submodule-is-not-initialized/31411086)
3.  if you use emacs, you might get the error when use git:  
    
    ```shell
    error:
    "git fatal: unable to auto-detect email address windows"
    ```
    
    you can try to modify `windows credentials` form following:  
    `Control Panel → All Control Panel Items → Credential Manager` and click `Windows Credentials`, to see `Generic Credentials`, and modify the **User name** and **Password**.  
    ![](/ox-hugo/windows-credentials.png)


## More {#more}

If you want to reference my .gitconfig, you can find that at [shdennlin/dotfiles/.gitconfig](https://github.com/shdennlin/dotfiles/blob/main/.gitconfig).
