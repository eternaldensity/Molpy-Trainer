# Molpy Trainer

xkcd: 1190: Time: Another Game

## Credits

Code by Eternal Density (and probably other OTTers)

Graphics likely by GLR and OTTers, when they are added

For personal amusement only.

## Changelog

### 0.009
- wooo lots of progress

### 0.008
- more progress
- changing how I'm setting server stuff up a little

### 0.007
- progress section
- todo secton
- committing from ubuntu!

### 0.006
- more molpy names

### 0.005
- some molpy names
- django hosting link

### 0.004
- Bag list
- start of object model
- some more useful links
- More molpy names

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

For the server scripting, I'll use Python. It looks like Django is worth using. (With postgresql, Gunicorn and NGINX)

## Molpy Name List
- Antelopey
- Badgermolp
- Bearraptor
- Beesnake
- Camolpy (camel)
- Centimolpy
- Chipmonpy
- Chirpy
- Chupamolpy 
- Deerpy
- Dolphy
- Dragonflopy
- Ecolipy (E. coli)
- Facebug
- Flutterbee
- Foxmolpy
- Goatpy
- Gatorraptor
- Geckolpy
- Guineamolp
- Hamply
- Kangamolp
- Keyboard
- Lizmolp
- Manapy (manatee)
- Meowlpy
- Millimolpy
- Molpanzee
- Molpanda
- Molpbear
- Molpicoot
- Molephant
- Molmmoth
- Molmot (marmot)
- Molpguin
- Molphish
- Molpidillo
- Molpouse
- Molpossum
- Molpy
- Molpybara
- Molpydile
- Molpyguana
- Molpymundi (coatimundi)
- Molpysnake
- Moltise (tortois)
- Monkeymolp
- Moopy (cow)
- Moosepy
- Murtle
- Neckpy (giraffe)
- Orcaraptor
- Owlpy
- Pricklymolp
- Quackmolpy
- Rabtor
- Raptor
- Raptorcat
- Raptorshark
- Ratpy
- Rhrinocerolpy
- Ribbit
- Sealpy
- Seawolpy
- Slowwormolpy
- Skunkpy
- Slothpy
- Sparrow-raptor
- Squirpy
- Trilobolpy
- Viperraptor
- Wallapy
- Waterottermolpy
- Wolpy (dog)
- Woolpy (sheep)
- Wormolpy
- Zemolp (zebra)

## Bag type list
- Shopping bag
- Paper bag
- Hessian bag
- Library bag
- Sports bag
- Lunch bag
- Plastic bag
- Coma bag
- Handbag
- Backpack
- Duffle bag
- Antistatic bag
- Bin bag
- Burn bag
- Diplomatic bag
- Messenger bag
- Popcorn bag
- Tea bag
- Punching bag
- Airbag
- Body bag
- Travel bag
- Tote bag
- Thermal bag
- Bowling bag
- Baguette bag
- Bucket bag
- Clutch bag
- Doctor's bag
- Envelope bag
- Feed bag
- Saddle bag
- Shoulder bag
- Sling bag
- Weekend bag
- Gift bag
- Chip bag (Doritos!)
- Wine bag

See http://bagbible.com/blog/bag-101/types-of-bags/ and http://en.wikipedia.org/wiki/Bag

## Object Model

Each User will be associated with 1 OTTer (trainer)

Each OTTer has many bags. Bags are held by 0 or 1 OTTer.

Bags may contain no Molpies, or multiple. A molpy may be in 0 or 1 bag.

The world is made up of regions which contain locations. Locations can contain OTTers, molpies, bags, and more, though these objects may only be in a single location.

Routes link locations to locations (where each route links 2 locations together). Routes will have a cost and other properties which govern how OTTers (and possibly molpies) can move between them.

Locations have a biome which affects the molpies that are in it (maybe the trainers too?) as well as the molpies that may be found in it.

A molpy is an instance of a breed. This affects the molpy's stats and abilities and how it reacts to biomes and training and what offspring it may have. Breeds may have subspecies which differ slightly from the main breed.

## Useful links

### Python Templating links

Basically stuff about Django and deployment and stuff to use it with

- https://docs.djangoproject.com/en/1.5/topics/templates/
- https://docs.djangoproject.com/en/1.5/topics/db/models/
- https://medium.com/cs-math/f29f6080c131 lots of useful info (11 things about django dev)
- http://michal.karzynski.pl/blog/2013/06/09/django-nginx-gunicorn-virtualenv-supervisor/ (am following this)
- http://goodcode.io/blog/django-nginx-gunicorn/ another about setting stuff up
- http://bailey.st/blog/2012/05/02/ubuntu-django-postgresql-and-nginx-a-rock-solid-web-stack/ looks about right (though a little older)
- https://bitbucket.org/DNX/django-fagungis/ should help with the above
- http://django-user-accounts.readthedocs.org/en/latest/ for user accounts
- http://www.dajaxproject.com/ for ajax: looks pretty awesome!
- http://djangofriendly.com/hosts/ hosting: webfaction sounds good (and has github support too, lol, that site happens to be hosted on it :D)
- http://www.dajaxproject.com/ dajax/dajaxice for django+ajax
- http://docs.celeryproject.org/en/latest/django/first-steps-with-django.html for celery

## Other tech links

- https://help.ubuntu.com/community/UsingTheTerminal because I'm an utter noob
- http://packages.ubuntu.com/lucid/vcs/mercurial-git because fagungis wants to use mercurial but I'm using github
- http://www.virtualenv.org/en/latest/ source bin/activate    deactivate
- to check nginx status /etc/init.d/nginx status
- http://www.celeryproject.org/ celery does async task/jobj queue stuff, including scheduling. written in Python!

## Progress

- Ubuntu installed in VirtualBox
- Git installed and this repo cloned
- Installed pip and django-fagungis
- Decided django-fagungis is too confusing for me and I'd better manually install stuff (see link marked 'am following this' above)
- Got django and postgresql working
- gunicorn seems to be working
- Yes it was working, it just needed nginx to actually send requests to it
- supervisor working (it starts gunicorn automatically, with all the right settings to start django)
- nginx is now working! had to copy the config into the sites-enabled directory rather than symlink the directories cos it choked on the directory. Or maybe I can symlink the file?

## Todo

### Basic server stuff

- celery?
- Figure out deployment process
- Maybe move into root/webapps rather than home/ed/webapps if I can figure out why pip wouldn't install django from there
- Get dajax going

### Actual project stuff

- Build a more complete conceptual object model
- Plan forms and views
- Build django python object structure
- Create views and forms
- Use admin interface to start adding stuff (molpy breeds! bags!) to database
- Figure out how to schedule tasks
- Write the game logic
- Style stuff better
- Hopefully it's getting close to something OTTers can use by this point and there are some remaining who haven't been basemented


