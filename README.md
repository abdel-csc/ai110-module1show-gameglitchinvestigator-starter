# 🎮 Game Glitch Investigator: The Impossible Guesser

## 🚨 The Situation

You asked an AI to build a simple "Number Guessing Game" using Streamlit.
It wrote the code, ran away, and now the game is unplayable. 

- You can't win.
- The hints lie to you.
- The secret number seems to have commitment issues.

## 🛠️ Setup

1. Install dependencies: `pip install -r requirements.txt`
2. Run the broken app: `python -m streamlit run app.py`

## 🕵️‍♂️ Your Mission

1. **Play the game.** Open the "Developer Debug Info" tab in the app to see the secret number. Try to win.
2. **Find the State Bug.** Why does the secret number change every time you click "Submit"? Ask ChatGPT: *"How do I keep a variable from resetting in Streamlit when I click a button?"*
3. **Fix the Logic.** The hints ("Higher/Lower") are wrong. Fix them.
4. **Refactor & Test.** - Move the logic into `logic_utils.py`.
   - Run `pytest` in your terminal.
   - Keep fixing until all tests pass!

## 📝 Document Your Experience

- [ ] Describe the game's purpose.
This game's purpose is that it's intentionally wonky and out of place with "secret" number creation, and guiding higher or lower guessing hints to encourage us AI engineers to probe properly. 
- [ ] Detail which bugs you found.
I've found that the hints were backwards, the hard mode range was less than the normal one (1-50 vs 1-100) the secret number converted to a string on even attempts breaking comparisons, attempts reset to 0 on the new game but initialized at 1,  the range display always showed 1-100 regardless of the difficulty, and how the scoring was inconsistent. Some of these might be more meticulous than others.
- [ ] Explain what fixes you applied.
Updated to use actual low and high variables, verified by switching difficulties, and I swapped the hints to properly guide users.

## 📸 Demo

- [ ] [Insert a screenshot of your fixed, winning game here]


## 🚀 Stretch Features

- [ ] [If you choose to complete Challenge 4, insert a screenshot of your Enhanced Game UI here]
