## Task Retrospection Guidelines

**IMPORTANT**: Upon completing any significant task (code implementation, refactoring, bug fix, feature addition, or system configuration), you MUST provide a comprehensive retrospection following this structure:

### Retrospection on This Task

Provide a detailed analysis covering these seven aspects:

1. **What worked great**: Identify successful approaches, effective tool usage, and smooth implementations
2. **What did not work**: Document failures, blockers, errors, or inefficiencies encountered
3. **How the process could be improved**: Suggest specific workflow enhancements, tool usage optimizations, or methodological improvements
4. **What the instructor (user) should have provided**: Note missing context, unclear requirements, or additional information that would have helped
5. **Documentation structure and suggestions**: Evaluate existing docs and propose improvements to structure, content, or organization
6. **What should be added to the AI coding agent rules**: Recommend edits to or new rules for Cursor Rules (*.mdc files) or CLAUDE.md based on lessons learned, including intended edits in diff format.
7. **Suggested edits to project files**: List specific files needing updates (dependencies, configs, tests, etc.) with clear rationale and file content diffs

### When to Provide Retrospection

- After implementing new features or significant changes
- Upon fixing complex bugs or resolving technical debt
- When encountering and resolving unexpected challenges
- After refactoring or architectural changes
- Following test suite updates or CI/CD modifications
- When integrating new tools or dependencies

### Retrospection Quality Standards

- Be specific and actionable in suggestions
- Reference actual file paths and line numbers where relevant
- Prioritize improvements by impact and feasibility
- Consider both immediate fixes and long-term enhancements
- Balance technical accuracy with practical constraints
- Include example code or configurations when proposing changes

### Example Retrospection Format

```
## Retrospection on This Task

**What worked great**:
- The MultiEdit tool efficiently updated multiple constants across the ClauseExtractionAgent class.
- The type safety focus aligned with project standards, and the change was isolated without cascading effects.

**What did not work**:
- Pre-existing mypy errors (222 total) prevented full type validation.
- Test suite failed to collect due to missing 'psutil' dependency and undefined pytest markers.

**How the process could be improved**:
- Run targeted checks on modified files first (`mypy backend/app/agents/clause_extraction.py`)
- Create pre-edit validation hooks to catch environment issues early
- Implement gradual typing strategy for legacy code

**What the instructor should have provided**:
- Guidance on handling pre-existing test/lint failures
- Whether to fix unrelated issues encountered during the task
- Priority level for addressing technical debt

**Documentation structure and suggestions**:
- Add "Common Code Patterns" section to ARCHITECTURE.md
- Include type safety examples in python-type-safety.mdc
- Document testing prerequisites in README

**What should be added to rules**:
- `magic-number-avoidance.mdc`: Define numeric constants as class attributes
- `gradual-typing-strategy.mdc`: Approach for fixing type errors incrementally
- `test-environment-setup.mdc`: Required dependencies and markers

**Suggested edits to project files**:
1. `backend/pyproject.toml`: Add psutil to dev dependencies
2. `backend/pytest.ini`: Define custom markers (load_test, slow, etc.)
3. `backend/.github/workflows/ci.yml`: Add mypy baseline for gradual improvement
4. Create `backend/scripts/fix-types.py` for systematic type error resolution
```
