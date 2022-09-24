---
title: Porting Hugo to New Computer
date: 2021-04-07T21:08:00-04:00
# lastmod: 2021-04-07T21:08:00-04:00
# author: Author Name
# authorlink: https://author.site
# cover: /img/cover.jpg
categories:
  - coding
tags:
  - coding
# showcase: true
# draft: true
---

Notes taken when I try to port hugo and my firebase website to a new computer

<!--more-->

I got new macbook and want to set up my website again.

### part i, git lone repo
git clone my website repository

example:
from my github, find the ssh clone link, then do: 

be sure to do submodule as well.

```
git clone --recurse-submodules -j8 git@github.com:arthasisacat/panini.git
```



### part ii: set up hugo and firebase 
follow most of things in this [link](https://www.smashingmagazine.com/2020/04/free-developer-blog-hugo-firebase/#comments-free-developer-blog-hugo-firebase)

0. set up nvm, npm, etc
[https://docs.npmjs.com/downloading-and-installing-node-js-and-npm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)
if you do it properly, later commands does **not** need `sudo`

1. set up hugo
```
brew install hugo
```

2. set up firebase
 
```
npm install -g firebase-tools

firebase login
```

3. pull submodule (for theme)
this step can be ignored if you do step I clone repo correctly.

source [link](https://discourse.gohugo.io/t/site-not-displaying-after-moving-files-from-linux-to-windows/31372)
```
git submodule update --init --recursive
```

### part iii: try it out
try to modify things and build hugo:
```
hugo
```

then deploy on firebase
```
firebase deploy
```
### part iv
create new post
```
hugo new posts/my-first-post.md
```
### part v troubleshooting
when deploy, I see this error
```
firebase deploy

Error: Failed to get Firebase project panini-everything. Please make sure the project exists and your account has permission to access it.
```

Solution:
```
firebase logout
firebase login
```




