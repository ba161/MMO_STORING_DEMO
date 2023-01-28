# MMO_STORING_DEMO

MMO storing demo is a program implementing saving method commonly used in MMO GAMES
we have used sqlite3 DBMS as persistent storage

the goal of this program is to show how different saving methods can be exploited if an attacker managed to find a consistent way of crashing the server 
and how to fix the issue 


this guide show the step implement different exploitation
(automatic) meaning by default the action is taken the first time the application opened ,
so there is no need to performe the action manually
duping:
<br>
1- open application
</br>
<br>
2- create vulnerable server
<br>
3- create user id = 0  (automatic)
<br>
4- login user id = 0  (automatic)
<br>
5- create user id = 1  (automatic)
<br>
6- login user id = 1  (automatic)
<br>
7- trade performed from user id = 0 to user id = 1 , ammount = 1500
<br>
8- logout user id = 1 
<br>
9- server crash
<br>
10- restart the application
<br>
11- create vulnerable server
<br>
<br>
*rolling back from undesired/desired outcome:
<br>
1- open application 
<br>
2- create vulnerable server
<br>
3- create user id = 0  (automatic)
<br>
4- login user id = 0  (automatic)
<br>
5- gamble 1500
<br>
6- crash server
<br>
7- restard the application
<br>
8- create vulnerable server
<br>
<br>
<br>
note!
<br>
this demo only simulate how server process game data ,and its interaction with the database
<br>
we eleminated many of the complexity that come with creating MMO  like client-side, network, etc
