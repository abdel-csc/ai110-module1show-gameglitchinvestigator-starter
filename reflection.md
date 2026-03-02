# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
It honestly looked pretty bland. The UI was basic but I imagine all of these projects possess a basic UI because the integral part is the issues to be found. What was weird to me were how the logic was backwards. For instance a bug that I found out was that if you reached a high threshold you would be prompted to go higher. Which honestly was kind of a funny one. 
- List at least two concrete bugs you noticed at the start  
  (for example: "the secret number kept changing" or "the hints were backwards").
  The two concrete bugs would be the one I previously mentioned which is the "backwards" bug but another one would be the range of numbers of difficult, with the normal being higher the "hard". It was just pretty inconsistent overall. 

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
I used the copilot chat feature built into VSCODE for this project, and also asked GPT for some verification on whether or not the issues I were finding were bugs in the overall context. 
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
One AI suggestion that I added was the import in app.py that would successfully allow the logic to workalongside the main code. It was a small but integral part of the project.
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).
There was one AI suggestion when asking to merge both of these files, and I knew it was "wrong" from the get-go because it changed so much in my app.py. The reason why I put "wrong" in quotes is because it was not necessarily incorrect like it would still run but it was just so much unecessary jargon that signalled that I needed to be more specific.

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
I would be the tester to decide if things were really working. I also used Ai to cross check and analyze if that particular bug I focused on to be fixed, was well, fixed!
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
  I ran 3 tests for too_low, too_high, and winning_guess. It showed me what was failing (assertions) among the ranges and prompted me to fix them to move forward. After re-running them, it would show me that the 3 tests would pass due to the modifications I made to the hint logic. 
- Did AI help you design or understand any tests? How?
Yes, AI is best as a supplement of verification after human input. When these tests had failed, it had suggested the aforementioned solutions and shortly after they worked in my favor.

---

## 4. What did you learn about Streamlit and state?

- In your own words, explain why the secret number kept changing in the original app.
When the code is ran in the app, everythings is read essentially all over again from top to bottom. So the randomization of random.randint kept generating a new number everytime as a result.
- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
I like to think of streamlit reruns like a person with amensia. They forget the codeentirely everytime the button is pressed, but when you provide a session state, it's basically like that aforementioned person writing on a notepad who they are so they don't forget.
- What change did you make that finally gave the game a stable secret number?
The code that allowed for a fix was "if "secret" not in st.session_state" as it allowed for the secret code to be generated only once, not at everytime its reran. 

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects? This could be a testing habit, a prompting strategy, or a way you used Git.
Being more specific is a must. I honestly have to say Jason stressed that last lecture about prompting and it stuck to me. Not to say I'm the best at it now, but I at least now what to do moving forward. 
- What is one thing you would do differently next time you work with AI on a coding task?
As I said before I would be more specific. Not being specific almost cost the AI to rewrite everything from scratch, which is a big no-go in my book. Again it may run, but it's not what we're looking for. 
- In one or two sentences, describe how this project changed the way you think about AI generated code.
I often hear nowadays that AI generated projects are known as AI-slop or just have issues altogether. But this shows me that AI can not only build projects such as these, and also help debug said projects so they're fully functional and ready to be pushed! 
