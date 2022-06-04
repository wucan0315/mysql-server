# mysql-server


## 什麼是mysql
一種資料庫
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
出現綠色的Active表示mysql正在運行
```
 sudo service mysql status
```
- Step-4 登入mysql 
```
 sudo mysql -u root
```
![Image](https://raw.githubusercontent.com/wucan0315/wucan0315/main/%E7%99%BB%E9%99%B8mysql%E4%BC%BA%E6%9C%8D%E5%99%A8.jpg)
- Step-5 查看mysql伺服器中所有資料 
```
 SHOW DATABASES;
``` 
- Step-6 建立名為dbname的資料庫
```
 CREATE DATABASE `dbname`;
```
![Image](https://raw.githubusercontent.com/wucan0315/wucan0315/main/%E5%BB%BA%E7%AB%8B%E8%B3%87%E6%96%99%E5%BA%AB.jpg)
- Step-7 進入名為dbname的資料庫
```
 USE `dbname`;
```
![Image](https://raw.githubusercontent.com/wucan0315/wucan0315/main/%E7%99%BB%E9%99%B8%E8%B3%87%E6%96%99%E5%BA%AB.jpg)
- Step-8 建立表格 
以下SQL敘述，可以建立名為users的表格，這個表格有兩個欄位。
第一個欄位是userid，儲存的資料型別是tinyint SIGNED(有號8-bit整數)，必須NOT NULL(不能是空的)，且作為每列(row)資料的PRIMARY KEY(主鍵)，會AUTO_INCREMENT(自動遞增)。
第二個欄位是username，儲存的資料型別是varchar(50)(最大可以存50個字元)。
```
 CREATE TABLE `users` (
     `userid` tinyint SIGNED NOT NULL PRIMARY KEY AUTO_INCREMENT,
     `username` varchar(50)
);
```
![Image](https://raw.githubusercontent.com/wucan0315/wucan0315/main/%E5%89%B5%E5%BB%BA%E8%A1%A8%E6%A0%BC.jpg)

- Step-9  插入學號至users表格中
```
 INSERT INTO `users` (`username`)
     VALUES ('學號');
```
![Image](https://raw.githubusercontent.com/wucan0315/wucan0315/main/%E5%8A%A0%E5%85%A5%E5%AD%B8%E8%99%9F%E8%87%B3%E8%A1%A8%E6%A0%BC%E4%B8%AD.jpg)

- Step-10 查看users表格中的資料
```
SELECT * FROM `users`;
```
![Image](https://raw.githubusercontent.com/wucan0315/wucan0315/main/%E6%9F%A5%E7%9C%8B%E8%A1%A8%E6%A0%BC%20.jpg)
- Step-11 退出mysql 
```
 quit
```
![Image](https://raw.githubusercontent.com/wucan0315/wucan0315/main/%E9%9B%A2%E9%96%8Bmysql.jpg)
