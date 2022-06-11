# mysql-server

* [mysql介紹](#mysql介紹)
* [實作步驟](#實作步驟)
* [參考資料](#參考資料)
* [組員名單](#組員名單)
 
## mysql介紹
* MySQL是由麥克爾·維德紐斯所創造的，原本是一個開放原始碼的關聯式資料庫管理系統，現在分為免費的社群版與收費的標準版、企業版等。<br>
* 關聯式資料庫 
是以資料之間的關聯性為基礎架構的資料庫系統，通常把資料分類為資料表（table），然後再透過資料表之間的關聯性做查詢。

## 實作步驟
- Step-1 更新套件
```
 sudo apt update 
```
- Step-2 安裝mysql-server 
```
 sudo apt install mysql-server
```
![Image](https://raw.githubusercontent.com/wucan0315/wucan0315/main/%E5%AE%89%E8%A3%9Dmysql.jpg)
- Step-3 檢查mysql狀態 
**出現綠色的Active表示mysql正在運行
```
 sudo service mysql status
```
![Imag](https://raw.githubusercontent.com/wucan0315/wucan0315/main/%E6%AA%A2%E6%9F%A5mysql%E7%8B%80%E6%85%8B.jpg)<br>
ctrl+c即可跳出
- Step-4 登入mysql 
```
 sudo mysql -u root
```
![Image](https://raw.githubusercontent.com/wucan0315/wucan0315/main/%E7%99%BB%E9%99%B8mysql%E4%BC%BA%E6%9C%8D%E5%99%A8.jpg)
- Step-5 查看mysql伺服器中所有資料 
```
 show databases;
``` 
- Step-6 建立名為test的資料庫
```
 create database `test`;
```
![Image](https://raw.githubusercontent.com/wucan0315/wucan0315/main/%E5%BB%BA%E7%AB%8B%E8%B3%87%E6%96%99%E5%BA%AB.jpg)
- Step-7 進入名為test的資料庫
```
 USE `test`;
```
![Image](https://raw.githubusercontent.com/wucan0315/wucan0315/main/%E7%99%BB%E9%99%B8%E8%B3%87%E6%96%99%E5%BA%AB.jpg)
- Step-8 建立表格 
以下SQL敘述，可以建立名為users的表格，這個表格有兩個欄位。
第一個欄位是number，儲存的資料型別是int，且作為每列(row)資料的PRIMARY KEY(主鍵)。
第二個欄位是userid，儲存的資料型別是varchar(50)(最大可以存50個字元)。
```
create table users(
    number int,
    userid varchar(50),
    PRIMARY KEY (number)
);
```
![Image](![image](https://user-images.githubusercontent.com/106713917/173044372-6c92a23c-2169-48d5-b73c-25be337ca74f.png)

- Step-9  插入學號至users表格中
```
 insert into users values (1, 'b1042037') , (2, 'b1042034') , (3, 'b1042042');
```
![Image](https://user-images.githubusercontent.com/106713917/173044644-5949a608-1141-43be-85d7-e7a01be631de.png)

- Step-10 查看users表格中的資料
```
SELECT * FROM `users`;
```
![image](https://user-images.githubusercontent.com/106713917/173044745-75d376e4-2728-461d-b6b7-7141e181cbec.png)

- Step-11 刪除number為2的資料
```
delete from users where number = 2;
```
- Step-12 再次查看表格  <br>
![image](https://user-images.githubusercontent.com/106713917/173045075-9646ae21-44e1-48c9-a234-7c4e27237d22.png)  
- Step-13 刪除user的資料
```
drop table users;
```
![image](https://user-images.githubusercontent.com/106713917/173046942-6a3a3b88-2912-43a3-ac92-60ea029934da.png)
- Step-14 退出mysql 
```
 quit
```
![Image](https://raw.githubusercontent.com/wucan0315/wucan0315/main/%E9%9B%A2%E9%96%8Bmysql.jpg)

## 參考資料
[https://ui-code.com/archives/293](https://ui-code.com/archives/293)  <br>
[https://magiclen.org/ubuntu-server-mysql-php/](https://magiclen.org/ubuntu-server-mysql-php/)  <br>
[https://markdown.tw/](https://markdown.tw/)  <br>
[https://zh.wikipedia.org/wiki/MySQL](https://zh.wikipedia.org/wiki/MySQL])  <br>
[https://clay-atlas.com/blog/2019/11/21/sql-table-create-insert-update-remove-delete/](https://clay-atlas.com/blog/2019/11/21/sql-table-create-insert-update-remove-delete/)  <br>

## 組員名單 
b1042037吳奕燦 b1042034章嘉妏 b1042041卓家葳 
```
https://www.yannyann.com/2018/08/remove-mysql-mariadb-completely-and-recover/
```
