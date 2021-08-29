const {Client, RichEmbed} = require('discord.js');
const bot = new Client();

const token = 'YOUR TOKEN';

const PREFIX = '!';


bot.on('ready', () => {
    console.log('This bot is active!');
})

bot.on('message', message => {
    let args = message.content.substring(PREFIX.length).split(" ");
    

    switch (args[0]) { 
        case 'help':
            const Embed = new RichEmbed()
            .setTitle("Helper Embed")
            .setColor(0xFF0000)
            .setDescription("Make sure to use the !help to get access to the commands");

            message.author.send(Embed);
        break;
    }


});

            
                        
bot.login(token);
