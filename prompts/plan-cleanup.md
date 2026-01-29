# Plan cleanup prompt

## Prompt

```
There is a PLAN.md detailing various improvements. Can you do an analysis of the current state of the project, compare it to the PLAN.md, and remove all items from the PLAN.md that are fully completed and no longer relevant? Remove similar checkpoint items that are fully complete and no longer relevant. 

Please use sub-agents to accomplish these goals. Once a sub-agent is done, have another sub-agent review its work. If there are any recommendations, have another sub-agent consider them and implement them. Repeat this process in a loop until all sub-agents achieve consensus that the result is incredibly high quality (10/10, exceptional work, absolutely zero issues, minor or otherwise) and does not require any revisions. 
```

## Comments

- 
