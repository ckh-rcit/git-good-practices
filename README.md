# General Good Practices for GIT/GITHUB Usage

Guide on general good practices to use go by when working with GIT/GITHUB

# Commit Notes & Descriptions

When you push a commit, ensure that your commit message is clear and descriptive enough for others to quickly understand its purpose and determine if it's relevant to what they are looking for.

## Conventional Commits

The Conventional Commits specification is a lightweight standard that helps improve the readability and structure of commit messages, making it easier to manage and understand the history of a project.

The general format of a conventional commit message is:
```
<type>(<scope>): <description>

<body>

<footer>
```

## Here are the components:

1. **\<type>**: A short string indicating the purpose of the commit. Common types include:
- ***feat***: A new feature
- ***fix***: A bug fix
- ***chore***: Tasks that don't modify the code, like updating dependencies or build scripts
- ***refactor***: Code changes that neither fix a bug nor add a feature, usually to improve code quality or readability
- ***docs***: Changes to documentation
- ***style***: Changes to code formatting, such as whitespace or semicolons, that don't affect the code's logic
- ***test***: Adding or updating tests
- ***perf***: Code changes that improve performance
- ***build***: Changes to the build system or external dependencies
- ***ci***: Changes to continuous integration configuration files and scripts
- ***revert***: Reverting a previous commit
2. **(&lt;scope&gt;)**: Optional. A short description of the part of the codebase the commit affects, typically enclosed in parentheses. This can be a module, component, or specific area of the code.

3. **\<description>**: A brief, imperative description of the change, e.g., "Add user login functionality" or "Fix memory leak in image processing".

4. **\<body>**: Optional. A more detailed explanation of the commit, if necessary. It should explain the motivation for the change and contrast it with previous behavior.

5. **\<footer>**: Optional. This section can include references to related issues or commits, such as "Closes #123" or "See #456 for more information."

**Example of a "good" commit:**
```markdown
feat(powershell): Add Get-ServerStatus function

This commit introduces a new function, Get-ServerStatus, to the
PowerShell script for monitoring server health. The function retrieves
the status of various server components and services.

- Add Get-ServerStatus function to ServerHealth.ps1
- Implement checks for CPU usage, memory usage, and disk space
- Include checks for critical services (IIS, SQL Server, etc.)
- Return a status object with overall health and individual component statuses

Related to #15
```
**Explanation of the components:**
- feat(powershell): This indicates that the commit adds a new feature related to the PowerShell script.
- Add Get-ServerStatus function: A brief, imperative description of the change.
The body of the message provides a more detailed explanation of the commit, including a list of specific changes made to implement the feature.
- Related to #15: The footer includes a reference to a related issue in the issue tracker (e.g., GitHub).
