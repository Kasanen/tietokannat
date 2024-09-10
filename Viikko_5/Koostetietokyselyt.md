# Koostetietokyselyt

### Tehtävä 1
```sql
select max(elevation_ft)
from airport;
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_5/images_koos/5.1.png?raw=true)

### Tehtävä 2
```sql
select continent, count(*)
from country
group by continent;
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_5/images_koos/5.2.png?raw=true)

### Tehtävä 3
```sql
select screen_name, count(*)
from game, goal_reached
where id = game_id
group by screen_name;
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_5/images_koos/5.3.png?raw=true)

### Tehtävä 4
```sql
select screen_name
from game
where co2_consumed in(
    select min(co2_consumed)
    from game
);
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_5/images_koos/5.4.png?raw=true)

### Tehtävä 5
```sql
select country.name, count(*)
from airport, country
where airport.iso_country = country.iso_country
group by country.iso_country
order by count(*) desc
limit 50;
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_5/images_koos/5.5.png?raw=true)

### Tehtävä 6
```sql
select country.name
from airport, country
where airport.iso_country = country.iso_country
group by country.iso_country
having count(*) >=1000;
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_5/images_koos/5.6.png?raw=true)

### Tehtävä 7
```sql
select name
from airport
where elevation_ft in(
    select max(elevation_ft)
    from airport
)
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_5/images_koos/5.7.png?raw=true)

### Tehtävä 8
```sql
select name
from country
where iso_country in(
    select iso_country
    from airport
    where elevation_ft in(
        select max(elevation_ft)
        from airport
    )
);
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_5/images_koos/5.8.png?raw=true)

### Tehtävä 9
```sql
select count(*)
from game, goal_reached
where id = game_id and screen_name ="Vesa"
group by screen_name;
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_5/images_koos/5.9.png?raw=true)

### Tehtävä 10
```sql
select airport.name
from airport
where latitude_deg in(
    select min(latitude_deg)
    from airport
);
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_5/images_koos/5.10.png?raw=true)