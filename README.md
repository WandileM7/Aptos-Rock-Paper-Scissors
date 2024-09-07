# Enhanced Rock Paper Scissors Game on Aptos

This project is an Aptos-based implementation of the classic Rock Paper Scissors game, with additional features for an enhanced gaming experience.

## New Features

### 1. Endless Gameplay
Players can now enjoy multiple rounds of Rock Paper Scissors without needing to redeploy the contract. After each game, players can choose to play again, allowing for extended gameplay sessions.

### 2. Score Tracking
The smart contract now keeps track of the scores for both the player and the computer. This feature adds a competitive element to the game, allowing players to see their performance over multiple rounds.

- Player Score: Tracks the number of games won by the player
- Computer Score: Tracks the number of games won by the computer
- Games Played: Keeps count of the total number of games played

## How to Play

1. Start a new game by calling the `start_game` function.
2. Set your move (Rock: 1, Paper: 2, Scissors: 3) using the `set_player_move` function.
3. Generate the computer's move with `randomly_set_computer_move`.
4. Finalize the game results by calling `finalize_game_results`.
5. View the game outcome and updated scores.
6. To play another round, call `reset_for_new_game` and repeat steps 2-5.

## Smart Contract Functions

- `start_game`: Initializes a new game instance with zero scores.
- `set_player_move`: Sets the player's move for the current round.
- `randomly_set_computer_move`: Generates a random move for the computer.
- `finalize_game_results`: Determines the winner and updates the scores.
- `reset_for_new_game`: Resets the game state for a new round while keeping the scores.
- `get_player_move`, `get_computer_move`, `get_game_results`: View functions to check the current game state.
- `get_player_score`, `get_computer_score`, `get_games_played`: View functions to check the overall scores and number of games played.

## Installation and Setup

1. Clone this repository:
   ```
   git clone https://github.com/WandileM7/enhanced-rock-paper-scissors-aptos.git
   ```
2. Install the Aptos CLI if you haven't already.
3. Compile the Move module:
   ```
   aptos move compile
   ```
4. Deploy the module to the Aptos blockchain:
   ```
   aptos move publish
   ```

## Interacting with the Game

You can interact with the game using the Aptos CLI or by building a frontend application that interfaces with the smart contract.

Example CLI command to start a game:
```
aptos move run --function-id 'default::RockPaperScissors::start_game'
```

## Future Enhancements

I'm constantly looking to improve the game. Some ideas for future enhancements include:
- Implementing a player vs. player mode
- Adding APT token wagering
- Creating a web-based frontend for easier interaction

## Contributing

I welcome contributions to this project! Please feel free to submit issues or pull requests with your ideas and improvements.

