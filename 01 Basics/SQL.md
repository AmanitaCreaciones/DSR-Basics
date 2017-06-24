# SQL basics

## Select all from a given table

SELECT * 

FROM tabla


## Select unique values from a given column in a table

SELECT DISTINCT col_1

FROM tabla

## Count values of a table/column

SELECT COUNT(col_1)

FROM tabla

## Select columns from a table given conditions, ordered and limited by the number of rows

SELECT col_1, col_2

FROM tabla

WHERE col_3 = || <= || >= || !=  'text'

AND || OR col_4 = number

LIMIT number

ORDER BY col_5 ASC || DESC, col_6 ASC || DESC

## Select columns from a table with condition between values

SELECT col_1, col_2

FROM tabla

WHERE col_3 BETWEEN || NOT BETWEEN 9 AND 10

## Select columns from a table given condition IN

SELECT col_1

FROM tabla

WHERE col_3 IN || NOT IN (1,2,'text')

## Select columns from a table given condition of similarity LIKE

SELECT col_1

FROM tabla

WHERE col_3 LIKE || NOT LIKE || ILIKE 'j%'

* ILIKE is not case sensitive

* _ => Match a single caracter

* % => Match sequence of caracters


## Aggregate functions

SELECT AVG || MEAN || MAX || MIN || SUM || ROUND((SUM(col_1))

FROM tabla

## GROUP BY columns from a table

SELECT col_1 , SUM(col_2)

FROM tabla

WHERE col_4 IN ('A','B')

GROUP BY col_1

HAVING SUM(col_2) > 20 

* HAVING wolks like WHERE but for grouped values

## Select columns/tables and rename them

SELECT col_1 AS columna

FROM tabla AS tb

## Select columns from a table given conditions

SELECT col_1

FROM tabla

## Select columns from a table given conditions

SELECT col_1

FROM tabla

## Select columns from a table given conditions

SELECT col_1

FROM tabla

## Select columns from a table given conditions

SELECT col_1

FROM tabla

## Select columns from a table given conditions

SELECT col_1

FROM tabla
