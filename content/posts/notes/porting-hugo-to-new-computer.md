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
### part ii: set up hugo and firebase 
follow most of things in this [link](https://www.smashingmagazine.com/2020/04/free-developer-blog-hugo-firebase/#comments-free-developer-blog-hugo-firebase)

1. set up hugo
```
brew install hugo
```
2. set up firebase
might need to add `sudo` 
```
npm install -g firebase-tools

firebase login
```

3. pull submodule (for theme)
source [link](https://discourse.gohugo.io/t/site-not-displaying-after-moving-files-from-linux-to-windows/31372)
```
git submodule update --init --recursive
```

### part iii
try to modify things and build hugo:
```
hugo
```

then deploy on firebase
```
firebase deploy
```



