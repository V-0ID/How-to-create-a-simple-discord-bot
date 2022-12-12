# How-to-create-a-simple-discord-bot

> A guide on how to create a simple discord bot. This is a simple introduction to getting your discord bot working, getting advanced commands to work, and connecting databases takes much more effort and experience to consider. Before following this tutorial it is recommended that you have a simple understanding of **JavaScript/Node.JS** and the documentation on the **Discord API**.
https://discord.com/developers/docs/reference
> 
> _**THIS TUTORIAL WILL ONLY INCLUDE WRITING CODE FOR THE BOT NOT SETTING IT UP IN THE DISCORD DEVELOPER PORTAL**_

## Getting Started!

1. Make sure you have Node.js installed on your computer. You can check if you have it installed by running the **`node -v`** command in your terminal. If you don't have Node.js installed, you can download it from the official website. -- https://nodejs.org/en/

2. Create a new project directory and initialize it as a Node.js project by running the **`npm init`** command. This will create a _**package.json**_ file in your project directory, which will be used to store information about your project and its dependencies.

3. install the Discord.js library, which will allow you to interact with the Discord API, by running the following command: **`npm install discord.js`** in your terminal

4. Create a new file called _**index.js**_ in your project directory and add the following code to it:

```JS
const Discord = require('discord.js');
const client = new Discord.Client();

client.on('ready', () => {
  console.log(`Logged in as ${client.user.tag}!`);
});

client.login('your_bot_token');

```

5. Replace **`your_bot_token`** with the token for your bot, which you can get from the Discord developer portal.

6. Start your bot by running the **`node index.js`** command in your terminal.

## Adding Commands
> This part will focus on adding commands to the bot, this will only show you how to add a simple command, to add more function read the discord documentation to add more complex functions in your bot.

1. You can now start creating commands for your bot by using the Discord.js library and the Discord API. For example, you can add the following code to your `index.js` file to create a `!ping` command that responds with **"Pong!"** when the user types **!ping** in a Discord channel:

```JS
client.on('message', msg => {
  if (msg.content === '!ping') {
    msg.reply('Pong!');
  }
});

```

### What Your Code Should Look Like:
```JS
const Discord = require('discord.js');
const client = new Discord.Client();

client.on('ready', () => {
  console.log(`Logged in as ${client.user.tag}!`);
});

client.login('your_bot_token');

client.on('message', msg => {
  if (msg.content === '!ping') {
    msg.reply('Pong!');
  }
});

```
