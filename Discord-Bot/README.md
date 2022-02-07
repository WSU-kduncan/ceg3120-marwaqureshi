Setup:

- How to get an API token
When you go to discord's developer portal after signing in, then navigate to the applications and select your class application that you are currently in. Select Bot under the settings menu on the left, and under 'Build-A-Bot' you can see the 'TOKEN'. Clickit and reveal the API token. The oAuth should be in the same .env file inside same directory as source code work. You can check this by doing la command.

- Where to put it to work with the code
The API token helps your Bot connect to Discord using the token. An easy way to do it is through creating .env file and performing the code " DISCORD_TOKEN={your-bot-token} " in it to make sure the token is stored in a safe place. Like I mentioned before, the .enc has to be stored with the source code. Check with la command. Also, if there are any errors relating to traceback error, you can create a new .env to see there is a problem with the .env and replace new token with old token. This is just so that you can see how important the .env file is.

- Dependencies (what packages need to be installed to run the code)
We need to remind ourselves that we are using python version 3 to begin with. Also, a python library calle discord.py will be used, including Async.IO. The package that we need is pip. We also need a library called dotenv which loads the environment variables from a env file into shell environment variable. make sure to install using commands such as, sudo apt install python 3, sudo apt install python3-pip, pip install -U discord.py, pip install -U python-dotenv.

Usage:

- With your changes to the code in place, describe what commands you can type in your Discord server
When using the Discord server, one can write the message to be towel! and the random picks of hitchhiker quotes will generate a quote. However, when you check my modified code, you can see that you can type 'Hi' and the code will pick at random 1 out of the 4 options. Also, if the user types 'Bye', the bot will respond with 1 out of the 3 random quotes that we have put options for.

- What response this will provide (from your bot)
The response that the bot will provide will be a quote from the hello_quote and bye_quote at a random. So if the user says 'Hi', the bot will respond with 'Heyyy, I am the famous bot that you have been looking for!', 'whatsuppppp', 'Hi, How are you?', 'Peek A Boo. Hi!'. However, when user types 'Bye', the bot responds with 'Good Bye' , 'See You Later' , 'Aww I will miss you' .

Research:

- You may have realized that it is lame that it only runs when you run the program.
Yes I have realized that the bot does not respond when the program is not running. Visually, you can witness that the bot appears to be offline when the program is not running. As soon as the user runs the program, then bot comes online andyou are able to work with the bot and receive replies.

- In the real world, things are "always on", not waiting for Bob to turn his PC on and make sure the program is running.Yes that is correct! In the real world when we say Good Morning to someone, we do not have to run their program and thenwait for a reply. As it is seen, when we greet someone we receive an instant reply back, unless the person ignores us. In this case, the bot is designed to reply whenever the program is running. 

- Research some possible solutions that would solve this, and discuss why you think it would work.
The solution to this issue is Cloud. Having a remote computer that runs 24/7 would be a great option in the pool of solutions perhaps. Heroku is a free remote cloud hosting service which is also free and can help our bot stay running. Atleast you can start there for sure. (https://stackoverflow.com/questions/64388307/how-to-make-your-discord-bot-always-active).



