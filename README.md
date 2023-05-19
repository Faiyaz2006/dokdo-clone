<div align="center">
    <img src="assets/dokdo.png">
    <br/>
</div>

## About

This is a clone of [wonderlandpark/dokdo](https://github.com/wonderlandpark/dokdo)

Dokdo. Easy Discord bot debuging tool.

It's debugging tool for `discord.js` projects.

## Preview

![sh](assets/dokdo.gif)

### Stable

```sh
npm i Cyzer7007/dokdo-clone#main
```

## Features

### Shell command on stdout update

![shell](assets/dokdo.gif)

### Easy shard broadcastEval manager

![shard](assets/shard.png)

## Example usage

```js
const Discord = require('discord.js')
const client = new Discord.Client({ intents: ['GUILDS', 'GUILD_MESSAGES'] })

const Dokdo = require('dokdo')

const DokdoHandler = new Dokdo(client{ owners: ["1234", "1234"] ) // If owner is not specified then it will use Bot Application ownerID as default for owner option.

client.on('messageCreate', async message => {
  if (message.content === 'ping') return message.channel.send('Pong') // handle commands first
  DokdoHandler.run(message) // try !dokdo
})

client.login('super secret token')
```