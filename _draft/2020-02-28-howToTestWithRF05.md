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

選擇存放路徑, 為測試專案命名 : **Test**
<figure class="foto-legenda">
	<img src="{{"/assets/img/maruIMG/2020/0226_rf/07.png"}}">
</figure>

由於這個測試案例會用到web dirver,  
我們先點選專案**Test** > 點選 **Edit** tab > 點選 **Library**  
輸入
```
   selenium2library  
```
<figure class="foto-legenda">
	<img src="{{"/assets/img/maruIMG/2020/0226_rf/11.jpg"}}">
</figure>

導入成功後就會出現在library欄位囉  
(如果出現紅字或導入不成功, 請記得回去[安裝篇](https://gitmaruneko.github.io/2020/02/17/howToTestWithRF01.html)檢查有沒有成功安裝selenium2library)
<figure class="foto-legenda">
	<img src="{{"/assets/img/maruIMG/2020/0226_rf/12.jpg"}}">
</figure>

### 建立測試案例
測試專案建立後, 請滑鼠右鍵點選專案名稱**Test**  > **New Test Case**

<figure class="foto-legenda">
	<img src="{{"/assets/img/maruIMG/2020/0226_rf/06.png"}}">
</figure>





## Other

### 無法顯示Robot Framework報告
```
  System.setProperty("hudson.model.DirectoryBrowserSupport.CSP", "")
```

### Reference
* [Jenkins Plugin - Robotframework](https://plugins.jenkins.io/robot/)