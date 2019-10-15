**1.1 – Project description, database engine used, potential users, maybe some other stuff**

For our project, we will be creating an athletic team database using MySQL. This will keep track of all players on the Loyola Marymount University Women's Soccer team and their games and statistics. The potential users of this database are coaches or athletic departments who want to keep track and seek out statistics for their players and games played. 

**1.2 – Data description, generally what type of data will be stored**

The data stored will be individual player data and statistics. This will be data about each player and their accomplishments for the current soccer season. The season's game data and results will also be stored. (names, numbers, sates) 

**1.3 – At least five examples of the type of data your database will provide to the user**

1) The database will provide the user with basic information about each player on the roster such as number, hometown, year, etc. 
2) The database will provide the user with dates for when each game was played and who it was against. 
3) The database will provide the user with the results of these games, letting the user know if it was won, tied, or lost. 
4) The database will provide the user with each player's individual statistics for each game such as time played. 
5) The database will provide the user with overall season statistics for each player on the team including goals scored, assists made, and games started. 

**1.4 – A preliminary idea of the schema of the database including table descriptions and potential columns**

The database will include three entities/tables. A player table which will have attributes/columns player name, number, class year, position, and hometown with number being the primary key since no two players on a team will have the same number. Second there will be a game table with columns for game number, result, date, opponent, and location. The primary key in this table will be the game number. There will be a participation relationship between these two entities which will include attributes goals scored in game and minutes played in game. The third column will be the statistics table. In this table, there will be columns for player number, goals scored, assists, total minutes played, cards received, and games started. The primaty key in this table will be the player number. 
We will potentially discover more data points as the project progresses. 


**1.5 – A complete preliminary Entity-Relationship Diagram [ERD] for the database**
