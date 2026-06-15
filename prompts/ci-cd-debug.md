# Analysis plan prompt

## Prompt

```
Can you investigate the following CI/CD failures and determine if they represent production, configuration, or test bugs? Please provide the appropriate fix (if it is a production issue, fix production, if it is a test issue, fix tests, etc). If these are test failures, consider converting these or other tests to be data-driven. Consider adding additional diagnostics to help understand the issue(s).

Consider the code base as a whole and what the failures indicate - are they even necessary Are they fragile? 

If the problems are real, are there other files or code areas that this could apply to? If so, do a sweep of those to see if they exhibit similar issues, and if they do, apply similar, appropriate fixes. The idea is to prevent the entire concept and class of issue from happening in the future. I'm only interested in general, complete fixes. I want to avoid fragility and make these checks extremely robust and reliable. Please simplify wherever possible to achieve this. Please do not bloat the project with unnecessary tests or scripts.

Feel free to do web searches to understand modern techniques, approaches, and best practices to this and any similar issues.

Each phase of CI should also be as fast as possible - ideally <1min.

When doing work, consider applying red-green techniques.

Please use sub-agents where appropriate to accomplish these goals. Once a sub-agent is done, have another sub-agent review its work in an adversarial fashion. If there are any recommendations, have another sub-agent consider them and implement them. Repeat this process in a loop until all sub-agents achieve consensus that the result is incredibly high quality (110/100, exceptional work, absolutely zero issues, minor or otherwise) and does not require any revisions. If not using subagents, perform this loop on your main thread. I want 110% here, give it all you've got!

The logs are at "logs_*.zip"
```

## Comments

- 
