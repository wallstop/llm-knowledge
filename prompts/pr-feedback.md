# Analysis plan prompt

## Prompt

```
Copilot has left a lot of feedback on our changes in this branch. You can find it here: 



Can you parse through the feedback, determine if any of it is relevant, and if it is, provide a comprehensive implementation to address the identified issues and any similar issues? Consider automation, such as tests or githooks to help prevent this category of issue. Please add additional diagnostics to help understand the issue(s). Consider simplifying if there are too many overlapping concerns, too much complexity, or too much fragility. When changing files, make sure we abide by repo guidelines and rules. If there is any new knowledge learned, be sure to update llm info appropriately.

The goal is to understand why the issues are happening, understand the root caus(es), apply relevant fixes, and create infrastructure such that the entire category of issues can not be made again. I'm only interested in general, complete fixes. I want to avoid fragility and make these checks extremey robust and reliable.

If the feedback is relevant, when addressing it, consider the code base as a whole. Are there other files or code areas that this could apply to? If so, do a sweep of those to see if they exhibit similar issues, and if they do, apply similar, appropriate fixes. The idea is to prevent the entire concept and class of issue from happening in the future.

The goal is to understand why feedback is being given, understand the root cause of the feedback, apply relevant fixes, and create infrastructure such that the issues the feedback uncovered can not be made again. I'm only interested in general, complete fixes. I want to avoid fragility and make these checks extremey robust and reliable.

Feel free to do web searches to understand modern techniques, approaches, and best practices to this and any similar issues.

Please use sub-agents to accomplish these goals. Once a sub-agent is done, have another sub-agent review its work in an adversarial fashion. If there are any recommendations, have another sub-agent consider them and implement them. Repeat this process in a loop until all sub-agents achieve consensus that the result is incredibly high quality (110/100, exceptional work, absolutely zero issues, minor or otherwise) and does not require any revisions. I want 110% here, give it all you've got!
```

## Comments

- 
