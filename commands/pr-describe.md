# PR Describe

Create a PR description for $ARGUMENTS.
Read the entire file first to get a thorough understanding.

1. **Understand the code first**
Use the following to understand the code changes:
```sh
git log -p --reverse main..HEAD
```

Read affected files to understand the changes beyond the diffs -- in the broader context of the codebase.

2. **Start with Why**
Answer any of the following questions:
- "Why is this PR required?"
- "Why do we want those changes in the codebase?"

Thsi is the most important part of the PR so be as detailed as possible.

3. **Dive into What**
Group code changes in the way that makes the most sense:
- refactoring
- UI, style & design system
- database
- test
- etc.

4. **QA**
Write a bullet point lists of what was tested to help reviewers identify missing test cases.

5. **Highlight what you think deserves the most attention**
Usually business logic and data validation are the core of the pull requests and deserve particular attention from reviewers.

6. **Prepare the PR description**
Use this template:

```
# Why
[Why is this change needed? Business context/problem being solved]

# What
[Group changes logically - refactoring, UI, database, tests, etc.]

# QA
- [ ] [Toggleable (using `<details></details>`) summary of which scenarios are covered by automated tests if any]
- [ ] [Specific steps to reproduce/verify the changes]

# Review Focus
[What deserves the most reviewer attention? Business logic, security, performance, etc.]

# Screenshots/Media
[If UI changes - before/after screenshots, videos, etc.]

# Notes
[Breaking changes, limitations, deployment considerations, follow-up work, etc.]
```

7. **Push the PR description to GitHub**
```sh
gh pr edit $ARGUMENTS --title <some title> --body <some body>
```
---
- Remember to use the GitHub CLI (`gh`) for all GitHub-related tasks.
- Do not create any file