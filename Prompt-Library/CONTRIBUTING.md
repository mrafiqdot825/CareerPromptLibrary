# Contributing to Prompt Library

Thank you for taking the time to contribute to **Prompt Library**!

We welcome contributions of high-quality AI system prompts, templates, category improvements, and workflow guides.

## Guidelines for Prompts

When adding or updating a prompt file:

1. **Structured Layout**: Every prompt file should include:
 - **Role & Persona**: Clear domain expertise definition.
 - **Objective**: What the prompt achieves.
 - **System Prompt**: Exact system instructions for the LLM.
 - **User Prompt Template**: Parameterized prompt with `{{VARIABLES}}`.
 - **Expected Output Format**: Clear structural requirements for responses.
 - **Best Practices & Pro Tips**: Edge cases and optimization tips.

2. **No Hallucinations**: Ensure system prompts enforce non-hallucinatory constraints, type safety, and real-world best practices.

3. **Markdown Standards**: Follow standard GitHub Flavored Markdown styling.

## Submitting a PR
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/new-prompt`).
3. Commit your changes (`git commit -m "feat(ai): add vector search prompt"`).
4. Push to your branch and submit a Pull Request.
