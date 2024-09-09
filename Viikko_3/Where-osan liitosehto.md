# Where-osan liitosehto

### Tehtävä 1
```sql
select country.name as "country name", airport.name as "airport name"
from country, airport
where airport.iso_country = country.iso_country
and country.name = "Iceland";
```
![Tehtävä](?raw=true)

### Tehtävä 2
```sql
select airport.name as "airport name"
from country, airport
where airport.iso_country = country.iso_country
and country.name = "France" and airport.type = "large_airport";
```
![Tehtävä](?raw=true)

### Tehtävä 3
```sql
select country.name as "country_name", airport.name as "airport_name"
from country, airport
where airport.iso_country = country.iso_country
and country.continent = "AN";
```
![Tehtävä](?raw=true)

### Tehtävä 4
```sql
select elevation_ft
from airport, game
where location = ident and screen_name ="Heini";
```
![Tehtävä](?raw=true)

### Tehtävä 5
```sql
select elevation_ft * 0.3048 as elevation_m
from airport, game
where location = ident and screen_name ="Heini";
```
![Tehtävä](?raw=true)

### Tehtävä 6
```sql
select airport.name
from airport, game
where game.location = airport.ident
and game.screen_name = "Ilkka";
```
![Tehtävä](?raw=true)

### Tehtävä 7
```sql
select country.name
from airport, game, country
where game.location = airport.ident
and airport.iso_country = country.iso_country
and game.screen_name = "Ilkka";
```
![Tehtävä](?raw=true)

### Tehtävä 8
```sql
select name
from goal, goal_reached, game
where game.id = game_id and goal.id = goal_id and screen_name = "Heini";
```
![Tehtävä](?raw=true)

### Tehtävä 9
```sql
select airport.name
from goal, goal_reached, game, airport
where game.id = game_id 
and goal.id = goal_id 
and airport.ident = location
and screen_name = "Ilkka";
```
![Tehtävä](?raw=true)

### Tehtävä 10
```sql
select country.name
from goal, goal_reached, game, airport, country
where game.id = game_id 
and goal.id = goal_id 
and airport.ident = location
and country.iso_country = airport.iso_country
and screen_name = "Ilkka";
```
![Tehtävä](?raw=true)

