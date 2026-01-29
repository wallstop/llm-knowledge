# Analysis plan prompt

## Prompt

```
Copilot has left a lot of feedback on our changes in this branch. You can find it here: 

**INSERT_FEEDBACK_AND_LINK_TO_PR**

Can you parse through the feedback, determine if any of it is relevant, and if it is, provide a comprehensive implementation to address the identified issues and any similar issues? Consider adding/updating/modifying llm skills/guidance with any new knowledge so the issues can be prevented in the future.

Please use sub-agents to accomplish these goals. Once a sub-agent is done, have another sub-agent review its work. If there are any recommendations, have another sub-agent consider them and implement them. Repeat this process in a loop until all sub-agents achieve consensus that the result is incredibly high quality (10/10, exceptional work, absolutely zero issues, minor or otherwise) and does not require any revisions. 
```

## Comments

- 
