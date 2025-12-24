# Documentation freshness prompt

**Tag:** Experimental

## Prompt

```
Can you ensure that all documentation, comments, and examples are up-to-date, easy-to-understand, and accurate to the current state of the repo?
```

## Prompt (comprehensive audit)

```
Can you do an analysis of the documentation and ensure that it is up-to-date with production behavior? Any function/functionality/class should exist in the code base, there should be no hallucinations. We've also changed some features - please ensure that all documentation is accurate and that the code compiles. If there are images that should no longer exist, please remove them. If there should be more areas of documentation, please add them. The main goal is complete, easy-to-understand, minimally duplicated documentation with appropriate images/gifs (or stubs, that I need to fill in) for functionality.

Please do a comprehensively analysis using sub-agents, make any necessary changes, and let me know what areas need manual attention, as well as what images/gifs I either need to replace or add.
```

## Comments

- 
