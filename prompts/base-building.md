# Codebase conversion research prompt

## Prompt

```
This repo has a generic agentic harness that works with github copilot, claude code, openai's chatgpt/codex, gemini, cursor, etc: https://github.com/wallstop/unity-helpers

The concept is that the agentic files specific to each front-end are just thin wrappers around ".llm/context.md", which holds the real context.

The ".llm" folder is organized into skills, code samples, research, all kinds of relevant llm data specific to that repo. Each file has a 300 line hard-line limit that is enforced via git hooks, tests, and CI/CD infrastrucutre, to help minimalize context.

The llm skill files have trigger metadata. A generated index (via precommit hooks, validated in CI/CD) is utilized to ensure context.md is aware of all skills/llm files.

Can you adapt this infrastructure and concept to this repo? I'm interested in:
- generic .llm/context.md
- front end agentic pointer files to context.md for all major llm vendors
- Skills specific to our repos
- File length enforcement
- Index generation
- Automation around all of this
- Clean organization
  
Please use sub-agents where appropriate to accomplish these goals. Once a sub-agent is done, have another sub-agent review its work in an adversarial fashion. If there are any recommendations, have another sub-agent consider them and implement them. Repeat this process in a loop until all sub-agents achieve consensus that the result is incredibly high quality (110/100, exceptional work, absolutely zero issues, minor or otherwise) and does not require any revisions. If not using subagents, perform this loop on your main thread. I want 110% here, give it all you've got!
```

## Comments

This is the best generic structure for "use one agentic knowledge base with every agentic front end" that I've come across. I came up with it a long time ago and haven't found anything close. The idea is that every specific agent file is just a pointer to a generic `context.md`. The context file then just shoots off pointers to all kinds of other hyper-specific files that you build up for your repo.

Works with:
- Claude
- GitHub Copilot
- Codex
- Cursor
- Gemini

## Prompt

```
This repo is from a legendary developer and has tons of useful skills, data, and workflows around using llms and agentic concepts to create work, projects, implement ideas, validate workflows, etc.

https://github.com/garrytan/gstack

Our own repo has a specific, generalized ".llm" structure that can be used for any pluggable llm front-end.

Can you do a deep analysis of the linked repo and see if we can adapt any useful, practical practices, concepts, skills, workflows, or approaches to this repo?

I'm specifically interested in:
- Code review
- Debugging / analyzing
- Architectural planning
- Preventing categories of issues
- Red/green team for impl/analysis/review/planning/testing
- Adversial/zero-knowledge hand-offs for hardening and correctness
- Testing and verification techniques and strategies (not just happy path, but positive, negative, error, extreme cases)
- Simplicity
- Single-source-of-truth
- Performance
- Reliability
- Determinism, especially in testing.
- Maintainability
- Documentation
- Roles
- Rules
- Workflows
- Mandatory gates/checks
- llm file structure/metadata/concepts/approaches

Please use sub-agents where appropriate to accomplish these goals. Once a sub-agent is done, have another sub-agent review its work. If there are any recommendations, have another sub-agent consider them and implement them. Repeat this process in a loop until all sub-agents achieve consensus that the result is incredibly high quality (110/100, exceptional work, absolutely zero issues, minor or otherwise) and does not require any revisions. If not using subagents, perform this loop on your main thread. I want 110% here, give it all you've got!
```

## Comments

After setting up the base, I then follow up with this prompt. It has a ton of bullet points. Depending on the model and context window I will hand-tune the bullets. The most important concepts are adversarial/zero-knowledge handoffs, single source of truth, and code reviews.

## Prompt

```
Can you research modern best-practices for converting and adapting a project to **INSERT_TOOL_HERE** (with **INSERT_LANGUAGE_HERE**), and add or update various llm skills and/or context, such that agentic workflows can have success with working with this project? Please search the internet for tips, tricks, and best practices over the past 5 years. Consider these as a starting point:

**INSERT_LINKS_HERE**

Please use sub-agents where appropriate to accomplish these goals. Once a sub-agent is done, have another sub-agent review its work in an adversarial fashion. If there are any recommendations, have another sub-agent consider them and implement them. Repeat this process in a loop until all sub-agents achieve consensus that the result is incredibly high quality (110/100, exceptional work, absolutely zero issues, minor or otherwise) and does not require any revisions. If not using subagents, perform this loop on your main thread. I want 110% here, give it all you've got!

Please be EXTREMELY mindful of timeouts, large content, user-requests - everything needs to happen autonomously, no sub-agent can hang or require user input. Forward progress needs to happen.

Please ensure that when doing web requests, there is some finite timeout and that they do not hang. It is imperative that this research makes forward progress.

It is extremely important that no files, like pdfs or similar, are downloaded into the main directory, or require prompts to download/select areas to download things to. This must be done fully autonomously.
```

## Comments

I find a bunch of blog posts or docs or whatever and hand-tune this prompt many times over to build up project and repo-specific knowledge and skills.

- 
