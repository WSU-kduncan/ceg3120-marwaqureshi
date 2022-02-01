Setup:

- How to get an API token
When you go to discord's developer portal, then navigate to the applications and select your class application that you are currently in. Select Bot under the settings menu on the left, and under 'Build-A-Bot' you can see the 'TOKEN'. Clickit and reveal the API token.

- Where to put it to work with the code
The API token helps your Bot connect to Discord using the token. An easy way to do it is through creating .env file and performing the code " DISCORD_TOKEN={your-bot-token} " in it to make sure the token is stored in a safe place.

- Dependencies (what packages need to be installed to run the code)
We need to remind ourselves that we are using python version 3 to begin with. Also, a python library calle discord.py will be used, including Async.IO. The package that we need is pip. We also need a library called dotenv which loads the environment variables from a env file into shell environment variable.  

Usage:

- With your changes to the code in place, describe what commands you can type in your Discord server
When using the Discord server, one can write the message to be towel! and the random picks of hitchhiker quotes will generate a quote.

- What response this will provide (from your bot)
The response that the bot will provide will be a quote from the hitchhikers quotes at a random. 

Research:

- You may have realized that it is lame that it only runs when you run the program.
Yes I have realized that the bot does not respond when the program is not running. Visually, you can witness that the bot appears to be offline when the program is not running. As soon as the user runs the program, then bot comes online andyou are able to work with the bot and receive replies.

- In the real world, things are "always on", not waiting for Bob to turn his PC on and make sure the program is running.Yes that is correct! In the real world when we say Good Morning to someone, we do not have to run their program and thenwait for a reply. As it is seen, when we greet someone we receive an instant reply back, unless the person ignores us. In this case, the bot is designed to reply whenever the program is running. 

- Research some possible solutions that would solve this, and discuss why you think it would work.
The solution to this issue is Cloud. Having a remote computer that runs 24/7 would be a great option in the pool of solutions perhaps. Heroku is a free remote cloud hosting service which is also free and can help our bot stay running. Atleast you can start there for sure. (https://stackoverflow.com/questions/64388307/how-to-make-your-discord-bot-always-active).



