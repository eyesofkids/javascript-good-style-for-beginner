# 命名

## 前言

對於函式、變數的命名，對於中文的初學者是第一個挑戰，首要的原因是因為我們並非英文語系國家的開發者，對於英文的專業字詞當然會有很多不熟悉的地方。以下提供一些基本的指引。

## 程式碼檔案的命名

對於JavaScript中的檔案名稱，以下提供幾個建議給初學者參考:

1. 如果沒有其它特別規定，一律使用全小寫英文

與下一節中程式碼中識別名稱命名的規則不同，我會建議使用全小寫的命名，主要的原因是有些作業系統中，對於檔案名稱大小寫是視為同樣的。當然這是有例外的，有些函式庫或框架可能會要求其它的檔案命名方式會較為合適。

2. 路徑與檔案名稱，不能用中文或有空白字元

使用中文的開發者有時候會在檔案的路徑中，或是檔案名稱使用中文，這些都是經常會造成檔案執行上的錯誤或無法執行的原因。當然檔案的名稱中也不能使用空白字元。

3. 用連接符號(-)和點(.)來區分英文字詞與版本編號

用連接符號(-)和點(.)這兩種符號來區分檔案的英文字詞或是版本編號，例如`jquery.plugin-1.4.2.js`這樣的命名。少用下底線(_)的原因是有時候會看成是空白。

## 識別名的命名

> 直接總結: 除了類別或是特別的函式外(註: 例如React的元件)，其它都用小駝峰。

一個良好的命名會有其規則，目前最常使用的是大駝峰式與小駝峰命名法，命名規則也只一種慣例，並無強制性，目的是容易識別和可讀性。不過，當你或你的團隊一旦選用好要使用哪一種命名規則，在整個應用程式中，編寫時應保持一致性。

大駝峰式(upper camel case)

又稱為 Pascal(巴斯卡) 命名法，指的是每個單字的第一個英文字母會是大寫的，例如`DisplayInfo`或是`MyButton`。

小駝峰式(lower camel case)

指的是每個單字的第一個英文字母會是小寫的，例如`myData`或是`myName`。

當你要定義各種函式、類別、變數或常數的識別名稱時，應該使用上述的的命名方式，例如定義一個名字的變數識別名時，你當然可以定義成為`myname`、`my_name`、`my-name`、`MY_NAME`、`myName`...各種名稱，但目前各種新式的程式語言中，我會建議使用`myName`或`MyName`兩種。

在某些情況中，會使用`MY_NAME`這種專門常數的命名規則，或是你有可能看到某些有自己風格的函式庫命名，像是PHP語言中常見的利用下底線的命名，例如`$my_name`這種，我們在JavaScript剛開始學習時比較少見。

以簡單的各種命名情況，什麼時候要用大駝峰，什麼時候要用小駝峰以下是一個簡單的列表:

- Classes(類別) - PascalCase 大駝峰
- Methods(方法) - camelCase 小駝峰
- Properties(屬性) - camelCase 小駝峰
- Functions(函式) - camelCase 小駝峰
- Variables(變數/常數) - camelCase 小駝峰

## 通用命名規則

### 少用簡寫或自己發明縮寫

> 使用整個的字詞，不要任意縮寫或簡寫

不好的命名: setBgColor / 好的命合: setBackgroundColor
不好的命名: userAdr / 好的命名: userAddress
不好的命名: fName, lName / 好的命名: firstName, lastName

### 語意不明或對象不明

> 動作需要有明確的針對對象

不好的命名: insert() 這是要插入什麼？/ 好的命名: insertDiv()
不好的命名: name 這是什麼名稱？/ 好的命名: memberName
不好的命名: isOk() 什麼東西ok不ok？ / 好的命名: isConnected 連上線了嗎？

### 不要拼錯英文單字

> 字典是你的好朋友

錯誤的拼字: memuItem / 正確的拼字: menuItem
錯誤的拼字: pueryString / 正確的拼字: queryString

## 變數(常數)的識別名稱

變數(常數)經常代表的是一種名詞，名詞也有單複數的型態，複數通常是給陣列使用的命名，代表多個個體。

字串或物件類型是用單一個英文名詞最為明顯，以下為範例:

```text
firstName
clock
dog
```

> 註: 因為JavaScript是動態資料類型的關係，為了容易分辨變數是什麼資料類型的，某些開發者會偏好在變數(常數)名稱前加上它的類型，而且常用簡寫，例如`num, str, bool, obj, arr, func`等等，這也是一種方式。

字串類型要很容易看得出的話，用以下的開頭或是包含在其中的字詞，就可以一眼看出是字串:

```text
string
name
description
label
text
```

數字類型的話，在英文字詞中和中文也是類似的，有些特別的名詞，就有隱含為數字類型的，例如以下幾個常用的:

> 計數/金額類

```text
cost
price
total
count
amount
```

> 長寬高等計量單位

```text
length
width
height
area (面積)
weight
volume (體積)
```

> 其它常見

```text
age
year
day
time (hour, minute, second)
degree
speed
id
```

> 註: id值不一定，但通常從資料庫來的資料最常見用數字

那麼，要如何命名例如"本班所有學生的數量"或是有多少某個物品的數量，有以下幾種:

```text
studentCount
totalStudent
numberOfStudent
```

陣列之類的集合結構，有數量很多的意思，大部份都用"複數"型態的字詞，或者資料的類型來分別，也可以在後面加上`Array`或`List`來代表是一個列表或陣列例如:

```text
studentArray
students
todoList
```

布林值通常都以`is`或`has`開頭，例如以下的範例:

```text
isEmpty
hasBasket
```

> 對於日期與時間有很多種命名方式，在JavaScript裡，Date 這個物件包含了年月日時分秒與微秒值，而不是英文字典上的單指"日期"而已。

## 函式的識別名稱

函式通常指的是對某些個體或群體作的動作與行為，所以最簡單的想法就是`動詞+名詞`的命名方式。如果針對的是整體，後面的名詞就用`all`就行了。

> 常用的動作詞（函數用）開頭

```text
set 設定
get 獲得
use 使用
add 加上、相加
delete/remove 移除
update 更新
make/take 作某…事
move 移動
submit 提交
check 檢查
insert 單體
extend append 展開
print/display/show 印出/顯示
log 記錄
list 列出
reset 重置
link 連至
repeat 重覆
replace 取代
find search 尋找
format 格式化
open close 打開/關閉
subscribe/unsubscribe 訂閱/取消訂閱
clear 清除
xxxxTo 到xxx
```

## 參考

- https://stackoverflow.com/questions/3742650/naming-conventions-for-number-of-foos-variables