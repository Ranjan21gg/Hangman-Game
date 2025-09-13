# 🎯 Hangman Game (Python)
# https://www.programiz.com/online-compiler/0etHSRrXQ8e1E

A fun *text-based Hangman game* built with Python.  
You guess a randomly chosen word one letter at a time, with a limit of *6 wrong guesses*.

---

## 📌 Features
- ✅ Predefined list of 5 words (python, hangman, game, random, string)
- ✅ Randomly selects a word each time you play
- ✅ Tracks guessed letters and shows your progress
- ✅ Validates input (only single alphabet letters allowed)
- ✅ Maximum of 6 incorrect guesses before you lose
- ✅ Clear win/lose messages

---

## 🛠 Requirements
- Python 3.x  
(No external libraries are required — just the built-in random module)

---

## ▶ How to Play
1. Copy the code into a file named hangman.py.
2. Open your terminal or command prompt.
3. Run the game:
   ```bash
   python Hangman.py


#Logic Diagram
┌───────────────┐
        │ Start Game    │
        └───────┬───────┘
                │
        ┌───────▼───────┐
        │ Pick Random   │
        │ Word          │
        └───────┬───────┘
                │
        ┌───────▼───────┐
        │ Initialize     │
        │ Attempts = 6   │
        │ Display = ___  │
        └───────┬───────┘
                │
        ┌───────▼───────┐
        │ Show Current   │
        │ Word + Attempts│
        └───────┬───────┘
                │
        ┌───────▼──────────┐
        │ Take User Guess   │
        └───────┬──────────┘
                │
        ┌───────▼──────────┐
   ┌───►│ Already Guessed? │───┐
   │    └───────┬──────────┘   │
   │            │Yes           │
   │            ▼              │
   │    (Ask for new letter)   │
   │                           │
   │            No             │
   │            │              │
   │    ┌───────▼──────────┐   │
   │    │ Letter in Word?  │   │
   │    └───────┬──────────┘   │
   │            │              │
   │    Yes     │ No           │
   │            │              │
   │    ┌───────▼───────┐      │
   │    │ Reveal Letter │      │
   │    └───────┬───────┘      │
   │            │              │
   │    ┌───────▼───────┐      │
   │    │ All Letters   │──────┘
   │    │ Guessed?      │
   │    └───────┬───────┘
   │            │Yes
   │            ▼
   │   🎉 YOU WIN!
   │
   │ No
   │
   └───► Decrease Attempts ──► Attempts == 0?
                         │
                         │Yes
                         ▼
                 💀 YOU LOSE!
