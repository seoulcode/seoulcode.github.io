---
layout: post
title:  "[linux] xterm config"
date:   2019. 11. 26. (화) 13:59:31 KST
categories: [linux, tool]
---

xterm의 설정이다. 

1. 자신의 home디렉토리에 .Xresources파일을 만든다.
1. 파일 내용을 아래와 같이 추가한다.
**.Xresources 파일 내용**
```bash
xterm*utf8: 1
xterm*faceName: Fira Code Retina:size=10
xterm*faceNameDoublesize: NanumGothicCoding:size=9
xterm*background: black
xterm*foreground: white
xterm*utf8Title: true
xterm*boldMode: false
```
1. `$> sudo reboot` or `$> xrdb -merge ~/.Xresources`

