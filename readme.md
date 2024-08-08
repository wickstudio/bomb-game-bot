# Bomb Game Discord Bot

This is a Discord bot for a bomb game, where players can join and answer questions to survive. The bot is built using `discord.js` and features dynamic game management, including player join/leave handling, question asking, and image generation.

## Features

- **Join and Leave Game**: Players can join or leave the game using buttons.
- **Randomized Questions**: The bot asks randomized questions from a predefined list, and players must answer correctly to survive.
- **Dynamic Image Generation**: The bot generates an image with the question and the player's name.
- **Player Health Management**: Players have hearts (lives), and they lose a heart for incorrect answers or timeouts.
- **Automatic Game Management**: The game automatically starts when enough players join and stops when there's a winner.

## Requirements

- Node.js v16.x or higher
- Discord.js v14.x
- Canvas v2.x

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/wickstudio/bomb-game-bot.git
   cd bomb-game-bot
   ```

2. **Install the dependencies**:
   ```bash
   npm install
   ```

3. **Configuration**:
   - Create a `config.json` file in the root directory and add your bot's token and the role ID that has permission to start/stop the game.
   - Example:
     ```json
     {
       "token": "YOUR_BOT_TOKEN",
       "roleId": "YOUR_ROLE_ID"
     }
     ```

   - Add your quiz questions in `quiz.json` in the format:
     ```json
     [
       {
         "partial": "This is a partial question?",
         "complete": "This is a complete question."
       }
     ]
     ```

4. **Run the bot**:
   ```bash
   node index.js
   ```

## Commands

- **Start Game**: `-بومب` — Starts the bomb game if there isn't an active game.
- **Stop Game**: `-ايقاف` — Stops the current game if there is one active.

## How to Play

1. Use the command `-بومب` to start the game.
2. Players can join or leave the game using the buttons.
3. Once enough players join, the game starts automatically.
4. The bot will ask players questions in a random order. Players must answer correctly to avoid losing hearts.
5. The game continues until only one player is left.

## Handling Errors

The bot is designed to handle common errors gracefully, including incorrect answers and timeouts. If any unexpected issues arise, they are logged, and the bot attempts to continue running smoothly.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request.

## Support

For support, join our [Discord server](https://discord.gg/wicks).