# Sisäkyselyt

### Tehtävä 1
```sql
select name
from country
where iso_country in(
    select iso_country
    from airport
    where name like "Satsuma%"
);
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_4/images_sisa/4.1.png?raw=true)

### Tehtävä 2
```sql
select name
from airport
where iso_country in(
    select iso_country
    from country
    where name ="Monaco"
);
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_4/images_sisa/4.2.png?raw=true)

### Tehtävä 3
```sql
select screen_name
from game
where id in(
    select game_id
    from goal_reached
    where goal_id in(
        select id
        from goal
        where name ="CLOUDS"
    )
);
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_4/images_sisa/4.3.png?raw=true)

### Tehtävä 4
```sql
select country.name
from country
where iso_country not in(
    select airport.iso_country
    from airport
);
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_4/images_sisa/4.4.png?raw=true)

### Tehtävä 5
```sql
select goal.name
from goal
where id not in(
    select goal_id
    from goal_reached
    where game_id not in(
        select id
        from game
        where screen_name ="Heini"
    )
);
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_4/images_sisa/4.5.png?raw=true)