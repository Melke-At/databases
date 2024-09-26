###exc4q1
select country.name as "country name", airport.name as "airport name"
from country inner join airport on airport.iso_country = country.iso_country
where country.name = "Finland" and scheduled_service = "yes";
![exc4q1.png](pictures%2Fexc4%2Fexc4q1.png)

###exc4q2
select screen_name, airport.name
from game inner join airport on location = ident;
![exc4q2.png](pictures%2Fexc4%2Fexc4q2.png)

###exc4q3
select screen_name, country.name
from game inner join airport on location = ident 
inner join country on airport.iso_country = country.iso_country;
![exc4q3.png](pictures%2Fexc4%2Fexc4q3.png)

###exc4q4
select airport.name, screen_name
from airport left join game on ident = location where name like "%Hels%";
![exc4q4.png](pictures%2Fexc4%2Fexc4q4.png)

###exc4q5
select name, screen_name
from goal left join goal_reached on goal.id = goal_id 
left join game on game.id = game_id;
![exc4q5.png](pictures%2Fexc4%2Fexc4q5.png)

###exc5q1
select name from country where iso_country in 
(select iso_country from airport where name like "Satsuma%");
![exc5q1.png](pictures%2Fexc5%2Fexc5q1.png)

###exc5q2
select name from airport where iso_country IN
(select iso_country from country where name = "Monaco");
![exc5q2.png](pictures%2Fexc5%2Fexc5q2.png)

###exc5q3
select screen_name from game where id in (select game_id
from goal_reached where goal_id in(select id from goal
where name = "CLOUDS"));
![exc5q3.png](pictures%2Fexc5%2Fexc5q3.png)

###exc5q4
select country.name from country where iso_country not in
(select airport.iso_country from airport);
![exc5q4.png](pictures%2Fexc5%2Fexc5q4.png)

###exc5q5
select name from goal where id not IN( select goal.id
from goal, goal_reached, game where game.id = game_id 
and goal.id = goal_id and screen_name = "Heini");
![exc5q5.png](pictures%2Fexc5%2Fexc5q5.png)
