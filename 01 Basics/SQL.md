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

## UNION of tables (one after the other)

	SELECT *

	FROM tabla_1

	UNION

	SELECT *

	FROM tabla_2

* UNION delete duplicated values

* UNION ALL doesn't delete duplicated values 

## INNER JOINs from tables

	SELECT T1.col_1,T1.col_2,T2.col_1,T2.col_2

	FROM tabla_1 AS T1

	INNER JOIN tabla_2 AS T2

	ON T1.col_1 = T2.col_1


* if both columns ID have the same name, instead of "ON T1.col_1 = T2.col_1" can be used "JOIN Tabla_2 USING(col_1)"

## Select columns from a table given conditions

	SELECT col_1

	FROM tabla

## Select columns from a table given conditions

	SELECT col_1

	FROM tabla

## Select columns from a table given conditions

	SELECT col_1

	FROM tabla



	
	SELECT film.title,actor.first_name 

	FROM film_actor

	LEFT JOIN actor 

	ON film_actor.actor_id = actor.actor_id

	LEFT JOIN film

	ON film.film_id = film_actor.film_id




	SELECT film.title , rental.return_date

	FROM rental

	LEFT JOIN inventory

	ON inventory.inventory_id = rental.inventory_id

	LEFT JOIN film

	ON film.film_id = inventory.film_id

	WHERE rental.return_date < '2005-05-28' AND rental.return_date >= '2005-05-27'


	SELECT * 

	FROM film

	LEFT JOIN inventory 

	ON inventory.film_id = film.film_id

	WHERE inventory.film_id IS NULL





	SELECT rental_rate, title

	FROM film

	WHERE rental_rate > (

		SELECT AVG(rental_rate)
  
		FROM film
  
		)
  
  
  
