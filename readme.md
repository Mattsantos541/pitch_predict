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