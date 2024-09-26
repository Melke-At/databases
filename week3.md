###ex2q1
select * from goal;
![ex2q1.png](pictures%2Fex2q1.png)

###ex2q2
select NAME, type from airport where iso_country = "FI";
![ex2q2.png](pictures%2Fex2q2.png)

###ex2q3
select name from airport where iso_country = "FI" order by name;
![ex2q3.png](pictures%2Fex2q3.png)

###ex2q4
select name, type from airport where iso_country = "FI" order by type, name;
![ex2q4.png](pictures%2Fex2q4.png)

###ex2q5
select name from country where name like "F%";
![exc2q5.png](pictures%2Fexc2q5.png)

###exc2q6
select name from country where name like "%F%";
![exc2q6.png](pictures%2Fexc2q6.png)

###exc2q7
select location from game where screen_name = "vesa";
![exc2q7.png](pictures%2Fexc2q7.png)

###exc2q8
select co2_consumed from game where screen_name = "Ilkka";
![exc2q8.png](pictures%2Fexc2q8.png)

###exc2q9
select distinct co2_budget from game;
![exc2q9.png](pictures%2Fexc2q9.png)

###exc2q10
select screen_name, co2_budget, co2_consumed, (co2_budget - co2_consumed) As co2_left from game 
where screen_name = "Ilkka";
![exc2q10.png](pictures%2Fexc2q10.png)

###exc3q1
select country.name as "country name", airport.name as "airport name"
from airport, country
where airport.iso_country = country.iso_country and country.name = "Iceland";
![exc3q1.png](pictures%2Fexc3%2Fexc3q1.png)

###exc3q2
select airport.name as "airport name"
from airport, country
where airport.iso_country = country.iso_country and country.name = "France" and airport.type = "large_airport";
![exc3q2.png](pictures%2Fexc3%2Fexc3q2.png)

###ecx3q3
select country.name as country_name, airport.name as airport_name
from airport, country
where airport.iso_country = country.iso_country and country.continent = "AN";
![exc3q3.png](pictures%2Fexc3%2Fexc3q3.png)

###exc3q4
select elevation_ft
from airport, game
where location = ident and screen_name = "Heini";
![exc3q4.png](pictures%2Fexc3%2Fexc3q4.png)

###exc3q5
select elevation_ft*0.3048 as elevation_m
from airport,game
where location = ident and screen_name = "Heini";
![exc3q5.png](pictures%2Fexc3%2Fexc3q5.png)

###exc3q6
select name 
from airport,game
where location = ident and screen_name = "Ilkka";
![exc3q6.png](pictures%2Fexc3%2Fexc3q6.png)

###exc3q7
select country.name
from airport,game,country
where location = ident and airport.iso_country = country.iso_country and screen_name = "Ilkka";
![exc3q7.png](pictures%2Fexc3%2Fexc3q7.png)

###exc3q8
select name
from goal,goal_reached,game
where goal.id = goal_id and game.id = game_id and screen_name = "Heini";
![exc3q8.png](pictures%2Fexc3%2Fexc3q8.png)

###exc3q9
select airport.name
from airport, game, goal, goal_reached
where ident = location and game.id = game_id and goal.id = goal_id and screen_name = "Ilkka" and goal.name = "CLOUDS";
![exc3q9.png](pictures%2Fexc3%2Fexc3q9.png)

exc3q10
select country.name
from country, airport, game, goal, goal_reached
where airport.iso_country = country.iso_country and ident = location 
and game.id = game_id and goal.id = goal_id and screen_name = "Ilkka" and goal.name = "CLOUDS";
![exc3q10.png](pictures%2Fexc3%2Fexc3q10.png)
