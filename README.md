
# LolScout
### Purpose:
In the 5 v 5 Videogame/Esport two teams of 5 players compete against each other. 
Before the 'Game' start each player chooses 1 of (currently 133) characters, known as a champion. No two players may play the same champions. 
In ranked and professional play, players may "ban" a champion and prevent either side from choosing that champion. 
There are several common strategies for this 'Pick/Ban' phase:
1. Ban the "strongest" champion. 
2. Ban the champions that are strongest against champions your team is planning on picking. 
3. Ban the champions that (in professional play) you know your opponents are most succesful/ skilled with. 

Since a team only has 5 bans, and every banned champion is banned for both teams, evaluating these three goals (and which 5 champions are worth banning) is a difficult task for professional League of Legends teams. 

The purpose of the project was to make classifier (Team 1 winning being the target), that would help answer the question of how to optimally do pick ban, and to use that classifier's output to answer the above questions. 



```python

```

## Data-Pull:Gathering Data
This notebook shows the current version of my data collection process. 
It's three different functions:
The first uses a champion.gg api key to poll champion.gg for the  k/d/a  and win/loss percentage of every champion in champion.gg
I don't end up using this data (for reasons fully explained on http://www.drunkenthieves.com/blog/lol_scout/ )

The second goes through  a list of summoners that haven't had summary statistics scraped, and uses cassiopeia to get those statistics. 

The third goes through a list of summoners, gets all of the ranked matches the api will return, adds that to a dataframe, and adds summoners in those matches to the 'summoners to scrape' list. 

## Data-Prep:Imputing Data
This notebook shows the current data prep steps I use for the xbgoost and keras classifiers. 
Because of the data collected, a majority of the player's do not have W/L status for all champions or for the specific champion they play in that match.


## Simple Champion Selection Classifiers
The notebook 5v5 rps test (which stands for 5 v 5 rock paper scissors), shows how a classifier works ignoring all of the data except for the champions chosen by each team. 

## Keras/Xgbost Selection Classifiers with secondary statistics
This notebook shows the using classifiers with the prepped data from the data-prep notebook. Unfortunately the results are no better than the 'simple' models, which leads me to believe that I have insufficient data to build an effective model. 
