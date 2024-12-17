
**create user**
first i thinks is create users in that case we can create a endpoint 
name: create user
path: /user/
method: Post 
body: 
{ "nombre": "Juan"}

status of the response: 200 ok , 400 (bad request)

![[Pasted image 20241216151555.png]]

thats teh page of teh frontend where i can put the information and when we push save it send the json whit the body 


**get users**
to get all the users to add them at the competition we need that information so, we need the players
name: get_users
path: /user/
method: get
response: { "id": 1, "nombre": "Juan"}

we feed the selector with the call of the api: 
![[Pasted image 20241216152312.png]]

**create competition**
in the same page we can create the competition , so we need the next things

name: create_competition
path: /competition/
method: post
body: { "competition_name": "mundial" , laps: 1, "Players": [ { "nombre": "Juan" }, { "nombre": "Pedro"}, { "nombre": "Paulo" } ]}

response: 200 ok 400 bad request





**get competition**
to create a career we need all the competitions created so we need the method get 

name: get_competitions
path: /competitions/
method: get 
response: 
{ "competition_name": "mundial" , laps: 1, "Players": [ { "nombre": "Juan" }, { "nombre": "Pedro"}, { "nombre": "Paulo" } ]}
![[Pasted image 20241216153740.png]]

**results of career**
after the competition we save the results of the career adding the places of the podium

name: Results_of_career
path: /Results/
method: post
body: {"name": "larry", "place1": 1, "place2": 0, "place3":0}

response: 200 ok 400 bad request


**get podium**
to get the podium we can filter the players and now which player was in the podium we ignore the others

name: get_results
path: /results/
method: get 
response: 
{ [ { "nombre": "Juan", "place 1": 1, "place2":0, "place3":0 }, { "nombre": "Pedro", "place 1": 1, "place2":0, "place3":0}, { "nombre": "Paulo", "place 1": 1, "place2":0, "place3":0 } ]}












