<div align="center">
  <h1>📜 Coolscript Language Guide</h1>
  <p><i>A lightweight, dynamic scripting language designed for simplicity and power.</i></p>
  
  ![Version](https://img.shields.io/badge/version-1.0.0.0-blue.svg)
  ![Platform](https://img.shields.io/badge/platform-Windows-lightgrey.svg)
  ![License](https://img.shields.io/badge/license-MPL%202.0-orange.svg)
</div>

---

## 📖 Table of Contents
- [1. Variables](#1-variables)
- [2. Input & Output](#2-input--output)
- [3. Math & Random Numbers](#3-math--random-numbers)
- [4. File Operations](#4-file-operations)
- [5. System Commands](#5-system-commands)
- [6. Comments](#6-comments)
- [7. Full Example: Greeting App](#7-full-example-greeting-app)
- [🚀 How to Run](#-how-to-run)

---

## 1. Variables
Variables in Coolscript are dynamically typed. You don't need to specify whether it's a string or a number — the engine handles it for you.

```coolscript
// Strings
LOCAL myName = 'John Doe'
LOCAL greeting = "Hello, World!"

// Numbers
LOCAL age = 25
LOCAL pi = 3.14

// The result of a function
LOCAL luckyNumber = MATH.RANDOM(1, 100)
```

💡 **Tip:** Use `+` to concatenate strings and variables together.

```coolscript
LOCAL fullGreeting = 'Hello, ' + myName + '!'
```

---

## 2. Input & Output
Interact with the user through the console window.

### 🖨️ Printing to Console
```coolscript
OUTPUT.PRINT('Hello, World!')
OUTPUT.PRINT('Your lucky number is: ' + luckyNumber)
```

### ⌨️ Reading User Input
```coolscript
OUTPUT.PRINT('What is your favorite color?')
LOCAL favoriteColor = OUTPUT.READLINE()
OUTPUT.PRINT('Wow, ' + favoriteColor + ' is a great color!')
```

### 🎮 Console Control

| Command | Description |
| :--- | :--- |
| `OUTPUT.CLEAR()` | Clears the entire console screen. |
| `OUTPUT.PAUSE()` | Pauses the script until the user presses any key. |

---

## 3. Math & Random Numbers
Coolscript provides basic math capabilities and a built-in random number generator.

```coolscript
// Generate a random number between 1 and 10 (inclusive)
LOCAL diceRoll = MATH.RANDOM(1, 10)

// Generate a random number between 1 and 100
LOCAL percent = MATH.RANDOM(1, 100)

OUTPUT.PRINT('You rolled a ' + diceRoll)
```

---

## 4. File Operations
Coolscript can create, read, modify, and delete text files in the same directory as the executable.

| Command | Description |
| :--- | :--- |
| `FILE.WRITE(filename, text)` | Creates a new file or overwrites an existing one. |
| `FILE.APPEND(filename, text)` | Adds text to the end of a file without erasing it. |
| `FILE.READ(filename)` | Reads the entire file into a variable. |
| `FILE.DELETE(filename)` | Permanently deletes the specified file. |

### 📝 Example: Writing and Reading
```coolscript
// Write data
FILE.WRITE('data.txt', 'Hello, file!')

// Append more data
FILE.APPEND('data.txt', '\nThis is the second line.')

// Read the file back
LOCAL content = FILE.READ('data.txt')
OUTPUT.PRINT(content)

// Clean up
FILE.DELETE('data.txt')
```

---

## 5. System Commands
Run external programs or system commands directly from your script.

```coolscript
// Open Notepad
SYSTEM.RUN('notepad.exe')

// Run a system command (e.g., list files in a directory)
SYSTEM.RUN('dir')
```

⚠️ **Warning:** `SYSTEM.RUN` executes commands silently. Be careful not to run harmful commands!

---

## 6. Comments
Keep your code readable with comments. The Coolscript engine ignores anything after `//`.

```coolscript
// This is a single-line comment
LOCAL x = 10 // This is an inline comment
```

---

## 7. Full Example: Greeting App
Here is a complete, working example of a small console application that asks for your name, saves it to a file, and greets you.

```coolscript
// Clear the screen
OUTPUT.CLEAR()

// Print a beautiful header
OUTPUT.PRINT('===================================')
OUTPUT.PRINT('       WELCOME TO COOLSCRIPT       ')
OUTPUT.PRINT('===================================')

// Ask for the user's name
OUTPUT.PRINT('Please enter your name:')
LOCAL userName = OUTPUT.READLINE()

// Save to a file
FILE.WRITE('user.txt', 'User: ' + userName)

// Greet the user
OUTPUT.PRINT('')
OUTPUT.PRINT('Greetings, ' + userName + '!')
OUTPUT.PRINT('Your name has been saved to user.txt')

// Wait for the user before closing
OUTPUT.PAUSE()
```

---

## 🚀 How to Run
1. Open **Coolscript Studio**.
2. Write your code in the editor.
3. Press **Build** → **Compile and run** to test it instantly.
4. Press **Build** → **Compile and Build to executable** to create a standalone `.exe` file.

---

<div align="center">
  <p>Made with ❤️ by Atpied Studios</p>
  <p><i>(c) Atpied Studios 2026. All rights reserved.</i></p>
</div>
