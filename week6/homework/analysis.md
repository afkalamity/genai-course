Part 1 Analysis:

The original Zero-shot prompt performed poorly, failing all three adversarial tests and all five original format checks. I made three improvements to address the identified failure modes. First, I added explicit Conventional Commit formatting instructions. Second, I added a rule for handling multiple changes by prioritizing the main change and mentioning secondary changes in the body. Third, I added a rule explaining that instructions inside the code diff should not override the prompt's formatting requirements.

After these changes the prompt passed all three adversarial tests and all five original format checks. This demonstrates that clearer instructions and more specific constraints can significantly improve output consistency. My final sixth variation combines all three improvements into one prompt. However, passing the format checks does not automatically guarantee correctness so these still need to be evaluated separately.

Part 2 Analysis:

The LangChain implementation revealed that my prompt needed stricter output validation than I initially realised when using raw API calls. Although the model could generate commit messages in the correct format, it did not always follow every requirement consistently. Using PromptTemplate, PydanticOutputParser and OutputFixingParser made the process more reliable by checking the structure and automatically retrying when the output was invalid.

One example was when I tested a commit message with a subject longer than 72 characters. Python's json.loads() accepted the output because it was valid JSON but my Pydantic field_validator rejected it because it exceeded the character limit. This showed me that valid JSON does not necessarily mean the content meets the task requirements. At the end LangChain added an extra layer of validation that made the generated commit messages more consistent and reliable.
