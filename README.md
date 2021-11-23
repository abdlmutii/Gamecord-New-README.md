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

### Table of content
- Games & Examples
  - [2048](#2048)
  - [Snake](#snake)
  - [Tic Tac Toe](#tic-tac-toe)
  - [Rock Paper Scissors](#rockpaperscissors-)
  - [Connect Four](#connectfour-)
  - [Trivia](#trivia-)
  - [Fishy](#fishy-)
  - [Slots](#slots)


### Tic Tac Toe
- **Check supported colors from discord.js guide [here](https://discordjs.guide/interactions/buttons.html#button-styles)**
```js
const { TicTacToe } = require('discord-gamecord')

new TicTacToe({
  message: message,
  slash_command: false,
  opponent: message.mentions.users.first(),
  embed: {
    title: 'Tic Tac Toe',
    overTitle: 'Game Over',
    color: '#5865F2',
  },
  oEmoji: '🔵',
  xEmoji: '❌',
  blankEmoji: '➖',
  oColor: 'PRIMARY',
  xColor: 'DANGER',
  waitMessage: 'Waiting for the opponent...',
  turnMessage: '{emoji} | Its now **{player}** turn!',
  askMessage: 'Hey {opponent}, {challenger} challenged you for a game of Tic Tac Toe!',
  cancelMessage: 'Looks like they refused to have a game of Tic Tac Toe. \:(',
  timeEndMessage: 'Since the opponent didnt answer, i dropped the game!',
  drawMessage: 'It was a draw!',
  winMessage: '{emoji} | **{winner}** won the game!',
  gameEndMessage: 'The game went unfinished :(',
}).startGame();
```
 
### Working with interactions
```js
message: interaction,
slash_command: true,
opponent: interaction.options.getUser('user'),
```

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
```js
message: interaction,
slash_command: true,
```
