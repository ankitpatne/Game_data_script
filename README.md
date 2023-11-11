
# get_game_data.py - Game Data Extraction and Compilation Script

## Introduction
This Python script automates the process of extracting game data from a specified source directory, organizing it in a new directory, and compiling/running the game code. The script assumes a specific directory structure where games are stored in subdirectories containing the word "game" and each game has a single .go file that needs to be compiled before running.

## Assumptions
- The data directory contains various files and directories.
- Games are stored in directories containing the word "game."
- Each game directory has a single .go file that requires compilation before running.

## Usage
```bash
python get_game_data.py <source_directory> <destination_directory>


### Example
```bash
python get_game_data.py data result
```

## Project Steps/Requirements

1. **Find all game directories from the source directory:**
   - Traverse the source directory to identify all directories containing the word "game."

2. **Create a new /games directory:**
   - Create a new directory named "games" in the specified destination directory.

3. **Copy and rename game directories:**
   - Copy each game directory to the /games directory in the destination.
   - Remove the "game" suffix from the copied directories.

4. **Create a .json file with game information:**
   - Generate a JSON file containing information about each game.
     - Game Name
     - Original Directory
     - Destination Directory

5. **Compile all game code:**
   - For each game directory, compile the single .go file using the `go build` command.
   - Handle any compilation errors and log the results.

6. **Run all game code:**
   - Execute the compiled binaries of each game.
   - Log the results of each game execution.

## Command Line Arguments
- `<source_directory>`: The path to the source directory containing game data.
- `<destination_directory>`: The path to the destination directory where the organized data will be stored.

## Dependencies
- Python 3.x
- The script assumes the presence of the Go compiler for compiling .go files.

## Usage Example
```bash
python get_game_data.py data result
```

## Note
- Ensure that the Go compiler is installed and available in the system's PATH.


This documentation provides an overview of the script, its purpose, usage, and the steps it takes to extract and compile game data. Users can follow the provided instructions to execute the script with the necessary command-line arguments.
