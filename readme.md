### Pitch Perfect

Overall Hypthesis: The catcher has a bigger influence on the pitching sequence and what a pitcher will throw next.


## Installation

Pybaseball can be installed via pip:

pip install pybaseball
or from the repo (which may at times be more up to date):

git clone https://github.com/jldbc/pybaseball
cd pybaseball
python setup.py install


**** Need to install Homebrew: brew install git-lfs for the large files to be able to push to Github


*** Must add *.csv to gitignore as you will not be able to commit these season files to github all files >50mb



Will use 2015-2017 seasons of the top 50 pitchers


Data Dictionary
ab_idat-bat ID. First 4 digits are year. Matches with ab_id in pitches.csv
batter_idplayer ID of the batter. Given by MLB, player names found in player_names.csv
eventdescription of the result of the at-bat
g_idgame ID. First 4 digits are year
inninginning number
onumber of outs after this at-bat
p_scorescore for the pitcher's team
p_throwswhich hand pitcher throws with. Single character, R or L
pitcher_idplayer ID of the pitcher. Given by MLB, player names found in player_names.csv
standwhich side batter hits on. Single character, R or L
topTrue if it's the top of the inning, False if it's the bottom


At Bat Columns

ab_idat - bat ID. First 4 digits are year. Matches with ab_id in pitches.csv
batter_id - player ID of the batter. Given by MLB, player names found in player_names.csv
event - description of the result of the at-bat
g_id - game ID. First 4 digits are year
inning - inning number
o - number of outs after this at-bat
p_score - score for the pitcher's team
p_throws - which hand pitcher throws with. Single character, R or L
pitcher_idplayer ID of the pitcher. Given by MLB, player names found in player_names.csv
stand - which side batter hits on. Single character, R or L
topTrue - if it's the top of the inning, False if it's the bottom

1= Fastball 2= Offspeed 3= Breaking Ball
Pitch Type Definitions
* FT - Two-seam Fastball- 1
* FC - Cutter- 1
* FF - Four-seam Fastball- 1
* SI - Sinker- 1
* FS - Splitter- 2
* CH - Changeup- 2
* SL - Slider- 3
* KC - Knuckle curve- 3
* CU - Curveball- 3

Acquire:
Downloaded the data set via Kaggle: https://www.kaggle.com/pschale/mlb-pitch-data-20152018

plan of attack:
(try a neural network) 
Predict pitches: 1=fastball 2= offspeed 3= Breaking pitch

1. run a prediction based on just the count- LR MVP .43
2. " ", runners on base- LR=.42
3. " ", score- LR=.42
4. " ", inning, pitch count
4. " ", handness of batter

5. " ", isolate catcher 
(Hypothesis)


