# Join

### Tehtävä 1
```sql
select country.name as "country name", airport.name as "airport name"
from country
inner join airport on airport.iso_country = country.iso_country
where country.name = "Finland" 
and scheduled_service = "yes";
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_4/images_join/4.1.png?raw=true)

### Tehtävä 2
```sql
select screen_name, airport.name
from airport
inner join game on game.location = airport.ident;
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_4/images_join/4.2.png?raw=true)

### Tehtävä 3
```sql
select game.screen_name, country.name
from airport
inner join game on game.location = airport.ident
inner join country on airport.iso_country = country.iso_country;
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_4/images_join/4.3.png?raw=true)

### Tehtävä 4
```sql
select airport.name, game.screen_name
from airport
left join game on game.location = airport.ident
where airport.name like "%Hels%"; 
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_4/images_join/4.4.png?raw=true)

### Tehtävä 5
```sql
select goal.name, screen_name
from goal
left join goal_reached on goal_id = goal.id
left join game on game.id = game_id;
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_4/images_join/4.5.png?raw=true)