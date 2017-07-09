# LoLScout
A Data Science project in Finding optimal picks/bans for league of legends. 
Project initiated to teach the author machine learning using league of legends as a dataset. 

Data gathering Structure: 
Using some pre-seeded summoner ids, the systems gets all of the games players have played. 
For each game, it adds a line to two data frames (one data frame assumes role is what matters, the other assumes that pick order matters).  (assuming the game id doesn't exist in the index).
It also looks for any players that do not exist in the index, and adds them. 

After finishing all matches for all players, it saves out the csvs, and requests being run again. 

This is a version 1 data engineering design. This design is limited by the current riot api keys (keys only last 24 hours), meaning after 72000 requests a new riot api key must be gnerated. 
Version 2 will use sqlite for the databases. 
Version 3 will generate a full postgresql database. 

There is a companion program that goes to champion.gg, and pulls all of the stats for a champion by role. 
To explain the ids in that program. 
1 is top, 2 is jungle, 3 is mid, 4 is adc, 5 is support. The format is 
position_championid_mm_dd_yy_patch
so 3_001_07-09-2017-7.11 is  annie (champion id 1) mid (position 3) on 7-09-2017 for patc 7.11





##Disclaimer LoLScout isn't endorsed by Riot Games and doesn't reflect the views or opinions of Riot Games or anyone officially involved in producing or managing League of Legends. League of Legends and Riot Games are trademarks or registered trademarks of Riot Games, Inc. League of Legends © Riot Games, Inc.