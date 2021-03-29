# MySQL Basics


This tutorial covers MySQL basic functionality with the example of Formula 1 2020 Driver Standings table.

## Create Table


```
CREATE TABLE F1_RESULTS_2020 (
    Place INT PRIMARY KEY,
    Name VARCHAR(30) UNIQUE,
    Team VARCHAR(25) NOT NULL
    #Year INT(4) DEFAULT '2020'
);
```



![Screenshot](/images/1-4.png)

