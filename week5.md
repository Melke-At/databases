###exc6q1
SELECT max(elevation_ft) FROM airport);
![exc6q1.png](pictures%2Fexc6%2Fexc6q1.png)

###exc6q2
select continent, COUNT(*) 
from country group by continent;
![exc6q2.png](pictures%2Fexc6%2Fexc6q2.png)

###exc6q3
select screen_name, COUNT(*) from game, goal_reached
where id = game_id group by screen_name;
![exc6q3.png](pictures%2Fexc6%2Fexc6q3.png)

###exc6q4
SELECT screen_name FROM game where co2_consumed IN
(SELECT MIN(co2_consumed) FROM game);
![exc6q4.png](pictures%2Fexc6%2Fexc6q4.png)

###exc6q5
select country.name, count(*) from airport, 
country where airport.iso_country = country.iso_country
group by country.iso_country order by count(*) desc limit 50;
![exc6q5.png](pictures%2Fexc6%2Fexc6q5.png)

###exc6q6
select country.name from airport, country
where airport.iso_country = country.iso_country
group by country.iso_country having count(*) > 1000;
![exc6q6.png](pictures%2Fexc6%2Fexc6q6.png)

###exc6q7
SELECT NAME from airport WHERE
elevation_ft in(select MAX(elevation_ft) FROM airport);
![exc6q7.png](pictures%2Fexc6%2Fexc6q7.png)

###exc6q8
select name from country where iso_country in (
select iso_country from airport where elevation_ft in(
select max(elevation_ft) from airport));
![exc6q8.png](pictures%2Fexc6%2Fexc6q8.png)

###exc6q9
select count(*) from game, goal_reached
where id = game_id and screen_name = "Vesa"
group by screen_name;
![exc6q9.png](pictures%2Fexc6%2Fexc6q9.png)

###exc6q10
select name from airport where latitude_deg 
in(select min(latitude_deg) from airport);
![exc6q10.png](pictures%2Fexc6%2Fexc6q10.png)

###exc7q1
update game set  location = (select ident from airport where 
name = "Nottingham Airport"), co2_consumed = co2_consumed+500
where screen_name = "Vesa";
![exc7q1.png](pictures%2Fexc7%2Fexc7q1.png)

###exc7q2
from goal_reached

###exc7q3
#delet FROM goal reached;
delete from goal_reached
where goal_id = "9" and game_id = "5";
![exc7q3.png](pictures%2Fexc7%2Fexc7q3.png)

###exc7q4
delete from game;
select * from game;
![exc7q4.png](pictures%2Fexc7%2Fexc7q4.png)