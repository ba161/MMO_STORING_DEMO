# MMO_STORING_DEMO

MMO storing demo is a program implementing saving method commonly used in MMO GAMES
we have used sqlite3 as DBMS

the goal of this program is to show how different saving methods can be exploited if an attacker managed to find a consistent way of crashing the server 
and how to fix the issue 


this guide show the step implement different exploitation
(automatic) meaning by default the action is taken the first time the application opened ,
so there is no need to performe the action manually
duping:
<br>
1- open application
</br>
2- create vulnerable server
3- create user id = 0  (automatic)
4- login user id = 0  (automatic)
5- create user id = 1  (automatic)
6- login user id = 1  (automatic)
7- trade performed from user id = 0 to user id = 1 , ammount = 1500
8- logout user id = 1 
9- server crash
10- restart the application
11- create vulnerable server

*rolling back from undesired/desired outcome:
1- open application 
2- create vulnerable server
3- create user id = 0  (automatic)
4- login user id = 0  (automatic)
5- gamble 1500
6- crash server
7- restard the application
8- create vulnerable server



note!
this demo only simulate how server process game data ,and its interaction with the database
we eleminated many of the complexity that come with creating MMO  like client-side, network, etc
