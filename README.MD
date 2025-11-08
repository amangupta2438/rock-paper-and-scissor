Rock Paper Scissors
A simple command-line implementation of the classic game Rock, Paper, Scissors in C++.
You play against the computer, entering your choice and seeing who wins.

Table of Contents
Description
Features
Getting Started
Prerequisites
Installation
Running the Program
How It Works
Usage Example
Contributing
License
Contact
Description
This project provides a basic console-based version of Rock, Paper, Scissors.
You choose between Rock, Paper or Scissors, the computer picks randomly, and then the result (win/lose/draw) is shown.

Features
Prompt the user for a choice (Rock / Paper / Scissors)
Validate user input (ensuring 1-3 is entered)
Random computer choice seeded from current time
Display both choices and the result
Repeat option: ask the user if they want to play again
Getting Started
Prerequisites
You’ll need a C++ compiler that supports C++11 (or newer) since the code uses static_cast and nullptr/stream features.
On many systems this might mean:

g++ (GNU C++ Compiler)
Or clang++
On Windows: Visual Studio or MinGW or similar
Installation
Clone (or download) this repository.
git clone <your-repo-url>
cd rock-paper-scissors

Compile the code. For example, using g++:

g++ -std=c++11 -o rps main.cpp

(Assuming your source file is main.cpp. Adjust names as needed.)

Running the Program

Once compiled, run the executable:

./rps

Or on Windows:

rps.exe

Follow the on-screen prompts: you’ll see a menu, choose your option (1=Rock, 2=Paper, 3=Scissors), and play. At the end, you’ll be asked whether you want to play again.

How It Works

The program seeds the random number generator with the current time (srand(time(0));).

It displays a menu and reads the user’s choice.

Input is validated using cin.fail() and bounds checking (1–3).

The computer’s choice is generated via rand() % 3 + 1.

Choices are matched to strings ("Rock", "Paper", "Scissors") for display.

The outcome is determined by comparing user choice and computer choice:

If equal → draw.

If “user wins” conditions (Rock beats Scissors, Paper beats Rock, Scissors beats Paper) → user wins.

Otherwise → computer wins.

The user is then asked whether they’d like to play again (entering y or Y continues the loop).

Usage Example
 ROCK PAPER SCISSORS
=============================

Rock
Paper
Scissors Enter your choice (1-3): 2
You chose: Paper Computer chose: Rock

🎉 You win!

Do you want to play again? (y/n): n

Thanks for playing! 👋

Contributing
