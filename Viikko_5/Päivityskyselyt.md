# Päivityskyselyt

### Tehtävä 1
```sql
update game
set  location = (select ident from airport where name = "Nottingham Airport"), co2_consumed = co2_consumed+500
where screen_name = "Vesa";
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_5/images_paiv/5.1.png?raw=true)

### Tehtävä 2
goal_reached

![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_5/images_paiv/5.2.png?raw=true)

### Tehtävä 3
```sql
DELETE FROM goal_reached;
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_5/images_paiv/5.3.png?raw=true)

### Tehtävä 4
```sql
DELETE FROM game;
```
![Tehtävä](https://github.com/Kasanen/tietokannat/blob/main/Viikko_5/images_paiv/5.4.png?raw=true)