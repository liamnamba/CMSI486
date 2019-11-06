**1.1 – Project description, database engine used, potential users, maybe some other stuff**

For our project, we will be creating an athletic team database using MySQL. This will keep track of all players on the Loyola Marymount University Women's Soccer team and their games and statistics. The potential users of this database are coaches or athletic departments who want to keep track and seek out statistics for their players and games played. 

**1.2 – Data description, generally what type of data will be stored**

The data stored will be individual player data and statistics. This will be data about each player and their accomplishments for the current soccer season. The season's game data and results will also be stored. The type of data will be integers and varchars. 

**1.3 – At least five examples of the type of data your database will provide to the user**

1) The database will provide the user with basic information about each player on the roster such as number, hometown, year, etc. 
2) The database will provide the user with dates for when each game was played and who it was against. 
3) The database will provide the user with the results of these games, letting the user know if it was won, tied, or lost. 
4) The database will provide the user with each player's individual statistics for each game such as time played. 
5) The database will provide the user with overall season statistics for each player on the team including goals scored, assists made, and games started. 

**1.4 – A preliminary idea of the schema of the database including table descriptions and potential columns**

The database will include three entities/tables: 


A player table which will have attributes/columns: player name, number, class year, position, and hometown with number being the primary key since no two players on a team will have the same number.


Second there will be a game table with columns for game number, result, date, opponent, and location. The primary key in this table will be the game number. There will be a participation relationship between these two entities which will include attributes goals scored in game and minutes played in game. 


The third entity will be the statistics table. In this table, there will be columns for player number, goals scored, assists, total minutes played, cards received, and games started. The primary key in this table will be the player number. The foreign key could either be player number, or player name.
We will potentially discover more data points as the project progresses. 

**2.1 – Project description, database engine used, potential users, maybe some other stuff**

As we outlined in the Preliminary Database Design Document, we are creating an athletic team database. We will be using MySQL to store and manage this data that will be keeping track of statistics for the Loyola Marymount Women's soccer team. These statistics will include all players and their key information as well as each game's information from the current season. The potential users of this database are coaches or athletic departments who want to keep track and seek out statistics for their players and games played. Players could also use this data to keep track of how they are performing in a given season and potentially identify areas for improvement.  

**2.2 – Data Dictionary, meaning a bullet list of the final tables/columns with a complete description of each**

The data stored will be individual player data and statistics. This will be data about each player and their accomplishments for the current soccer season. The season's game data and results will also be stored. The type of data will be integers and varchars. 


The database will include three entities/tables: 

- A player table to keep track of individual player data which will have attributes/columns: player name, player number, class year, position, and hometown. A players number will be the primary key since no two players on a team will have the same number, and we are only storing data for one team in our database.

- A game table which will keep track of each game's information with columns: game number, result, date, opponent, location, and game ball. Game ball will represent the "MVP" for that specific game and will store the number of the player who received this award. The primary key in this table will be the game number, which will simply be the order in which the games were played. The foreign key in this table would be the Game ball with player number data. 

- A statistics table to keep track of overall player accmplishments for the current season with columns: player number, goals scored, assists, total minutes played, cards received, and games started. The surrogate key will be a number 0-30 for each player. The foreign key would be player number.

**2.3 – A complete finalized Entity-Relationship Diagram [ERD] for the database**

The primary key for the players table is the player number. Since no player has the same number they will be no repeats. We added a field GameBall which links the statistics and games table. After every game 3 game balls are given to differnt players. Each gameball corresponds to a single game. The Games and Statistics table will have surragate keys as well.

![](https://github.com/liamnamba/CMSI486/blob/master/Project/erdv2.png)
 


