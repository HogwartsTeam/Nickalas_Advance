# Utaha

[![forthebadge made-with-python](http://ForTheBadge.com/images/badges/made-with-python.svg)](https://www.python.org/)
[![\[Telegram\] aiogram live](https://img.shields.io/badge/telegram-aiogram-blue.svg?style=flat-square)](https://t.me/aiogram_live)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
[![Actively Maintained](https://img.shields.io/badge/Maintenance%20Level-Actively%20Maintained-green.svg)](https://gist.github.com/cheerfulstoic/d107229326a01ff0f333a1d3476e068d)

![logo](https://telegra.ph/file/9e4dfb7c9cf54bf295271.jpg)


 මෙම බූතයන්ගේ සම්පුර්න අයිතිය
 [Hogwarts](https://t.me/HogwartsPlus) කන්ඩායම සතු වේ
 අනවසරයෙන් පිටපත් කිරිම සපුරා තහනම්

## group
[Hogwarts Bots](https://t.me/HogwartsGhosts)
* check the notes using /notes comand

## Special thanks for
* [utah](https://t.me/Kasumiutahabot)
* Hasindu Theekshana
* Rex
* And all Hogwarts Admins
## Deploy to heroku

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/hirushakeeth/utah.git)
## Saurce cords are written by
 < [matheesha](https://t.me/percy_jackson_4)
 ## Are you have any questin
 please contact [this person](https://t.me/percy_jackson_4)
 
## THE EASY WAY to Deploy 

### Follow the methord carefully
```
1) Create an account at https://heroku.com

```
```
2) Get APP_ID and API_HASH from my.telegram.org
```

```
3) Create a new bot from @botfather and copy its api token

```
![api](https://telegra.ph/file/9770210e1205bce0e06bb.png)

```
4) Click Deploy
```
[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/hirushakeeth/Daisy.git)
```
5) create redis database and copy uri like this yog get this from redislabs.com

```
![redis](https://telegra.ph/file/1fa95b98f6e435e178dbd.jpg)
```
30)    create mongodb cluster and get it uri
```
![mongodb](https://youtu.be/hkmc3e7U7R4)

```
36 Paste the Api token copied at token space

```
![Token](https://telegra.ph/file/83574a44d10a89ea8e4d9.png)
```
7) Enter url of the app ass https://#Appneme.herokuapp.com

8) Enter TL_APP_ID (Get from my.telegram.org 's API Development tools)

9) Enter TL_API_HASH (Get from my.telegram.org 's API Development tools)

```
![url](https://telegra.ph/file/5b159343abc4d3a369ac0.png
```
10)Then Deploy

11) After Deploy over click manage app
```
```
12) Goto Resources and Turn Worker Emilia to on (by clicking edit)

```
![worker](https://telegra.ph/file/eed4d6b0a2177bf7cdf76.png)
```
13) Goto Logs and check for the errors
```
![logs](https://telegra.ph/file/06409b6ce522d005a3ad4.png)
```


*A message for Experts*
     - Always you can change the owner name id and other settings when publishing..
     - The bots owner infomations present at Emilia/Modules/Lang/id.py and en.py.
     - Paste your coffeehouse api to activate your own chatbot.
     - You can remove entry Daisy logo in Main.py.
     - Link your Credit card to Heroku for get extra amount of dynos.
     
*I am just a learner and this is the code I used as MissDaisyRobot
```
<details>
<summary>-THE HARD WAY of deploying -</summary>



## Starting the bot.

Once you've setup your database and your configuration (see below) is complete, simply run:

`python3 -m tg_bot`


## Setting up the bot (Read this before trying to use!):
Please make sure to use python3.6, as I cannot guarantee everything will work as expected on older python versions!
This is because markdown parsing is done by iterating through a dict, which are ordered by default in 3.6.

### Configuration

There are two possible ways of configuring your bot: a config.py file, or ENV variables.

The prefered version is to use a `config.py` file, as it makes it easier to see all your settings grouped together.
This file should be placed in your `tg_bot` folder, alongside the `__main__.py` file . 
This is where your bot token will be loaded from, as well as your database URI (if you're using a database), and most of 
your other settings.

It is recommended to import sample_config and extend the Config class, as this will ensure your config contains all 
defaults set in the sample_config, hence making it easier to upgrade.

An example `config.py` file could be:
```
from tg_bot.sample_config import Config


class Development(Config):
    OWNER_ID = 254318997  # my telegram ID
    OWNER_USERNAME = "SonOfLars"  # my telegram username
    API_KEY = "your bot api key"  # my api key, as provided by the botfather
    SQLALCHEMY_DATABASE_URI = 'postgresql://username:password@localhost:5432/database'  # sample db credentials
    MESSAGE_DUMP = '-1234567890' # some group chat that your bot is a member of
    USE_MESSAGE_DUMP = True
    SUDO_USERS = [18673980, 83489514]  # List of id's for users which have sudo access to the bot.
    LOAD = []
    NO_LOAD = ['translation']
```

If you can't have a config.py file (EG on heroku), it is also possible to use environment variables.
The following env variables are supported:
 - `ENV`: Setting this to ANYTHING will enable env variables

 - `TOKEN`: Your bot token, as a string.
 - `OWNER_ID`: An integer of consisting of your owner ID
 - `OWNER_USERNAME`: Your username

 - `DATABASE_URL`: Your database URL
 - `MESSAGE_DUMP`: optional: a chat where your replied saved messages are stored, to stop people deleting their old 
 - `LOAD`: Space separated list of modules you would like to load
 - `NO_LOAD`: Space separated list of modules you would like NOT to load
 - `WEBHOOK`: Setting this to ANYTHING will enable webhooks when in env mode
 messages
 - `URL`: The URL your webhook should connect to (only needed for webhook mode)

 - `SUDO_USERS`: A space separated list of user_ids which should be considered sudo users
 - `SUPPORT_USERS`: A space separated list of user_ids which should be considered support users (can gban/ungban,
 nothing else)
 - `WHITELIST_USERS`: A space separated list of user_ids which should be considered whitelisted - they can't be banned.
 - `DONATION_LINK`: Optional: link where you would like to receive donations.
 - `CERT_PATH`: Path to your webhook certificate
 - `PORT`: Port to use for your webhooks
 - `DEL_CMDS`: Whether to delete commands from users which don't have rights to use that command
 - `STRICT_GBAN`: Enforce gbans across new groups as well as old groups. When a gbanned user talks, he will be banned.
 - `WORKERS`: Number of threads to use. 8 is the recommended (and default) amount, but your experience may vary.
 __Note__ that going crazy with more threads wont necessarily speed up your bot, given the large amount of sql data 
 accesses, and the way python asynchronous calls work.
 - `BAN_STICKER`: Which sticker to use when banning people.
 - `ALLOW_EXCL`: Whether to allow using exclamation marks ! for commands as well as /.

### Python dependencies

Install the necessary python dependencies by moving to the project directory and running:

`pip3 install -r requirements.txt`.

This will install all necessary python packages.

### Database

If you wish to use a database-dependent module (eg: locks, notes, userinfo, users, filters, welcomes),
you'll need to have a database installed on your system. I use postgres, so I recommend using it for optimal compatibility.

In the case of postgres, this is how you would set up a the database on a debian/ubuntu system. Other distributions may vary.

- install postgresql:

`sudo apt-get update && sudo apt-get install postgresql`

- change to the postgres user:

`sudo su - postgres`

- create a new database user (change YOUR_USER appropriately):

`createuser -P -s -e YOUR_USER`

This will be followed by you needing to input your password.

- create a new database table:

`createdb -O YOUR_USER YOUR_DB_NAME`

Change YOUR_USER and YOUR_DB_NAME appropriately.

- finally:

`psql YOUR_DB_NAME -h YOUR_HOST YOUR_USER`

This will allow you to connect to your database via your terminal.
By default, YOUR_HOST should be 0.0.0.0:5432.

You should now be able to build your database URI. This will be:

`sqldbtype://username:pw@hostname:port/db_name`

Replace sqldbtype with whichever db youre using (eg postgres, mysql, sqllite, etc)
repeat for your username, password, hostname (localhost?), port (5432?), and db name.

## Modules
### Setting load order.

The module load order can be changed via the `LOAD` and `NO_LOAD` configuration settings.
These should both represent lists.

If `LOAD` is an empty list, all modules in `modules/` will be selected for loading by default.

If `NO_LOAD` is not present, or is an empty list, all modules selected for loading will be loaded.

If a module is in both `LOAD` and `NO_LOAD`, the module will not be loaded - `NO_LOAD` takes priority.

### Creating your own modules.

Creating a module has been simplified as much as possible - but do not hesitate to suggest further simplification.

All that is needed is that your .py file be in the modules folder.

To add commands, make sure to import the dispatcher via

`from tg_bot import dispatcher`.

You can then add commands using the usual

`dispatcher.add_handler()`.

Assigning the `__help__` variable to a string describing this modules' available
commands will allow the bot to load it and add the documentation for
your module to the `/help` command. Setting the `__mod_name__` variable will also allow you to use a nicer, user
friendly name for a module.

The `__migrate__()` function is used for migrating chats - when a chat is upgraded to a supergroup, the ID changes, so 
it is necessary to migrate it in the db.

The `__stats__()` function is for retrieving module statistics, eg number of users, number of chats. This is accessed 
through the `/stats` command, which is only available to the bot owner.
</details>
