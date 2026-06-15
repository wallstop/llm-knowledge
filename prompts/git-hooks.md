# Fixing Git Hooks

## Prompt

```
Can you investigate the following githook failures? It is critical that the githooks are a last-resort. Ideally, failures such as these are caught in agentic workflows - see if there is opportunity to improve llm workflows, contenxt, and rules with automation. All githooks must be able to run on native linux, windows, and mac machines, with their own versioned executables - keep dependencies as minimal as possible, and do not rely on running inside of a devcontainer or this exact environment (for example, node module mismatch, auto-repair). Open source powershell is preferred over any other shell. I want zero manual touch - if automated recovery is possible, it is required.

The goal is to understand why the issues are happening, understand the root caus(es), apply relevant fixes, and create infrastructure such that the entire category of issues can not be made again, but, also, verify that whatever is being tested is even necessary - are we just creating unecessary work?

I'm only interested in general, complete fixes - this work should be generalized as much as possible. I want to avoid fragility and make these checks extremely robust and reliable.

All git hooks must be incredibly fast: targeting <1s for the full suite. Any slower runs than this must be investigated and fixed. There must be no manual actions to achieve this.

Feel free to do web searches to understand modern techniques, approaches, and best practices to this and any similar issues.

Please do not bloat the project with unnecessary tests or scripts.

When doing work, consider applying red-green techniques.

Please use sub-agents where appropriate to accomplish these goals. Once a sub-agent is done, have another sub-agent review its work in an adversarial fashion. If there are any recommendations, have another sub-agent consider them and implement them. Repeat this process in a loop until all sub-agents achieve consensus that the result is incredibly high quality (110/100, exceptional work, absolutely zero issues, minor or otherwise) and does not require any revisions. If not using subagents, perform this loop on your main thread. I want 110% here, give it all you've got!
```

## Comments
