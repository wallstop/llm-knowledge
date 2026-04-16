# Plan creation prompt

## Prompt

```
Can you figure out a comprehensive plan for addressing these problems? After a plan/fix is identified, I want it systematically applied/fixed forever in this project - via tests, llm concepts, etc.

Feel free to do web searches to understand modern techniques, approaches, and best practices to this and any similar issues.
```

## Comments

Whenever I'm iterating on a project, I usually list a bunch of problems and goals then slap this prompt onto the end to kick off plan mode.

# Plan write-to-file prompt

## Prompt

```
This plan is great! Please write out a detailed, prioritized PLAN.md action plan with enough information to fully implement all of the above. Once PLAN.md is written, please end the current session - there is no need to take any more action. I don't want any implementation done, code written, etc - there's nothing left to do after PLAN.md exists and contains the above information.
```

## Comments

Whenever I have an agent do plan mode, if the plan is larger than 2 phases, I utilize the above prompt to write it out to a PLAN.md file checked into the repo. I then spin up new, fresh, targeted sessions for agents to focus on specific areas of the plan. I've noticed that for larger scopes, agents have a difficult time fitting everything into one session in a reliable manner, even with sub-agents. If you're able to get a PLAN.md file, you can review it, and you can have agents implement small, scoped sections, with much higher quality.

# Plan execution prompt

## Prompt

```
There is a PLAN.md detailing improvements to this project. Please continue with the highest-priority item, making progress in a task-oriented fashion. As work is done, write details back to a "progress" directory in markdown format (literal "progress" directory at repo base, *not* ".llm/progress"), with descriptive, unified formatting and file naming (*session-NUMBER-brief-description*) for ease of discovery. Once items are fully complete, please ensure that PLAN.md items are up-to-date and any outdated or complete PLAN.md information is removed. 

Please use sub-agents to accomplish these goals. Once a sub-agent is done, have another sub-agent review its work in an adversarial fashion. If there are any recommendations, have another sub-agent consider them and implement them. Repeat this process in a loop until all sub-agents achieve consensus that the result is incredibly high quality (110/100, exceptional work, absolutely zero issues, minor or otherwise) and does not require any revisions. I want 110% here, give it all you've got!

Please only fully implement max five PLAN items per session - only one or two items if they are large, more if they are smaller.
```

## Comments

"There's a plan, do the plan!"

# Plan cleanup

```
There is a PLAN.md detailing various improvements. Can you do an analysis of the current state of the project, compare it to the PLAN.md, and remove all items from the PLAN.md that are fully completed and no longer relevant? Remove similar checkpoint items that are fully complete and no longer relevant. 

Please use sub-agents to accomplish these goals. Once a sub-agent is done, have another sub-agent review its work in an adversarial fashion. If there are any recommendations, have another sub-agent consider them and implement them. Repeat this process in a loop until all sub-agents achieve consensus that the result is incredibly high quality (110/100, exceptional work, absolutely zero issues, minor or otherwise) and does not require any revisions. I want 110% here, give it all you've got!
```

## Comments

Sometimes my plans are 2k+ lines, and agents are working through it. This works as cleanup midway through a plan, to help reduce the context bloat of further sessions that have to parse through a large plan file with partial status.
