# TODO Checklist for LLM Codegen Workflow

This checklist outlines the tasks required to execute a complete LLM code generation workflow—from brainstorming an idea to executing code and refining existing code bases. Each item is designed to be thorough and serves as a checkpoint to ensure that no critical step is missed.

## Greenfield Development

### Step 1: Idea Honing
- [ ] **Brainstorm with a Conversational LLM:** Begin by asking one question at a time to explore and refine your project idea in detail.
- [ ] **Gather Detailed Responses:** Document responses that cover requirements, architecture choices, data handling strategies, error handling plans, and testing ideas.
- [ ] **Compile the Specification:** Once the conversation naturally concludes, ask the LLM to compile the discussion into a comprehensive, developer-ready specification.
- [ ] **Save Specification:** Store this final document as `spec.md` in the repository.

### Step 2: Planning
- [ ] **Feed the Spec to a Reasoning Model:** Provide the completed `spec.md` to a reasoning model to create a detailed blueprint.
- [ ] **Draft a Step-by-Step Blueprint:** Generate a detailed, step-by-step plan that outlines how to build the project.
- [ ] **Break Down into Iterative Chunks:** Divide the blueprint into small, manageable prompts that are sequentially dependent and testable.
- [ ] **Ensure Integration:** Verify that each chunk is sufficiently detailed to avoid orphaned code, and that later steps naturally integrate previous work.
- [ ] **Generate a Prompt Plan:** Format the collection of prompts (using markdown code tags) and save it as `prompt_plan.md` in the repository.
- [ ] **Create This Checklist:** Use this `todo.md` file to keep track of progress across all stages.

### Step 3: Execution
- [ ] **Repository Setup:** Initialize the repository with boilerplate code (e.g., using uv, cargo, or similar tools).
- [ ] **Iterative Code Generation:** For each prompt in `prompt_plan.md`, input the prompt into your codegen tool (such as Claude or Aider) and copy the generated code into your IDE.
- [ ] **Test and Validate:** Run the code and execute tests. If tests pass, integrate the code; if not, use debugging tools (like repomix) to troubleshoot and refine.
- [ ] **Integration and Progression:** After each prompt’s output is validated, check off the corresponding task and proceed to the next prompt.
- [ ] **Final Integration:** Once all prompts have been executed and integrated, ensure that the entire system works together seamlessly.

## Non-Greenfield / Legacy Code Updates

- [ ] **Context Extraction:** Use a tool (e.g., repomix) to extract the relevant codebase context into an `output.txt` file.
- [ ] **Generate Code Review:** Pass `output.txt` to the LLM with a code review prompt to identify issues, bugs, or design improvements.
- [ ] **Generate GitHub Issues:** Use the LLM to convert findings into actionable GitHub issues that can be assigned and tracked.
- [ ] **Identify Missing Tests:** Have the LLM generate a list of missing test cases and suggested tests to improve coverage.
- [ ] **Iterative Improvement:** Apply fixes and enhancements based on the generated reviews and issues. Validate changes with a full test suite.
- [ ] **Document Updates:** Update the README or create new documentation as needed to reflect changes in the codebase.

## Additional Considerations

- [ ] **Version Control:** Maintain robust version control and backup for all key files, including `spec.md`, `prompt_plan.md`, and `todo.md`.
- [ ] **Monitor Token Usage:** Keep an eye on LLM token consumption and adjust prompt lengths or complexity if necessary.
- [ ] **Prompt Refinement:** Periodically review and refine your prompts to ensure clarity, consistency, and effectiveness.
- [ ] **Collaborative Checks:** Although this workflow is solo-focused, consider periodic pair programming or external reviews to validate progress.
- [ ] **Self-Care:** Ensure you take regular breaks and manage workload effectively to maintain sustainable productivity.

This checklist should serve as a living document—update and refine it as your workflow evolves. Each task should be marked complete only after it has been fully validated, ensuring a robust and integrated development process.
