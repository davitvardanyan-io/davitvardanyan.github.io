---
title: "How to Effectively Communicate with AI"
draft: false
categories: ["AI"]
description: "Three mechanical things you should understand to get better results from any AI model."
---

I've been noticing that many engineers struggle to get consistent results from AI tools. To work with any AI better, I've found there are three "mechanical" things you should understand. These will help you get better results from any cloud LLM or local model you run.

### 1. The "Token" Budget (Why AI gets "Dumb" in long chats)

Think of Tokens as the "currency" of an AI's attention. Most models don't read word-by-word; they read in chunks of about 4 characters.

- **The Limit:** Every AI has a "Context Window" (a maximum token count).
- **The "Memory" Trick:** As your conversation gets very long, the AI has to "forget" the beginning of the chat to make room for your new messages.

**Pro-Tip:** If you have been chatting for a long time and the AI starts making mistakes or forgetting your instructions, **start a fresh chat**. This clears the "clutter" and gives the AI its full processing power back.

### 2. The "Next Word" Engine (Predictive Nature)

Since the AI is always just predicting the "statistically likely" next word, it is very susceptible to **Leading Questions**.

- **Bad Way:** "This code is efficient, right?" (The AI will likely say "Yes" because you suggested it).
- **Better Way:** "Evaluate the efficiency of this code and suggest three improvements."

**Pro-Tip:** Treat the AI like a very talented intern who wants to please you. If you give it a "hint" of what you want to hear, it might lie (hallucinate) just to make you happy. Always ask for objective analysis.

### 3. Temperature: The "Creative vs. Boring" Dial

Most AI interfaces have a hidden setting called **Temperature**. It controls how "random" the word choice is.

- **Low Temperature (0.1 - 0.3):** The AI picks only the most likely words. Good for coding, math, and facts.
- **High Temperature (0.7 - 1.0):** The AI takes risks and picks less likely words. Good for brainstorming, writing stories, or creative naming.

**Pro-Tip:** If an AI is being too "repetitive" or "boring," tell it: *"Be more creative and use uncommon analogies."* This effectively forces it to act like the temperature is higher.

---

### How to Write a "Perfect" Prompt: The R-I-S-E Formula

Based on how AI "works" inside that "ZIP file," the best prompts follow the **R-I-S-E** formula:

| Element | Description | Example |
| :--- | :--- | :--- |
| **Role** | Give the AI a persona. | "Act as a Senior QA Automation Engineer." |
| **Input** | Give it the raw data. | "Here is a flaky Playwright test script..." |
| **Steps** | Tell it how to think. | "First, identify the wait strategy, then suggest a fix." |
| **Expectation** | Define the output format. | "Give me the answer in a code block with comments." |

---

### One Secret Advantage: "Chain of Thought"

Because the AI predicts word-by-word, if you ask it a hard question immediately, it might "trip" over its own logic.

**The Hack:** Always add the phrase **"Let's think step-by-step"** at the end of a hard request.

**Why it works:** This forces the AI to write out its logic *before* it gives the final answer. Since its "future" words are based on its "past" words, the act of writing the logic actually makes the final answer more accurate.

### Key Insights

To get the best results from cloud AI models, remember to manage the token budget by resetting chats, ask objective questions to avoid predictive bias, and use the R-I-S-E formula to ensure the model has the exact context it needs.
