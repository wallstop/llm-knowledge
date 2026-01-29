# Documentation freshness prompt

**Tag:** Experimental

## Prompt

```
Can you ensure that all documentation, comments, and examples are up-to-date, easy-to-understand, and accurate to the current state of the repo?
```

## Prompt (comprehensive audit)

```
Can you do an analysis of the documentation and ensure that it is up-to-date with production behavior? Any function/functionality/class should exist in the code base, there should be no hallucinations. We've also changed some features - please ensure that all documentation is accurate and that the code compiles. If there are images that should no longer exist, please remove them. If there should be more areas of documentation, please add them. The main goal is complete, easy-to-understand, minimally duplicated documentation with appropriate code samples and/or mermaid diagrams.

Please do a comprehensive analysis using sub-agents, make any necessary changes, and let me know what areas need manual attention.

Please ensure all documentation links resolve, all anchor links resolve.

Please do an analysis of any dead files in the docs/images subdirectories, and remove any no-longer needed or outdated files.

Plese use sub-agents to accomplish all of the above, parallelizing if possible. Once a sub-agent is done, have another sub-agent review its work. If there are any recommendations, have another sub-agent consider them and implement them. Repeat this process in a loop until all sub-agents agree that the result is incredibly high quality (10/10, absolutely zero issues, minor or otherwise) and does not require any revisions.
```

## Comments

- 
