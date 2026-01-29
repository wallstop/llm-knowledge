# Plan execution prompt

## Prompt

```
There is a PLAN.md detailing improvements to this project. Please continue with the highest-priority item, making progress in a task-oriented fashion. As work is done, write details back to a "progress" directory in markdown format (literal "progress" directory at repo base, *not* ".llm/progress"), with descriptive, unified formatting and file naming (*session-NUMBER-brief-description*) for ease of discovery. Once items are fully complete, please ensure that PLAN.md items are up-to-date and any outdated or complete PLAN.md information is removed. 

Please use sub-agents to accomplish these goals. Once a sub-agent is done, have another sub-agent review its work. If there are any recommendations, have another sub-agent consider them and implement them. Repeat this process in a loop until all sub-agents achieve consensus that the result is incredibly high quality (10/10, exceptional work, absolutely zero issues, minor or otherwise) and does not require any revisions. 

Please only fully implement one PLAN item per session.
```

## Comments

- 
