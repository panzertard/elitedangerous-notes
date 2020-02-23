---
layout: post
title:  "Image path test - Markdown linked images"
categories: [debug]
tags: [markdown, debug]
---

# Test
This is a test to see at when path to assets such as images breaks in Markdown.  

#### leading slash
![assets-wo-baseurl](/assets/panzertard-sf.jpg)  
![assets-w-hardcoded-baseurl](/elitedangerous-notes/assets/panzertard-sf.jpg)  
![assets-w-relative-updir](/../assets/panzertard-sf.jpg)  

![assets-img-wo-baseurl](/assets/img/panzertard-sf.jpg)  
![assets-img-w-hardcoded-baseurl](/elitedangerous-notes/assets/img/panzertard-sf.jpg)  
![assets-img-w-relative-updir](/../assets/img/panzertard-sf.jpg)  

#### w/o leading slash
![assets-wo-baseurl](assets/panzertard-sf.jpg)  
![assets-w-hardcoded-baseurl](elitedangerous-notes/assets/panzertard-sf.jpg)  
![assets-w-relative-updir](../assets/panzertard-sf.jpg)  

![assets-img-wo-baseurl](assets/img/panzertard-sf.jpg)  
![assets-img-w-hardcoded-baseurl](elitedangerous-notes/assets/img/panzertard-sf.jpg)  
![assets-img-w-relative-updir](../assets/img/panzertard-sf.jpg)  

#### w dot slash
![assets-wo-baseurl](./assets/panzertard-sf.jpg)  
![assets-w-hardcoded-baseurl](./elitedangerous-notes/assets/panzertard-sf.jpg)  
![assets-w-relative-updir](./assets/panzertard-sf.jpg)  

![assets-img-wo-baseurl](./assets/img/panzertard-sf.jpg)  
![assets-img-w-hardcoded-baseurl](./elitedangerous-notes/assets/img/panzertard-sf.jpg)  
![assets-img-w-relative-updir](./assets/img/panzertard-sf.jpg)  
