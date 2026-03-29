---
title: "How to Get the Best Outputs from AI"
draft: false
categories: ["AI"]
description: "Six essential techniques for getting consistent, tailored results from any AI model."
---

I've been noticing that while AI is very capable and can solve many different problems, there's a recurring issue: every time I ask the same question to the same model (or across different cloud LLMs), I receive completely different results. One day, the output is perfectly aligned with my repository's style; the next day, it generates a generic, unstructured response. 

This made me start wondering: *how can I consistently receive the exact output that I want, or that I would have written myself?*

I started to think about a solution and found several highly useful things that I can add to any AI conversation. By applying these to any chat or prompt, the output matches exactly what I wanted to see. Here is how you can incorporate these pillars in your next project to get better, more reliable results from any AI tool.

### 1. Project Context and RAG

The first essential piece is providing deep project context. If I give the AI more background about what I am building (such as key details, relevant pages, overall architecture, and specific goals), the AI will understand how to work within the project significantly better. 

This naturally leads to **RAG (Retrieval-Augmented Generation)**. In simple terms, RAG is a method where an AI fetches relevant facts, documentation, or codebase snippets from external sources and adds them to its context *before* generating a response. Without context, an AI model is just making educated guesses based on statistical patterns. By explicitly setting the stage (or automating this context retrieval via RAG) and explaining the "why" behind what you need, you ground the model's responses in your reality. Before asking for a new feature, take a moment to drop in a quick summary of the project state.

### 2. Clear Instructions

Providing explicit instructions is crucial. It is not enough to simply ask for a piece of code; you need to define the boundaries. For example, explain what makes a good approach versus a bad approach. 

You can literally show it: *"this is the good way to create a method for our system, and this is the bad way."* Even better, show a concrete code snippet of the pattern you expect; one real example eliminates ambiguity faster than a paragraph of abstract description ever could. This level of clarity means that the AI will understand exactly what to do and, more importantly, what *not* to do. It removes ambiguity, enforces your engineering standards, and stops the model from hallucinating syntax or libraries you don't even use.

### 3. Leveraging Skills

AI models can use a variety of different "skills" (or external tools) to do their work better. Providing the AI with specific skills gives it the possibility to accomplish tasks that it simply couldn't do by just being asked what to do natively. 

Building effective skills means going beyond generic tool definitions. You need to provide rich descriptions, clear schemas for inputs and outputs, and context on *when* the AI should trigger the skill. Whether it's the ability to read a specific file format, execute a test suite, validate a configuration script, or query a database, equipping the AI with explicit, well-defined skills transforms it from a passive text generator into an active, capable engineering assistant. 

### 4. Integrating External Apps via Model Context Protocol (MCP)

As you start expanding what your AI can do, you'll eventually need it to interact with external applications. This is where the **Model Context Protocol (MCP)** becomes invaluable. 

MCP essentially gives an AI the possibility to seamlessly work with external tools. Instead of the AI being isolated to the chat window, an MCP server adds advanced skills (like giving the AI a "Playwright MCP" that allows it to open a browser, click buttons, and run end-to-end tests for you). It's about giving the AI the ability to take action. By giving the AI standard ways to hook into external apps, MCP turns a conversational chatbot into a fully capable agent that can execute real workflows across different services.

### 5. Iterate with Feedback Loops

I stopped expecting perfection on the first try. Instead, I treat AI like a collaborator: I review, correct, and refine. Each round of feedback narrows the gap between what I got and what I actually wanted. This iterative approach is especially valuable for complex tasks where the first output is a starting point, not the final answer.

### 6. Scope the Task

Breaking a large request into smaller, well-defined pieces gives the AI less room to go off-track. Instead of asking "build me an auth system," I say "create the login endpoint with token validation using this specific pattern." Smaller scope means more control, and more control means more predictable results.

### Key Insights

These pillars (**Context, Instructions, Skills, MCP, Iteration, and Scoping**) are about building the essential infrastructure and the AI environment right alongside your codebase. They are foundational assets, just like setting up a `package.json` or a CI/CD pipeline, that you configure *before* you ever write your first prompt. You implement them once (by creating your instruction markdown files, defining JSON schemas for skills, or configuring MCP servers), store them in your repository, and they permanently upgrade the AI's baseline behavior for every future session.

When working with any AI assistant, relying on zero-shot prompts often leads to inconsistent and frustrating results. By establishing deep project context (often powered by RAG), explicit instructions, well-defined skills, and using protocols like MCP to let the AI interact with external applications, you transform a generic chat into a highly tailored, predictable engineering workflow. Keep these pillars established in your repository, and your AI interactions will become significantly more effective and reproducible.

-   **Embrace Iteration**: Treat AI as a collaborator, not an oracle. Review, refine, repeat.
-   **Small Scope, Big Control**: The tighter the task definition, the more predictable and accurate the result.
