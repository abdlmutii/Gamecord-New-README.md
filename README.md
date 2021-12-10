<div align="center">
![cool new image maybe lol](wow link)
</br>
<a href="https://discord.gg/invite/GaczkwfgV9"><img src="https://img.shields.io/discord/800631529351938089?style=for-the-badge&color=5865F2&logo=discord&logoColor=white&label=Aniket" alt="Discord server" /></a>
    <a href="https://www.npmjs.com/package/discord-gamecord"><img src="https://img.shields.io/npm/dt/discord-gamecord.svg?maxAge=3600&color=CC3534&style=for-the-badge&logo=npm" alt="npm downloads" /></a>
</div>

### What is gamecord?
- [**Discord Gamecord**](https://discord.gg/invite/GaczkwfgV9) is a powerful module that allows you to play games within Discord

### How to install gamecord?
```diff
+ npm install discord-gamecord
````

- 🤩 Beginner friendly
- 🎨 Very customizable `messages`, `buttons`, `colors`, `etc..`
- 🎮 Support 11+ games
- 📎 First discord games package support slash commands,
- 🇪🇬 Support for translations, adapt the strings for your own language!

### Examples
- Games
  - [2048](example/2048)
  - [Snake](#snake)
  - [Tic Tac Toe](examples/tic-tac-toe)
  - [Rock Paper Scissors](examples/rockpaperscissors)
  - [Connect Four](examples/connectfour)
  - [Trivia](examples/trivia)
  - [Fishy](examples/fishy)
  - [Slots](examples/slots)

### Docs
- **Gamecord have docs to check and understand all games and package, in [`discord-gamecord.js.org`](https://discord-gamecord.js.org/)**
- **But i'm looking for examples! , Check [`examples`](examples folder link) folder**

### Snake
```js
const { Snake } = require('discord-gamecord')

new Snake({
  message: message,
  slash_command: false,
  embed: {
    title: 'Snake',
    color: '#5865F2',
    OverTitle: 'Game Over',
  },
  snake: { head: '🟢', body: '🟩', tail: '🟢', over: '💀' },
  emojis: {
    board: '⬛', 
    food: '🍎',
    up: '⬆️', 
    right: '➡️',
    down: '⬇️',
    left: '⬅️',
  },
  foods: ['🍎', '🍇', '🍊'],
  stopButton: 'Stop',
  othersMessage: 'You are not allowed to use buttons for this message!',
}).startGame();
```

### Working with interactions 
- **Also known as [`slash commands`](), just change this few things below :**
```js
message: interaction,
slash_command: true,
```

### Looking For Help?
![Server Widget](server widget url)
