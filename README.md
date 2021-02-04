# BotDash.pro

**First you will want to go to** https://botdash.pro

Then Go to account **-->** Login 

![Login](https://cdn.discordapp.com/attachments/797611832336580628/806909010053300254/unknown.png)

**When you have logged in go to the dashboard create a New project** 

![NewProject](https://cdn.discordapp.com/attachments/783764518072352809/806909892774461480/unknown.png)

**Go to vscode rep.it glitch.com**
`npm i discord.js`
`npm i botdash.pro` 

Heres a Starter code

```js

const botdash = require('botdash.pro'); //Require botdash.pro
const discord = require('discord.js'); //Require Discord.JS
const client = new discord.Client(); //Create a discord bot client
var dashboard = ""; //Declare variable
client.login("--- DISCORD BOT TOKEN ---"); //Login to the bot client
client.on('ready', () => { //Client is ready
    console.log("ready"); //print messageclient
    dashboard = new botdash.APIclient("--- BOTDASH TOKEN ---"); //Connect to botdash with a discord.js 
});
client.on('message', async function(message) { //Discord message recieved
    const prefix = await dashboard.getVal(message.guild.id, "botprefix"); //Get a value
    if (message.content == `${prefix}ping`) { //Simple ping command with customizable prefix
        message.channel.send('pong'); //Send pong back 
    }
});
```
**How to Get a api token go to actions settings and grab the api token**
![APITOKEN](https://cdn.discordapp.com/attachments/783764518072352809/806911212922601522/unknown.png)

