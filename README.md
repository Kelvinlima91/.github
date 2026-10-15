# ⚙️ .github (Central Configurations)

This repository centralizes global configurations and **Reusable Workflows (GitHub Actions)** for task automation and automated code reviews.

## 🤖 Gemini AI Code Review

Reusable workflow that performs automated code reviews on Pull Requests using the Google Gemini API.

### How to use in other repositories:

Create the file `.github/workflows/code_review.yml` in your project repository:

```yaml
name: Trigger Code Review

on:
  pull_request:
    types: [opened, synchronize]

jobs:
  call-review:
    uses: Kelvinlima91/.github/.github/workflows/code-review.yml@main
    secrets: inherit
