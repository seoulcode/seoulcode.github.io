---
layout: post
title:  "[centos] yum install kernel-devel"
date:   2019-11-20 17:00:21 +0900
categories: [centos, package]
---

kernel-devel에서 원하는 버전을 설치하기 

**cmd :**
```
yum install "kernel-devel-uname-r == $(uname -r)"
```
