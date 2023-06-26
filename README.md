# DataBase_Practical
### Aggregate Functions
```
/* Aggregate Functions*/
CREATE TABLE BookDetails(
	BookId int,
	BookName varchar(255),
	Author varchar(255),
	Edition varchar(255),
	Publisher varchar(255),
	BookQuantity int,
	BookPrice int
);
INSERT INTO BookDetails VALUES(101,'IT','Deniz','5','FED',20,120);
INSERT INTO BookDetails VALUES(102,'Java','Kesh','2','SAW',30,520);
INSERT INTO BookDetails VALUES(103,'FullStack','Rashk','3','FREK',21,220);
INSERT INTO BookDetails VALUES(104,'C++','Lokesh','9','KIM',33,180);
INSERT INTO BookDetails VALUES(105,'C#','Laashk','6','NORTH',22,310);
INSERT INTO BookDetails VALUES(106,'CUDA','Hrish','7','WEST',28,160);
INSERT INTO BookDetails VALUES(107,'Parallel Computing','Krissh','4','AAIRE',21,190);
INSERT INTO BookDetails VALUES(108,'Python','Ken','5','DEV',20,200);
INSERT INTO BookDetails VALUES(109,'SQL','Mathew','3','KANYE',30,310);
INSERT INTO BookDetails VALUES(110,'Database Management','James','4','SCOT',26,340);
INSERT INTO BookDetails VALUES(111,'Probability','Kanan','13','KATTY',24,470);
INSERT INTO BookDetails VALUES(112,'Mern','Denver','8','GOMEZ',34,320);
INSERT INTO BookDetails VALUES(113,'MongoDB','Travis','2','GREY',12,400);
SELECT *FROM BookDetails;

SELECT COUNT(*) AS No_of_Books FROM BookDetails;
SELECT AVG(BookPrice) as Average_Price FROM BookDetails;
SELECT SUM(BookQuantity) as Total_Books FROM BookDetails;
SELECT MAX(BookPrice) as Maximum_Book_Price FROM BookDetails;
SELECT MIN(BookPrice) as Minimum_Book_Price FROM BookDetails;

```

### Date and Time
```
CREATE TABLE Customer(
	CustId int ,
	CustName varchar(255),
	Purchase varchar(255),
	PurchaseDate DATETIME,
	Store varchar(255),
	Price float
);
INSERT INTO Customer VALUES(201,'Rose','Stack','2023-01-12 12:12:23','LA',220.00);
INSERT INTO Customer VALUES(202,'Linda','SQL','2023-12-12 13:21:11','sedsa',310.00);
INSERT INTO Customer Values(203,'Kim','C++','2023-03-03 08:09:12','Eastr',234.00);
INSERT INTO Customer Values(104,'Kardas','C#','2012-12-01 23:12:54','Waq',241.23);
SELECT *FROM Customer;

SELECT CURTIME() AS currenttime;
SELECT CURDATE() AS currentdate;
SELECT NOW() AS DateTime;

SELECT CustId, PurchaseDate FROM Customer;

SELECT DATE(PurchaseDate) FROM Customer;
SELECT TIME(PurchaseDate) FROM Customer;
SELECT CustId , CustName , DATE(PurchaseDate) FROM Customer;
SELECT CustId , CustName , TIME(PurchaseDate) FROM Customer;
SELECT CustId , CustName , HOUR(PurchaseDate) FROM Customer;
SELECT CustId , CustName , MONTHNAME(PurchaseDate) FROM Customer;

SELECT EXTRACT(YEAR FROM '2023-11-21');

SELECT YEAR('2023-11-21');
SELECT MONTH('2023-11-21');
SELECT DAY('2023-11-21');
SELECT SECOND('13:22:12');
SELECT MINUTE('13:22:12');
SELECT HOUR("13:22:12");
SELECT MONTHNAME('2023-11-21');

SELECT DATE_ADD('2018-05-01',INTERVAL 1 DAY);
SELECT DATE_SUB('2018-05-01',INTERVAL 1 YEAR);
SELECT DATEDIFF('2007-12-31 23:59:59','2007-12-20');
SELECT DATE_FORMAT('1997-10-04 22:23:00','%D %a %b %Y %h %i %p') As DateFormatted;
```
### String Function
```
CREATE TABLE BookDetails(
	BookId int,
	BookName varchar(255),
	Author varchar(255),
	Edition varchar(255),
	Publisher varchar(255),
	BookQuantity int,
	BookPrice int
);
INSERT INTO BookDetails VALUES(101,'   IT Basics   ','Deniz','5','FED',20,120);
INSERT INTO BookDetails VALUES(102,'  Java Programming  ','Kesh','2','SAW',30,520);
INSERT INTO BookDetails VALUES(103,'  Full Stack Programming  ','Rashk','3','FREK',21,220);
INSERT INTO BookDetails VALUES(104,'C++ Programming','Lokesh','9','KIM',33,180);
INSERT INTO BookDetails VALUES(105,'C# Programming','Laashk','6','NORTH',22,310);
INSERT INTO BookDetails VALUES(106,'CUDA Programming','Hrish','7','WEST',28,160);
INSERT INTO BookDetails VALUES(107,'Parallel Computing','Krissh','4','AAIRE',21,190);
INSERT INTO BookDetails VALUES(108,'Python Programming','Ken','5','DEV',20,200);
INSERT INTO BookDetails VALUES(109,'SQL Programming','Mathew','3','KANYE',30,310);
INSERT INTO BookDetails VALUES(110,'Database Management','James','4','SCOT',26,340);
INSERT INTO BookDetails VALUES(111,'Probability','Kanan','13','KATTY',24,470);
INSERT INTO BookDetails VALUES(112,'Mern Programming','Denver','8','GOMEZ',34,320);
INSERT INTO BookDetails VALUES(113,'MongoDB Connectivity','Travis','2','GREY',12,400);
SELECT *FROM BookDetails;

SELECT BookId , UPPER(BookName) AS BookNameUppercase FROM BookDetails;
SELECT BookId , LOWER(Publisher) AS PublisherLowercase FROM BookDetails;

SELECT BookId , CONCAT(BookName,Author,Edition) AS CONCAT1 FROM BookDetails WHERE BookId<=105;
SELECT BookId , CONCAT_WS(',',BookName,Author,Edition) AS CONCAT2 FROM BookDetails WHERE BookId<=105;

SELECT BookId , LENGTH(BookName) AS LenghtofBook FROM BookDetails WHERE BookId<=103;
SELECT BookId , BIT_LENGTH(BookName) AS BitLenghtofBook FROM BookDetails WHERE BookId<=103;
SELECT BookId , CHAR_LENGTH(BookName) AS CharLenghtofBook FROM BookDetails WHERE BookId<=103;

SELECT BookId , FORMAT(BookPrice,4) AS Price FROM BookDetails;

SELECT BookId , REPEAT(Publisher,2) AS ReapeatPublisher FROM BookDetails WHERE BookId<=104;
SELECT BookId , REPLACE(Edition,Edition,5) AS ReplaceEdition FROM BookDetails WHERE BookId<=105;
SELECT BookId , REVERSE(Author) AS ReverseAuthor FROM BookDetails WHERE BookId<=103;

SELECT SPACE('7') AS SPACE;
SELECT TRIM(BookName) AS TrimBookName FROM BookDetails WHERE BookId<=103;
```
