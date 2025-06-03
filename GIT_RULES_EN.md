# Git Usage Rules  
**Version 2.0**

---

## 1. Branch Rules

- Avoid pushing directly to main branches like `main` or `develop`.
- Create a new branch for each task, feature, or bug fix.
- Branches should usually be created from `develop`, unless otherwise instructed (e.g., `main` for hotfixes).

### Branch Naming Convention

Branch names must begin with the task ID and follow this structure:

- New feature: `feature/TASK-ID-feature-name`
- Bug fix: `bugfix/TASK-ID-description`
- Hotfix: `hotfix/TASK-ID-critical-issue`
- Test: `test/TASK-ID-test-description`

**Examples:**

- `feature/PROJ-101-user-login`
- `bugfix/PROJ-102-validation-error`

> ⚠️ **Hotfix branches** should be used only for critical issues requiring immediate attention, such as system outages or security problems.

---

## 2. Commit Message Rules

Commit messages must follow this structure:

```
TASK-ID: <type>(<scope>): <short message>
```

### Examples:

- `PROJ-101: feat(auth): add SMS login`
- `PROJ-102: fix(payment): correct total calculation`
- `PROJ-103: docs(api): update endpoint descriptions`

### Allowed Commit Types:

- `feat`: Add a new feature
- `fix`: Fix a bug
- `refactor`: Code refactoring without changing behavior
- `docs`: Documentation changes
- `style`: Code style changes (non-functional)
- `test`: Add or update tests
- `chore`: Maintenance tasks or tooling updates
- `perf`: Code performance improvements

> 💡 **Notes:**
> - Keep messages short, clear, and written in English using the present tense.
> - Each commit should contain only one logical change (Atomic Commit).

---

## 3. Merge Request (MR) Rules

- After completing a task, open a Merge Request to `develop` (or `main` in case of hotfix).
- Include the task ID and a short description in the MR title.  
  _Example:_ `PROJ-101: Merge feature/user-login into develop`
- Developers are responsible for resolving conflicts before submitting MRs.

### Code Review Guidelines

- Minimum review count (e.g., 2–3 reviewers) should be followed as per team guidelines.
- Final review must be done by a Tech Lead.
- All technical feedback or suggestions must be documented as comments.

### Source Branch Cleanup

- Enable the **"Delete source branch after merge"** option, unless explicitly needed.
- Any leftover branches should be resolved and deleted within two weeks of the merge.

---

## 4. Open Branch Limit per Developer

- Each developer should have **no more than 2 active branches** at a time.
- Outdated or inactive branches must be cleaned up regularly to keep the repository organized.

---

_These rules are subject to review and update based on project and team needs._
