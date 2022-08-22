# Genshin Artifact Rater

Discord bot that rates an artifact against an optimal 5* artifact. Put the command and image in the same message.


### Setup
Install python locally on your machine then get an API key from https://ocr.space.

Then install the required packages by running the following command
```
python3.8 -m pip install -r requirements.txt
```

Store environment variables for OCR Space by creating a file called `.env` with the following inside
```
OCR_SPACE_API_KEY=<key>

```
If you need a different language change the language variable in line 232 to your respective language from bellow

```
en(), es(), de(), fr(), vi(), pt(), ja(), pl(), ru(), tw(), cn(), it(), idn()
```

## Usage
Send the image to yourself in discord and open the source file.
Then copy the link and use it with the bot

```
python rate_artifact.py "discord image link"
```


#### Default Weights

ATK%, DMG%, Crit - 1 \
ATK, EM, Recharge - 0.5 \
Everything else - 0

### Options
#### Level
Compare to specified artifact level (defaults to parsed artifact level)
```
-rate lvl=20
```

#### Weights
Set custom weights (valued between 0 and 1)
```
-rate atk=1 er=0 atk%=0.5
```
\<stat> is any of HP, HP%, ATK, ATK%, ER (Recharge), EM, PHYS, CR (Crit Rate), CD (Crit Damage), ELEM (Elemental DMG%), Heal, DEF, DEF%


