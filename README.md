# awesome_chocolates SQL - Jupyter Notebook

Explorer Data Using Jupyter Notebook + Mysql

Skills used : show tables, describe, select, disticnt, join, aggregate functions, Operator, Like, Case When <br>
Tools       : Jupyter Notebook + Mysql

### Show
```
show tables;
```

### Describe
```
desc geo;
```

### Select
```
select * from geo;
```

### Distinct
```
SELECT distinct(GeoID), Count(GeoID) as Hasil
FROM `sales`
group by 1
order by 1 asc;
```

### Join
```
SELECT *
FROM Geo
Inner Join Sales ON Geo.GeoID = Sales.GeoID order by geo asc limit 20;
```

### Aggregate Functions
```
select GeoID, sum(Amount), avg(Amount), sum(Boxes)
from sales
group by GeoID;
```

### Operator
```
select GeoID, Amount, Boxes 
from sales
where boxes >0 and boxes <=50 order by GeoID asc limit 20
```

### Like
```
select * from people
where salesperson like 'B%';
```

### Case When
```
select 	SaleDate, Amount,
		case 	when amount < 1000 then 'Under 1k'
				when amount < 5000 then 'Under 5k'
                when amount < 10000 then 'Under 10k'
			else '10k or more'
		end as 'Amount category'
from sales
limit 20
```