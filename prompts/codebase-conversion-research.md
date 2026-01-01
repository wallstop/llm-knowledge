# Codebase conversion research prompt

## Prompt

```
Can you research modern best-practices for converting and adapting a codebase to **INSERT_TOOL_HERE** (with **INSERT_LANGUAGE_HERE**), and add or update various llm skills and/or context, such that agentic workflows can have success with updating code? Please search the internet for tips, tricks, and best practices over the past 5 years. Consider these as a starting point:

**INSERT_LINKS_HERE**

Plesae utilize sub-agents to accomplish these goals.

Please be EXTREMELY mindful of timeouts, large content, user-requests - everything needs to happen autonomously, no sub-agent can hang or require user input. Forward progress needs to happen.

Please ensure that when doing web requests, there is some finite timeout and that they do not hang. It is imperative that this research makes forward progress.

It is extremely important that no files, like pdfs or similar, are downloaded into the main directory, or require prompts to download/select areas to download things to. This must be done fully autonomously.
```

## Comments

- 
