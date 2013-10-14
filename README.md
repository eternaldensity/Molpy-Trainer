# Molpy Trainer

xkcd: 1190: Time: Another Game

## Credits

Code by Eternal Density (and probably other OTTers)

Graphics likely by GLR and OTTers, when they are added

For personal amusement only.

## Changelog

### 0.003
- More brainstorming
- Links to Django stuff
- Some more Molpies

### 0.002
- Design Planning and Molpy List

### 0.001
- Added this document

### 0.0
- nothing

## Design Planning

OTTers will need to sign into an account as a Molpy Trainer.

A Trainer will start out with a small amount of currency to trade for various items.

A Trainer must catch a molpy to train. Molpies are caught by putting bait in a bag.

Trainers can have multiple molpies.

Various items and activities (to be determined) will increase or decrease various traits and abilities of molpies.

Each kind of molpy has its own basic traits and abilities which will be uniquely customised by training.

Trainers can battle their molpies for prizes and bragging rights. (Or Bagging rights)

Combat will consist of several rounds, and different molpies will be designed for short matches, some long matches, some in the middle.

Trainers will select the match type and length.

Perhaps multiplayer battles. Teams even.

Cram everything full of OTTish words of course.

Pingpong balls will be involved somehow.

And grapevines. Lots of grapevines. At a 12:2 molpy:grapevine ratio

Could set it in the Netherlands: http://what-if.xkcd.com/imgs/a/53/drain_nl.png

There won't be so much javascript since the game logic will be carried out serverside.

For the server scripting, I'll use Python. It looks like Django is worth using. (With Gunicorn and NGINX)

## Molpy Name List
-Beesnake
-Chirpy
-Chupamolpy 
-Guineamolp
-Hamply
-Kangamolp
-Keyboard
-Lizmolp
-Meowlpy
-Molpy
-Molpbear
-Molpguin
-Molpidillo
-Molpysnake
-Owlpy
-Pricklymolp
-Raptor
-Raptorcat
-Raptorshark
-Rabtor
-Ribbit
-Sparrow-raptor
-Squirpy
-Waterottermolpy
-Wolpy
-Zemolp

## Useful links

### Python Templating links

- https://docs.djangoproject.com/en/1.5/topics/templates/
- https://docs.djangoproject.com/en/1.5/topics/db/models/
- https://medium.com/cs-math/f29f6080c131 lots of useful info
- http://michal.karzynski.pl/blog/2013/06/09/django-nginx-gunicorn-virtualenv-supervisor/ could be handy