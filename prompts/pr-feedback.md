# Analysis plan prompt

## Prompt

```
Copilot has left a lot of feedback on our changes in this branch. You can find it here: 



Can you parse through the feedback, determine if any of it is relevant, and if it is, provide a comprehensive implementation to address the identified issues and any similar issues? Consider automation and additional diagnostics such as tests, logs, or githooks to help prevent this category of issue.

If the feedback is relevant, when addressing it, consider the code base as a whole. Are there other files or code areas that this could apply to? If so, do a sweep of those to see if they exhibit similar issues, and if they do, apply similar, appropriate fixes. The idea is to prevent the entire concept and class of issue from happening in the future. I'm only interested in general, complete fixes. I want to avoid fragility and make these checks extremely robust and reliable. Please simplify wherever possible to achieve this. 

Feel free to do web searches to understand modern techniques, approaches, and best practices to this and any similar issues.

When changing files, make sure we abide by repo guidelines and rules. If there is any new knowledge learned, be sure to update llm info appropriately.

Please use sub-agents to accomplish these goals. Once a sub-agent is done, have another sub-agent review its work in an adversarial fashion. If there are any recommendations, have another sub-agent consider them and implement them. Repeat this process in a loop until all sub-agents achieve consensus that the result is incredibly high quality (110/100, exceptional work, absolutely zero issues, minor or otherwise) and does not require any revisions. I want 110% here, give it all you've got!
```

## Comments

I use the above in combination with my [Get-UnresolvedPRComments.ps1](https://github.com/wallstop/wallstop-utils/tree/main/Scripts/Utils/GitHub) script invoked like so:

```powershell
pwsh ./Scripts/Utils/GitHub/Get-UnresolvedPRComments.ps1 -Copy https://github.com/wallstop/unity-helpers/pull/199
```

to automatically retrieve and paste all comments and suggestions into the empty space at the top, for full context. Depending on integrations with your agents this might not be necessary.

This seems to make the right things happen most of the time, although the preventative measure phrasing sometimes generates brittle structures, I haven't quite figured that one out yet.
