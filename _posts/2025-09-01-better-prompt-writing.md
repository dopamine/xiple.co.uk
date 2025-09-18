---
layout: post
title:  "Better prompt writing"

coverimg: 20XX-XX-XX-folder/image
---

Andrej Karpathy’s [Deep Dive into LLMs like ChatGPT](https://www.youtube.com/watch?v=7xTGNNLPyMI&ab_channel=AndrejKarpathy) is a 3hr technical lecture, with his [How I use LLMs](https://youtu.be/EWvNQjAaOHw) adding another 2hrs (not for the faint hearted) and I’m not mentioning these as something to watch (unless that is your jam). In a fit of hyperfocus, I did that for you.

Here’s what I learned from them about how to take advantage of tool use and the context window (“LLM working memory”) and write better prompts/queries:

- Generally speaking it’s best to start a new chat each time so the context window doesn’t get clogged up, instead of chatting in the same session thinking that it will “build up memory”.
- Tools are available in the more advanced models (like what we have access to here at Xero), so you can do things like:
    - Say `use web search` if you actually want the LLM to reference up to date content beyond its training.
    - Say `use code` to solve this if you’re asking a math question (or any question that could be abstracted into and solved by maths).
- LLMs are not good at one-shotting short answers. You’ll get much better results with: 
Write 1000 words on the topic, then finish up at the end with an exec summary / TL;DR, ie one paragraph, or a keywords only bullet list, or a concise stepped process summarising everything you’ve written. This way you get the short answer at the end but you allowed it some “thinking time” to build up more relevant text in its context window before giving you the answer.
- Good prompt format / great for gem instructions:
    - clear instruction
    - examples of input & expected output (this gives the level up!)
    - additional tweak instructions
- Gems are best used to store recurring prompts in, not as “topic experts”. Eg. a good use case is a gem for generating discussion guides based on attached templates and instructions saved in the Gem + your outline as text input, instead of a “brain” that knows everything about a certain topic.
