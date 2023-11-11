# CS 262 Monopoly Webservice for Lab09 and Homework03

This is the data service application for the 
[CS 262 sample Monopoly project](https://github.com/calvin-cs262-organization/monopoly-project),
And has been cloned for use in lab09 and homework03.
The lab/homework is deployed here:
          
- <https://stevenm-calvin-cs262lab09.azurewebsites.net/>

It has the following read data route URLs:
- <https://stevenm-calvin-cs262lab09.azurewebsites.net/> a hello message
- <https://stevenm-calvin-cs262lab09.azurewebsites.net/players/> a list of players
- <https://stevenm-calvin-cs262lab09.azurewebsites.net/players/1/> a single player with the given ID (1)
- <https://stevenm-calvin-cs262lab09.azurewebsites.net/players/-1/> return player not found
- <https://stevenm-calvin-cs262lab09.azurewebsites.net/blob/> undefined endpoint

Homework3:
- Join Query: 'SELECT Player.name, PlayerGame.score FROM Player, PlayerGame WHERE playerID=Player.id AND Player.id = ${id}'
- Function called from URL: "/playerscore/:id"
- example: <https://stevenm-calvin-cs262lab09.azurewebsites.net/playerscore/2/>

It is based on the standard Azure App Service tutorial for Node.js.

- <https://learn.microsoft.com/en-us/azure/app-service/quickstart-nodejs?tabs=linux&pivots=development-environment-cli>  

The database is relational with the schema specified in the `sql/` sub-directory
and is hosted on [ElephantSQL](https://www.elephantsql.com/). The database server,
user and password are stored as Azure application settings so that they aren&rsquo;t 
exposed in this (public) repo.
 
