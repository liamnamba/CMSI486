**2.1 – Project description, database engine used, potential users, maybe some other stuff**

As we outlined in the Preliminary Database Design Document, we are creating an athletic team database. We will be using MySQL to store and manage this data that will be keeping track of statistics for the Loyola Marymount Women's soccer team. These statistics will include all players and their key information as well as each game's information from the current season. The potential users of this database are coaches or athletic departments who want to keep track and seek out statistics for their players and games played. Players could also use this data to keep track of how they are performing in a given season and potentially identify areas for improvement.  

**2.2 – Data Dictionary, meaning a bullet list of the final tables/columns with a complete description of each**

The data stored will be individual player data and statistics. This will be data about each player and their accomplishments for the current soccer season. The season's game data and results will also be stored. The type of data will be integers and varchars. 


The database will include three entities/tables: 

- A player table to keep track of individual player data which will have attributes/columns: player name, player number, class year, position, and hometown. A players number will be the primary key since no two players on a team will have the same number, and we are only storing data for one team in our database.

- A game table which will keep track of each game's information with columns: game number, result, date, opponent, location, and game ball. Game ball will represent the "MVP" for that specific game and will store the number of the player who received this award. The primary key in this table will be the game number, which will simply be the order in which the games were played. The foreign key in this table would be the Game ball with player number data. 

- A statistics table to keep track of overall player accmplishments for the current season with columns: player number, goals scored, assists, total minutes played, cards received, and games started. The surrogate key will be a number 0-30 for each player. The foreign key would be player number.

*2.3 – A complete finalized Entity-Relationship Diagram [ERD] for the database *

![](https://github.com/liamnamba/CMSI486/blob/master/Project/new-erd.png)
 


