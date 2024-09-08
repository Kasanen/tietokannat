# Yhteen tauluun kohdistuvien kyselyiden harjoitukset

### Tehtävä 1
```sql
select * from goal;
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_3/3.1.png?raw=true)

### Tehtävä 2
```sql
select name as airport_type from airport where iso_country  ="FI";
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_3/3.2.png?raw=true)

### Tehtävä 3
```sql
select name from airport where iso_country  ="FI" order by name;
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_3/3.3.png?raw=true)

### Tehtävä 4
```sql
select name, type from airport where iso_country  ="FI" order by type asc, name asc;
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_3/3.4.png?raw=true)

### Tehtävä 5
```sql
select name from country where name like "F%";
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_3/3.5.png?raw=true)

### Tehtävä 6
```sql
select name from country where name like "%F%";
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_3/3.6.png?raw=true)

### Tehtävä 7
```sql
 select location from game where screen_name = "Vesa";
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_3/3.7.png?raw=true)

### Tehtävä 8
```sql
select co2_consumed from game where screen_name = "Ilkka";
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_3/3.8.png?raw=true)

### Tehtävä 9
```sql
select distinct co2_budget from game;
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_3/3.9.png?raw=true)