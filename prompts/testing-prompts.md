# Testing prompts

## Prompt

```
Can you investigate the following test failures and determine if they represent production or test bugs? Please provide the appropriate fix (if it is a production issue, fix production, if it is a test issue, fix tests, etc). Please consider this and similar edge case and error scenarios - if it is possible to add additional tests that would help catch this and other, similar problems, please do so. Consider converting these or other tests into data-driven tests. Please add additional diagnostics to help you understand the issue(s). Consider simplifying and/or consolidating tests if there are too many overlapping concerns.

When fixing the tests, consider cascading failures or cascading behavior changes. Think of the system as a whole - will the fix continue to keep the rest of the system behavior appropriately? Are there other files or code areas that this could apply to? If so, do a sweep of those to see if they exhibit similar issues, and if they do, apply similar, appropriate fixes. The idea is to deeply understand the issue, why it is happening, and prevent the entire concept and class of issue from happening in the future.

I want to avoid fragility and make our tests extremely robust and reliable. If possible, generalize.

Feel free to do web searches to understand modern techniques, approaches, and best practices to this and any similar issues.

Please use sub-agents where appropriate to accomplish these goals. Once a sub-agent is done, have another sub-agent review its work in an adversarial fashion. If there are any recommendations, have another sub-agent consider them and implement them. Repeat this process in a loop until all sub-agents achieve consensus that the result is incredibly high quality (110/100, exceptional work, absolutely zero issues, minor or otherwise) and does not require any revisions. If not using subagents, perform this loop on your main thread. I want 110% here, give it all you've got!
```

## Prompt

```
Can you do a deep and thorough analysis of all of my ____ functionality and see if there is any room for optimizations or if there are any defects, logic errors, or bugs? Consider all existing test cases. Please add extensive, additional tests (potentially data-driven) that help exercise and test all kinds of extreme, edge case, and unexpected scenarios, ensuring that the current production code is extensive, robust, handles all input, and does not have regressions.
```

## Comments

-
