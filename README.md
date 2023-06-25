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

### 
