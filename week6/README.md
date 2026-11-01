My task was to generate Conventional Commit messages from code changes made during my previous Week 5 labs. I wanted to compare different prompting techniques and see which one produced the most accurate, useful and correctly formatted commit messages.

I tested five prompting variations using the same five code changes to make the comparison fair. I evaluated each variation based on correctness, usefulness, format compliance, token usage and estimated cost.

V5 was my chosen winning variation because it combined role based instructions, examples and structured output requirements. It produced consistently well formatted commit messages and achieved a 100% format pass rate on the five original tests.

I also improved the original Zero-shot prompt through three iterations, creating a sixth variation. This addressed formatting issues, ambiguous instructions and conflicting constraints. The improved version passed all three adversarial tests and all five original format checks.

This experiment showed that combining different prompting techniques and providing clear instructions can improve the consistency of AI generated outputs. Using LangChain and Pydantic also added an extra layer of validation to make the results more reliable.


