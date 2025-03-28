---
title: PHP 入門
date: 2025-03-26 16:42:47
tags:
- php 
- 程式教學
categories: php 教學
description: php 簡介 - php 程式可以跟 HTML、CSS 等程式混用，但是檔名一定要 .php 。 PHP 程式是在主機上執行，所以在前端網頁使用檢視原始碼試看不到的，他是透過主機處理完之後才將結果傳給前端使用者...
---
### PHP 簡介
PHP 程式可以跟 HTML、CSS 等程式混用，但是檔名一定要 .php 。 PHP 程式是在主機上執行，透過主機將程式處理完之後才將結果傳給前端使用者，所以在前端網頁檢視原始碼看不到 PHP 程式。

### 開頭跟結尾
PHP 程式除了檔名要求 PHP 以外還需要開頭跟結尾用``` <?php ?> ```包起來，並且每段程式碼用 ; 做結尾。

```php
<?php 
    echo "我是簡易 PHP 範例";
?>
```

### 變數

在 PHP 語法裡變數不用另外的宣告，要以 $ 開頭。
#### 變數宣告規則
- 大小寫視為不同
- 變數只能使用英文字母、底線、數字(不能使用空白)
- 開頭只能英文或底線，不能使用數字當開頭
- 系統保留字不能用 如 array、while 其他 [保留字](http://php.net/manual/en/reserved.keywords.php)

#### 變數型態
- 整數(integer)
```php
<?php 
    $number = 10;
?>
```
- 字串(string)
```php
<?php 
    $text = "我是字串";
?>
```
- 布林值(booleam)
```php
<?php 
    $bool = True;
    $bool = False;
?>
```
- 陣列(Arrays)-以數字當索引值
```php
<?php 
    $arr[0] = "我是陣列0";
    $arr[1] = "我是陣列1";
?>
```
- 陣列(Arrays)-以字串當索引值(則字串稱為 鍵key)
```php
<?php 
    $arr['red'] = "#ff0000";
    $arr['green'] = "#00ff00";


    //使用時帶入 鍵key 就能得到值
    echo $arr['green']; //這樣會輸出 #00ff00
?>
```
### 註解
註解分兩種單行跟多行兩種
#### 單行註解
```php
<?php 
    // PHP 的單行註解
?>
```
#### 多行註解

```php
<?php 
    /* 
        PHP 的多行註解1
        PHP 的多行註解2
    */
?>
```

### 資料輸出
- 字串、數字輸出
```php 
<?php 
    //單純印出資料
    echo "我是資料";

    /*
        下面兩種方式都可以印出帶有變數的字串
        1.直接在 "" 加入變數
        2.使用 . 將字串跟變數相加
    */
    echo "印出第$num位";
    echo "印出第".$num."位";
?>
```
- 陣列輸出
```php 
<?php 
    $arr = {"#ff0000","#00ff00"};
    print_r($arr);
?>
```