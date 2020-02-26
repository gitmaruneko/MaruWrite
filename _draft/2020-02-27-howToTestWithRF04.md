---
layout: post
title:  "初探Robot Framework之小試身手 - 03"
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
第一個練習以WEB GUI為主  
在開始建立測試案例之前, 請先至[此網站-PHP and MySQL](http://thedemosite.co.uk/addauser.php)建立測試帳號 :
* username: test
* password: test

<figure class="foto-legenda">
	<img src="{{"/assets/img/maruIMG/2020/0226_rf/10.jpg"}}">
</figure>

## 開始第一個測試案例  

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








### Reference
* [WEB sample(http://thedemosite.co.uk/login.php)