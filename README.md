# Wordle50

Wordle50 is a clone of the popular game Wordle, implemented in C. The game prompts the user to guess a secret word of a specified length. The user has one more guess than the length of the word. After each guess, the game provides feedback on the guessed word.

## How to Play

1. Run the program with a single command-line argument that specifies the length of the secret word. The length must be between 5 and 8, inclusive.

    ```
    ./wordle 5
    ```

2. The game will prompt you to input a guess. The guess must be a word of the specified length.

    ```
    Input a 5-letter word: games
    ```

3. After each guess, the game will print the guessed word with color-coded feedback:

    - Green: The letter is in the correct position.
    - Yellow: The letter is in the word but not in the correct position.
    - Red: The letter is not in the word.

4. The game continues until you guess the word correctly or you run out of guesses.

## Implementation Details

The game is implemented in the `wordle.c` file. The main function handles the game loop and uses several helper functions:

- `get_guess(int wordsize)`: Prompts the user for a guess of the correct length.
- `check_word(string guess, int wordsize, int status[], string choice)`: Compares the guessed word to the secret word and assigns scores.
- `print_word(string guess, int wordsize, int status[])`: Prints the guessed word with color-coded feedback.

The secret word is selected pseudorandomly from a list of words stored in a text file. The list of words is loaded into an array at the start of the game.

## Note

This version of Wordle does not check if the guessed word is a real word. All guesses should be in lowercase characters.
