# Monkey Type - Terminal Typing Speed Test

A terminal-based typing speed test game written in C using the ncurses library. Test your typing skills with different difficulty levels and track your progress over time.

## Features

- **Multiple Difficulty Levels**: Easy, Medium, and Hard modes with varying word lengths
- **Real-time Feedback**: Color-coded typing with immediate visual feedback
- **Performance Metrics**: Track WPM (Words Per Minute), accuracy, and character statistics
- **History Tracking**: Save and view your typing test results
- **Interactive UI**: Navigate using arrow keys with a clean terminal interface
- **Timed Tests**: 60-second typing challenges
- **Custom Word Pool**: Uses external word file for generating random text

## Prerequisites

- GCC compiler
- ncurses library
- Unix-like operating system (Linux, macOS, WSL)

### Installing ncurses

**Ubuntu/Debian:**
```bash
sudo apt-get install libncurses5-dev libncursesw5-dev
```

**macOS:**
```bash
brew install ncurses
```

**CentOS/RHEL:**
```bash
sudo yum install ncurses-devel
```

## Installation

1. Clone or download the project files
2. Create a word pool file named `word_pool.txt` in the same directory
3. Compile the program:
- Type-Master-1
```bash
gcc -o Type-Master-1/monkey_type Type-Master-1/Monkey_type.c -lncurses
```
- Type-Master-2
```bash
gcc -o Type-Master-2/typing_game Type-Master-2/typing_game.c -lncurses
```
## Setup

### Word Pool File
✅ **Already included**: Your project includes a `word_pool.txt` file with words for the typing tests.

The program will automatically filter words from your file based on difficulty:
- **Easy**: 1-4 characters, 20 words
- **Medium**: 5-7 characters, 40 words  
- **Hard**: 8-20 characters, 60 words

## Usage

1. Run the program:
- Type-Master-1
```bash
./Type-Master-1/monkey_type
```
- Type-Master-2
```bash
./Type-Master-2/typing_game < word_pool.txt
```

2. Navigate the menu using arrow keys and press Enter to select
3. Choose your difficulty level
4. Press Enter to start the typing test
5. Type the displayed text as accurately as possible
6. View your results and optionally save them

### Controls

- **Arrow Keys**: Navigate menu options
- **Enter**: Select option or start test
- **Backspace**: Delete characters during typing
- **Tab**: Restart current test
- **Escape**: Exit current test
- **Any letter/space**: Type characters

## Difficulty Levels

| Level  | Word Length | Word Count | Description |
|--------|-------------|------------|-------------|
| Easy   | 1-4 chars   | 20 words   | Short, common words |
| Medium | 5-7 chars   | 40 words   | Moderate length words |
| Hard   | 8-20 chars  | 60 words   | Long, challenging words |

## Performance Metrics

The program tracks and displays:

- **Time Taken**: Total seconds spent typing
- **Words Per Minute (WPM)**: Typing speed calculation
- **Accuracy**: Percentage of correctly typed characters
- **Correct/Wrong Words**: Word-level accuracy statistics
- **Correct/Wrong Characters**: Character-level statistics
- **Characters Per Second (CPS)**: Raw character typing speed

## File Structure

```
monkey_type/
├── Monkey_type.c      # Main source code
├── word_pool.txt      # Word database (user-created)
├── History.txt        # Automatically generated results file
└── README.md          # This file
```

## Color Coding

During typing tests:
- **Green**: Correctly typed characters
- **Red**: Incorrectly typed characters
- **Blue**: Untyped characters (background)
- **Timer Colors**: 
  - Green: >30 seconds remaining
  - Yellow: 10-30 seconds remaining
  - Red: <10 seconds remaining

## History Feature

Results are automatically saved to `History.txt` with the following format:
```
NAME       TIME      WPM    ACCURACY
John       45s       65.23  94.50
```

Access your typing history through the main menu to track improvement over time.

## Troubleshooting

### Common Issues

**"No file found" error:**
- Ensure `word_pool.txt` exists in the same directory as the executable
- Check file permissions

**Compilation errors:**
- Install ncurses development libraries
- Use the correct compiler flags: `-lncurses`

**Display issues:**
- Ensure terminal supports colors
- Try resizing terminal window for better display

**"No suitable words found" error:**
- Check that `word_pool.txt` contains words matching the difficulty criteria
- Add more words of appropriate lengths to the file

## Contributing

Feel free to contribute improvements:
- Add new difficulty levels
- Implement additional statistics
- Improve the user interface
- Add new features like custom time limits

## License

This project is open source. Feel free to modify and distribute according to your needs.

## Acknowledgments

- Built with ncurses library for terminal UI
- Inspired by online typing test platforms
- Designed for improving typing skills and speed
```

