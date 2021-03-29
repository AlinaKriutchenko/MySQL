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
If you later need to combine this table with tables from previous years. 
In this case avoid Year column when insert values and it will be added automatically);

## Another way to define primary key:
```
Place INT,
PRIMARY KEY(Place)
```
## Auto filling:
```
Place INT AUTO_INCREMENT,
```
## Select:
```
SELECT * FROM FORMULA_1_2020;
```
![Screenshot](/Images/1-4.png)

## Describe:
```
DESCRIBE FORMULA_1_2020;
```
![Screenshot](/Images/1-5.png)

## To drop the table:
```
DROP TABLE FORMULA_1_2020;
```
## Add columns:
```
ALTER TABLE FORMULA_1_2020 ADD Points INT(3);
ALTER TABLE FORMULA_1_2020 ADD Podiums INT(2);
ALTER TABLE FORMULA_1_2020 ADD Wins INT(2);
ALTER TABLE FORMULA_1_2020 ADD Haircolor VARCHAR(15);

SELECT * FROM F1_RESULTS_2020;
```
![Screenshot](/Images/1-7.png)

## Drop the column
```
ALTER TABLE FORMULA_1_2020 DROP COLUMN Haircolor;
```
![Screenshot](/Images/1-8.png)
## Add new column after another column
```
ALTER TABLE FORMULA_1_2020 ADD Nationality VARCHAR(30) AFTER Team;
```
![Screenshot](/Images/1-9.png)
## Insert values into the table
```
INSERT INTO F1_RESULTS_2020 VALUES(1, 'Lewis Hamilton', 'MERCEDES', 'Great Britain', 347, 14, 11);
INSERT INTO F1_RESULTS_2020 VALUES(2, 'Valtteri Bottas', 'MERCEDES', 'FIN', 223, 11, 2);
INSERT INTO F1_RESULTS_2020 VALUES(3, 'Max Verstappen', 'RED BULL RACING HONDA', 'NED', 214, 11, 2);
INSERT INTO F1_RESULTS_2020 VALUES(4, 'Sergio Pérez', 'RACING POINT BWT MERCEDES', 'MEX', 125, 2, 1);
INSERT INTO F1_RESULTS_2020 VALUES(5, 'Daniel Ricciardo', 'RENAULT', 'AUS', 119, 2, 0);
INSERT INTO F1_RESULTS_2020 VALUES(6, 'Carlos Sainz', 'MCLAREN RENAULT', 'ESP', 105, 1, 0);
INSERT INTO F1_RESULTS_2020 VALUES(7, 'Alexander Albon', 'RED BULL RACING HONDA', 'THA', 105, 2, 0);
INSERT INTO F1_RESULTS_2020 VALUES(8, 'Charles Leclerc', 'FERRARI', 'MON', 98, 2, 11);
INSERT INTO F1_RESULTS_2020 VALUES(9, 'Lando Norris', 'MCLAREN RENAULT', 'Great Britain', 97, 1, 0);
INSERT INTO F1_RESULTS_2020 VALUES(10, 'Pierre Gasly', 'ALPHATAURI HONDA', 'FRA', 75, 1, 1);

INSERT INTO F1_RESULTS_2020 VALUES(11, 'Lance Stroll', 'RACING POINT BWT MERCEDES', 'CAN', 75, 2, 0);
INSERT INTO F1_RESULTS_2020 VALUES(12, 'Esteban Ocon', 'RENAULT', 'FRA', 62, 1, 0);
INSERT INTO F1_RESULTS_2020 VALUES(13, 'Sebastian Vettel', 'FERRARI', 'GER', 33, 1, 0);
INSERT INTO F1_RESULTS_2020 VALUES(14, 'Daniil Kvyat', 'ALPHATAURI HONDA', 'RUS', 32, 14, 0);
INSERT INTO F1_RESULTS_2020 VALUES(15, 'Nico Hülkenberg', 'RACING POINT BWT MERCEDES', 'GER', 10, 14, 0);
INSERT INTO F1_RESULTS_2020 VALUES(16, 'Kimi Räikkönen', 'ALFA ROMEO RACING FERRARI', 'FIN', 4, 14, 1);
INSERT INTO F1_RESULTS_2020 VALUES(17, 'Antonio Giovinazzi', 'ALFA ROMEO RACING FERRARI', 'ITA', 4, 14, 0);
INSERT INTO F1_RESULTS_2020 VALUES(18, 'George Russell', 'WILLIAMS MERCEDES', 'Great Britain', 3, 14, 0);
INSERT INTO F1_RESULTS_2020 VALUES(19, 'Romain Grosjean', 'HAAS FERRARI', 'FRA', 2, 14, 0);
INSERT INTO F1_RESULTS_2020 VALUES(20, 'Kevin Magnussen', 'HAAS FERRARI', 'DEN', 1, 14, 0);

INSERT INTO F1_RESULTS_2020 VALUES(21, 'Nicholas Latifi', 'WILLIAMS MERCEDES', 'CAN', 0, 14, 0);
INSERT INTO F1_RESULTS_2020 VALUES(22, 'Jack Aitken', 'WILLIAMS MERCEDES', 'Great Britain', 0, 14, 0);
INSERT INTO F1_RESULTS_2020 VALUES(23, 'Pietro Fittipaldi', 'HAAS FERRARI', 'BRA', 0, 14, 0);

SELECT * FROM F1_RESULTS_2020;
```
![Screenshot](/Images/1-10.png)
## If need to delete the first row
```
FROM F1_RESULTS_2020 WHERE Place = 1;
```
## Replace values in the table
```
#REPLACMENT
UPDATE F1_RESULTS_2020
SET Nationality = 'GBR'
WHERE Nationality = 'Great Britain'
#Or to change on for Lewis Hamilton:
#WHERE Nationality = 'Great Britain' OR Name = 'Lewis Hamilton';

SELECT * FROM F1_RESULTS_2020;
```
![Screenshot](/Images/untitled.jpg)



