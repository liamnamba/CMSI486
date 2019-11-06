**2.1 – Project description, database engine used, potential users, maybe some other stuff**

As we outlined in the Preliminary Database Design Document, we are creating an athletic team database. We will be using MySQL to store and manage this data that will be keeping track of statistics for the Loyola Marymount Women's soccer team. These statistics will include all players and their key information as well as each game's information from the current season. The potential users of this database are coaches or athletic departments who want to keep track and seek out statistics for their players and games played. Players could also use this data to keep track of how they are performing in a given season and potentially identify areas for improvement.  

**2.2 – Data Dictionary, meaning a bullet list of the final tables/columns with a complete description of each**

The data stored will be individual player data and statistics. This will be data about each player and their accomplishments for the current soccer season. The season's game data and results will also be stored. The type of data will be integers and varchars. 


The database will include three entities/tables: 

- A player table to keep track of individual player data which will have attributes/columns: player name, player number, class year, position, and hometown. A players number will be the primary key since no two players on a team will have the same number, and we are only storing data for one team in our database.

- A game table which will keep track of each game's information with columns: game number, result, date, opponent, and location. The primary key in this table will be the game number, which will simply be the order in which the games were played. 

*There will be a participation relationship between these two entities which will include attributes goals scored in game and minutes played in game. *

- A statistics table to keep track of overall player accmplishments. In this table, there will be columns for player number, goals scored, assists, total minutes played, cards received, and games started. The primary key in this table will be the player number. The foreign key could either be player number, or player name.
We will potentially discover more data points as the project progresses. 

2.3 

![](https://github.com/liamnamba/CMSI486/blob/master/Project/new-erd.png)
 


