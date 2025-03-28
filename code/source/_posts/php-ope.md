---
title: PHP 運算子
date: 2025-03-26 18:21:43
tags:
- php 
- 程式教學
categories: php 教學
description: 從上篇 PHP 入門 我們了解了 PHP 基本的變數定義，在這篇會提到一些 PHP 常用的運算子，通常運算子分算術運算子、關係運算子兩種，...
---

從上篇 [PHP 入門](../php-c1/) 我們了解了 PHP 基本的變數定義，在這篇會提到一些 PHP 常用的運算子。
通常運算子有分三種
- 指定運算子
- 算術運算子
- 關係運算子
- 邏輯運算子


## 指定運算子
指定運算子就是我們常見的 "=" ，將右邊的結果存入左邊的變數內。
```php
<?php
    $a = 10;
    //將 10 存入 變數a
    $a = $b;
    //將 變數b 存入 變數a
?>
```

## 算術運算子
算術運算子顧名思義就是我們常用的算術符號(加、減、乘、除 等...)。
- (+) 相加
```php
<?php 
    $a = 1+1;  // 輸出結果 $a 會等於 2
?>
 ```
- (-) 相減
```php
<?php 
    $a = 2-1;  // 輸出結果 $a 會等於 1
?>
 ```
- (*) 相乘
```php
<?php 
    $a = 2*3;  // 輸出結果 $a 會等於 6
?>
 ```
- (/) 相除
```php
<?php 
    $a = 6/3;  // 輸出結果 $a 會等於 2
?>
 ```
- (%) 取餘數
```php
<?php 
    $a = 5%2;  // 輸出結果 $a 會等於 1
    $b = 6%2;  // 輸出結果 $a 會等於 0
?>
 ```
- (**) 次方
```php
<?php 
    $a = 5**2;  // 表示5的2次方，輸出結果 $a 會等於 25
?>
 ```

範例 ： BMI 計算
```php
<?php
/*
體重，單位是公斤
身高，單位是公尺
BMI公式是 體重 除以 身高的平方
*/
    $weight = 60;
    $height = 1.6;
    $bmi = $weight / ($height**2); 
    echo $bmi;
?>
 ```

### 增量賦值（Augmented Assignment）
等號左右如果都用到一樣的數值，可以使用增量賦值去縮短程式碼並增加可讀性
```php 
<?php 
$a = 1;
//正常來說如果要讓變數A+1會寫成這樣
$a = $a + 1;
//可以將$a 省略縮短成 
$a += 1;

// 使用其他算術運算子一樣可以這樣做
$b -= 1;
$c *= 1;
?>
```

## 關係運算子
- (>) 大於
```php
<?php 
   2 > 1 ;  // 輸出結果 true
?>
 ```
- (<) 小於
```php
<?php 
    2 < 1;  // 輸出結果 false
?>
 ```
 - (>=) 大於等於
```php
<?php 
    2 >= 1;  // 輸出結果 true
?>
 ```
 - (<=) 小於等於
```php
<?php 
    2 <= 1;  // 輸出結果 false
?>
 ```
 - (==) 等於
```php
<?php 
    2 == 2;  // 輸出結果 true
    /*這邊注意!! 如果使用 == 他是會忽略資料型態的，所以 數字2 會等於 字串2 */
    2 == '2' // 輸出結果 true
?>
 ```
 - (!=) 不等於
```php
<?php 
    2 != 2;  // 輸出結果 false
?>
 ```
 - (===) 完全等於
```php
<?php 
    2 == 2;  // 輸出結果 true
    /*使用 === 會加入資料型態的判斷，所以 數字2 不等於 字串2 */
    2 == '2' // 輸出結果 false
?>
 ```
 - (!==) 完全不等於
```php
<?php 
     2 !== 2;  // 輸出結果 false
?>
 ```
## 邏輯運算子
- 且(and、&&)
```php
<?php
var_dump(true and false);  //輸出 bool(false)
var_dump(true && false);   //輸出 bool(false)
?>
```
- 或(or、||)
```php
<?php
var_dump(true or false); //輸出 bool(true)
var_dump(true || false); //輸出 bool(true)
?>
```
- 非(!)
```php
<?php
var_dump(!false);  //輸出 bool(true)
var_dump(!true);   //輸出 bool(false)
?>
```
- 互斥或(xor) (兩個一樣是 false 兩個不一樣是 true)
```php
<?php
var_dump(true xor false); //輸出 bool(true)
var_dump(true xor true);  //輸出 bool(false)
?>
```
以上一些 PHP 常見的運算子就先介紹到這裡，接著我們下一篇將提到 php 常用的判斷及迴圈的流程。