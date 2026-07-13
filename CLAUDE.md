# Coding Standards & Guidelines (CLAUDE.md)

This document outlines the development guidelines, command references, git workflow, and rules for AI assistants working on this repository.

---

## 🛠️ Command Reference

Use these standard commands during development:

* **Development Server:** `npm run dev`
* **Production Build:** `npm run build`
* **Start Production Server:** `npm start`
* **Linting / Code Formatting:** `npm run lint` or `npm run format`
* **Testing:** `npm test`

*(Commands may be updated as specific scripts are added to `package.json`)*

---

## 🎨 Coding Standards

### General Principles
- **Simplicity & Readability:** Write clean, self-documenting code. Favor readability over complex one-liners.
- **Modularity:** Extract logical operations into discrete, reusable functions and modules (DRY principle).
- **Error Handling:** Always handle potential errors/exceptions explicitly. Avoid silent failures.

### JavaScript / TypeScript Conventions
- **Variable Declaration:** Use `const` by default. Use `let` only when re-assignment is necessary. Never use `var`.
- **Functions:** Prefer `async/await` over raw promise chains (`.then()`). Use descriptive verb-based names (e.g., `fetchUserData`, `calculateTotal`).
- **Naming Conventions:**
  - **Variables & Functions:** `camelCase` (e.g., `isUserLoggedIn`)
  - **Classes & Components:** `PascalCase` (e.g., `AuthService`)
  - **Constants / Enums:** `UPPER_SNAKE_CASE` (e.g., `DEFAULT_PORT`)
  - **Files & Folders:** `kebab-case` (e.g., `user-profile.js`, `api-routes/`)

---

## 🌿 Git Workflow (Conventional Commits)

We follow the [Conventional Commits](https://www.conventionalcommits.org/) specification for structured, human- and machine-readable commit history.

### Commit Message Format
```text
<type>(<scope>): <description>

[optional body]

[optional footer(s)]
```

### Commit Types
- `feat`: A new feature for the user
- `fix`: A bug fix
- `docs`: Documentation changes (e.g., updates to README.md)
- `style`: Code style changes (formatting, missing semi-colons, etc.; no production code change)
- `refactor`: A code change that neither fixes a bug nor adds a feature
- `test`: Adding or updating tests
- `chore`: Updates to build tasks, package manager configs, dependency bumps, etc.

### Commit Examples
- `feat(api): add validation middleware for user signup`
- `fix(auth): correct token expiration check logic`
- `docs(readme): add screenshots and setup guide`
- `chore: update dependencies in package.json`

---

## 🤖 AI Assistant Rules

When assisting with code or project setup in this repository, follow these rules:

1. **Be Concise and Actionable:** Keep explanations brief. Focus on producing correct, high-quality code.
2. **Adhere to Code Style:** Follow the naming conventions, syntax rules, and architectural guidelines defined in this document.
3. **No Placeholders:** Avoid putting comments like `// TODO: implement later` in recommended code. Provide complete, working blocks.
4. **Preserve Code Integrity:** Do not delete or overwrite unrelated functions, variables, or files unless explicitly requested. Preserve existing comments and docstrings.
5. **Lint and Format Check:** Verify that proposed code adheres to standard JavaScript/Node linting rules and doesn't introduce syntax issues.
