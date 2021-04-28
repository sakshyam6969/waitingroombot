## Discord-Waitingroom-Bot

[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](https://discord.gg/bV9Up6BsPV)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/sakshyam6969/)
[![Ask Me Anything !](https://img.shields.io/badge/Ask%20me-anything-1abc9c.svg)](https://discord.gg/bV9Up6BsPV)
[![Support Server](https://img.shields.io/discord/591914197219016707.svg?label=&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)](https://discord.gg/bV9Up6BsPV)

A basic, easy to setup Waiting Room Bot to play an audiofile on your pc / a stream!

## [**DISCORD SUPPORT SERVER INVITE**](https://discord.gg/bV9Up6BsPV)

## Installation | How to use the Bot

 **1.** Install [node.js v12](https://nodejs.org/api/cli.html#cli_unhandled_rejections_mode) or higher

 **2.** Install [ffmpeg@latest](https://ffmpeg.org) 

 **3.** Download this repo and unzip it    |    or git clone it
 
 **4.** Install all of the packages with **`npm install`**     |  the packages are   **`npm install node.js discord.js @discordjs/opus`**
 
 **5.** start the bot with **`node index.js`**

## Usage - config.json

```javascript
{
  "token": "",        // Fill in your Bot token
  "voicechannel": "", // Voice Channel Id for your Bot Channel
  "guildid": ""       // Guild Id of your Server
}
```

## Usage - index.js  | function radioexecute()  | Line 26-34

```javascript
async function radioexecuteadmin() {
    const voiceChannel = client.guilds.cache.get(config.guildid).channels.cache.get(config.voicechannel); //define the Voice Channel
    await voiceChannel.leave(); // leave the channel
    await delay(300); // wait 300ms to provent a bug
    var connection = await voiceChannel.join();//join the channel and
    await connection.voice.setSelfDeaf(true); await connection.voice.setDeaf(true); //selfdeaf
    const dispatcher = connection.play('./audiofile.mp3'); //You can replace the './audifile.mp3' with any sort of Radio stream for example: 'https://streams.ilovemusic.de/iloveradio17.mp3'
    dispatcher.on("end", end => { radioexecuteadmin() });
}
```

## **NOTE:**

*Make sure that you have install [FFmpeg](https://ffmpeg.org), and added it to Systemenvironment variables (PATH)*

*If you are having errors/problems with starting delete the package.json file and do, before you install the packages `npm init`*

# SUPPORT ME AND MILRATO DEVELOPMENT

You can always Support me by inviting one of my **own Discord Bots**

[![SkyNet](https://cdn.discordapp.com/attachments/836669920800407603/836834189075677204/9dpokHUo.png)](https://discord.com/api/oauth2/authorize?client_id=831566323422330940&permissions=8&scope=bot)
[![Musicium Music Bot](https://cdn.discordapp.com/attachments/742446682381221938/770055673965707264/test1.png)](https://discord.com/api/oauth2/authorize?client_id=831902633388146759&permissions=8&scope=bot)
[![Milrato Multi Bot](https://cdn.discordapp.com/attachments/742446682381221938/770056826724679680/test1.png)](https://discord.com/api/oauth2/authorize?client_id=836823990907043840&permissions=8&scope=bot)


**Discord Server:**
[https://discord.gg/GgjJZCyYKD](https://discord.gg/GgjJZCyYKD)

**Discord Server:**
[https://discord.com/invite/4dGuGXK4A4](https://discord.com/invite/4dGuGXK4A4)

**Website:**
[mc-host24.de](https://mc-host24.de/user/affiliate/3121])
