---
layout: post
title:  "初探Robot Framework之結合Jenkins持續整合 - 05"
image: ''
date: 2020-02-28 23:50
cover: '/assets/img/maruIMG/2020/0223_rf/rf01.png'
tags:
- test
- robotframework
- QA

description: ''
categories: ''
serie: 
---

## 準備工作

本教學由安裝Robot Framework套件開始  
請預先裝好Jenkins環境 > [安裝Jenkins](https://jenkins.io/download/)

## [安裝Robot Framework套件](https://plugins.jenkins.io/robot/)

* 至Jenkins工作站 > **Manage Jenkins** > **Manage Plugins**
* 點選 **Available** > 搜尋 **Robot Framework**
<figure class="foto-legenda">
	<img src="{{"/assets/img/maruIMG/2020/0226_rf/10.jpg"}}">
</figure>

* 安裝完成後, 回到 **Manage Jenkins** >  **Configure System**
  找到Robot Framework選項, 勾選 ☑**Display "Robot Results" column in the job list view**
  這個選項可以讓我們在工作主頁面看到Robot Framework的建置結果


## 在Jenkins建立Robot Frameowrk任務

### 建立測試專案
開啟RIDE, 點選右上角**File** > **New Project**  

<figure class="foto-legenda">
	<img src="{{"/assets/img/maruIMG/2020/0226_rf/05.png"}}">
</figure>









### 無法顯示Robot Framework報告
```
  System.setProperty("hudson.model.DirectoryBrowserSupport.CSP", "")
```

### Reference
* [Jenkins Plugin - Robotframework](https://plugins.jenkins.io/robot/)