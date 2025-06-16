# 1. Clone the GitHub repo (you must have created it already)
git clone https://github.com/safwan010/my-first-project-github.git
cd my-first-project-github

# 2. Create the Python project file
echo "import random

def guess_number():
    number = random.randint(1, 10)
    attempts = 0

    print(\"🎯 Guess a number between 1 and 10\")

    while True:
        try:
            guess = int(input(\"Enter your guess: \"))
            attempts += 1

            if guess == number:
                print(f\"✅ Correct! You guessed it in {attempts} tries.\")
                break
            elif guess < number:
                print(\"Too low! Try again.\")
            else:
                print(\"Too high! Try again.\")
        except ValueError:
            print(\"❌ Please enter a valid number.\")

if __name__ == \"__main__\":
    guess_number()" > guess_number.py

# Commit #1: Add project file
git add guess_number.py
git commit -m "Added guess_number.py game script"

# 3. Create README.md
echo "# 🎮 Number Guessing Game (Python)

This is a simple command-line **number guessing game** written in Python.  
The program randomly selects a number between 1 and 10, and the user tries to guess it.

---

## 🚀 How to Run

\`\`\`bash
python guess_number.py
\`\`\`

---

## 🛠️ Features

- Random number generation
- User input validation
- Try counter
- Simple game loop

---

## 📁 Project Structure

- guess_number.py
- README.md
- .gitignore

---

## 🧠 Skills Demonstrated

- Python basics
- Loops & conditionals
- Exception handling
- Random module
" > README.md

# Commit #2: Add README.md
git add README.md
git commit -m "Added README with project description"

# 4. Create .gitignore
echo "__pycache__/
*.pyc
*.log
venv/
" > .gitignore

# Commit #3: Add .gitignore
git add .gitignore
git commit -m "Added .gitignore to ignore Python-related files"

# 5. Push all commits to GitHub
git push origin main
