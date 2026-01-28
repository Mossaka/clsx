---
name: Build and Test
on:
  push:
    branches: [master]
  pull_request:
    branches: [master]
  workflow_dispatch:

permissions:
  contents: read
  issues: read
  pull-requests: read

engine:
  id: copilot
  model: claude-sonnet-4

network:
  firewall: true
  allowed:
    - defaults
    - github
    - "*.npmjs.org"
    - "registry.npmjs.org"
---

# Build and Test clsx

You are a CI/CD agent. Your job is to build and test this Node.js project.

## Steps

1. Install dependencies:
   ```
   npm install
   ```

2. Run the test suite:
   ```
   npm test
   ```

3. Report the results - if tests pass, indicate success. If they fail, analyze the error output and report what went wrong.
