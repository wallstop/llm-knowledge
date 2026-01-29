# Analysis plan prompt

## Prompt

```
Can you investigate the following CI/CD failures and determine if they represent production, configuration, or test bugs? Please provide the appropriate fix (if it is a production issue, fix production, if it is a test issue, fix test, if it is a configuration issue, fix the configuration). Please consider this and similar edge case and error scenarios - if it is possible to add additional tests that would help catch this and other, similar problems, please do so. Consider converting these or other tests into data-driven tests. Please add additional test diagnostics to help you understand the issue(s). Consider simplifying and/or consolidating tests if there are too many overlapping concerns. Consider adding or updating llm skills and/or guidance with any gained knowledge, to help prevent the category of issue in the future.

Please use sub-agents to accomplish these goals. Once a sub-agent is done, have another sub-agent review its work. If there are any recommendations, have another sub-agent consider them and implement them. Repeat this process in a loop until all sub-agents achieve consensus that the result is incredibly high quality (10/10, exceptional work, absolutely zero issues, minor or otherwise) and does not require any revisions. 

This is on gitea version 1.25.4. Feel free to do web searches.
```

## Comments

- 
