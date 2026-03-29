---
title: "Beyond the Setup: Run-Time Prompt Engineering for Custom Agents"
draft: false
categories: ["AI"]
description: "Four tactical strategies for driving complex AI agents and maximizing their efficiency during an active session."
---

In my last post, I wrote about the fundamental importance of building an AI-ready ecosystem *before* you even start working: setting up project context, broad instructions, JSON schemas for skills, and MCP connections. 

However, I started thinking: once you've built that perfect environment (just like a customized `package.json` for a new project), how do you actually drive the vehicle? Having the best setup isn't enough if you don't effectively steer the model during your actual session. To get the best results, you need to use run-time "prompt engineering" to construct a temporary, custom agent tailored for the specific problem you are solving right now.

Here are four strategies I use during an active chat to optimize a model's execution and turn a generic conversation into a powerful, custom workflow.

### 1. Defining Agent Personas

Setting a very specific role at the exact start of a conversation instantly narrows down the AI's vocabulary, assumptions, and coding style. 

Instead of just saying "write a test," try something like: *"You are a Principal Software Engineer (SDET) who strictly follows DRY principles and focuses on deterministic wait states."* This acts as an instant architectural filter. It aligns the model to match a senior-level engineer's mindset, ensuring its approach to the problem is rigorous before code generation even begins.

### 2. "Few-Shot" Prompting (Concrete Examples)

While having general rules for "good vs. bad" approaches is excellent for your baseline infrastructure, human language in a direct prompt is still inherently ambiguous. 

Providing the AI with two or three complete, perfect examples of past work (like a previously merged pull request or an exact, working automation test from another file) gives it a direct, mathematical template to mimic. In my experience, explicitly showing concrete examples in the chat is the absolute best way to enforce repository style standards and avoid misunderstandings on complex code structures.

### 3. "Chain of Thought" (Thinking Before Acting)

Instead of asking the AI to immediately output a chunk of code, explicitly ask it to *"think step-by-step"* or write out an implementation plan first. 

When an AI is forced to map out its logic and architecture in a scratchpad before touching the final code, it drastically reduces logic errors and wild hallucinations. It is conceptually identical to forcing a developer to write a technical design document before opening a PR. Give the AI space to plan, and its code will be significantly better.

### 4. Feedback Loops and Self-Correction

Don't expect the AI to get complex tasks perfectly right on the very first try. The real magic happens when you treat the AI like a genuine pair programmer. 

If a test fails or a script crashes, simply take the raw terminal error log and feed it right back to the AI. You can say: *"Here is the error from your code. Analyze it, explain why it failed, and fix the issue."* Letting the AI debug its own work and iterate on raw feedback is almost always faster and more effective than a human trying to craft a flawless initial prompt to foresee every edge case.

### Key Insights

Your repository's infrastructure (RAG context, skills, and base rules) builds the perfect **environment** for your AI. But it is these active, run-time tactics, Persona design, Few-Shot examples, Chain of Thought, and Feedback loops, that optimize the AI's **execution**. 

Whenever you sit down for a complex engineering session, remember that combining a strong foundational environment with real-time prompt steering is how you create the ultimate custom agent workflow.
