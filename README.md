# awesome_chocolates

Explorer Data Using Mysql

Skills used : Operator, Join, CTE, LIKE, CASE WHEN, GROUP BY <br>
Tools       : MySql


### Showing sales data where amount is greater than 10,000 by descending order
```
select * from sales
where amount > 10000
order by amount desc;
```

### BETWEEN condition in SQL with < & > operators
```
select * from sales
where boxes >0 and boxes <=50;
```

### Using year() function to select all data in a specific year
```
select SaleDate, Amount from sales
where amount > 10000 and year(SaleDate) = 2022
order by amount desc;
```

### Join
```
SELECT *
FROM Geo
Inner Join Sales ON Geo.GeoID = Sales.GeoID
```

```
SELECT *
FROM Sales
Right Join People ON Sales.SPID = People.SPID
```

### LIKE operator in SQL

```
select * from people
where salesperson like 'B%';
```

```
select * from people
where salesperson like '%B%';
```

### Using CASE to create branching logic in SQL

```
select 	SaleDate, Amount,
		case 	when amount < 1000 then 'Under 1k'
				when amount < 5000 then 'Under 5k'
                when amount < 10000 then 'Under 10k'
			else '10k or more'
		end as 'Amount category'
from sales;
```


### GROUP BY in SQL

```
select team, count(*) from people
group by team
```

### ORDER BY, GROUP BY in SQL

```
SELECT Amount, MAX(Amount)
FROM `sales` 
group by 1
order by amount desc
```

### MIN MAX in SQL

```
SELECT MIN(Amount)
FROM `sales` 
```

```
SELECT MAX(Amount)
FROM `sales` 
```

### Distinct in SQL

```
SELECT distinct(GeoID), Count(GeoID) as Hasil
FROM `sales`
group by 1
order by 1 asc
```

```
SELECT distinct(PID), Count(PID) as Hasil
FROM `sales`
group by 1
order by 2 desc
```
