--Steps to train the NLU model:
1.Open the command prompt
2.Navigate to the RASA base folder 
3.Use rasa train nlu command to train the nlu model

--Steps to run the actions:
1.Open the command prompt
2.Navigate to the RASA base folder 
3.Use command Rasa run actions
4.server should be up and running

--Steps to train the core model
1.Open the command prompt
2.Navigate to the RASA base folder 
3.Use rasa train -vv -dump-stories --force command to train the core model

--Dialouge Flow:
1.Greet the chatbot
2.Bot utters greet back
3.Give the query to do restaurant search
4.varaition for restaruant search query:
	0 indicates that entity is present and 1 indicates that the entity is not present in query
	Location cuisine
	0		1
	1		0
	1		1
	0		0
5.Validate city
6.validate cusine
7.ask budget
8.Display top 5 restaruants based on rating and preffered budget
9.ask for mail confirmation 
10.if the user wants the restaurant details in mail then send mail
11.validate email and send email
12.else dont send mail and end conversation

--Actions:
ActionSearchRestaurants -to process the restaurant query search
ActionDecideEmail - to validate the email id and to decide the dialouge flow based on the mail confirmation
ActionSendEmail - to send email with restaurant details
ActionCheckCity-to check the city is servisable by our foodie  chatbot
ActionValidateCuisine - to validate the cuisine

--Changes
To change user key for zomato api, go to actions.py file and replace "config" value  with the new user key
To change sender email id, go to actions.py file and  go to ActionSendEmail class and replace "fromaddr" defined.

--Files contiang user key
actions-py -line number 23,line number 128,

--Files conating slack token
Credentials.yml -- line number 16

--Files contiang from adress email id and password for same account
action.py file --line number 191,upgrad123



