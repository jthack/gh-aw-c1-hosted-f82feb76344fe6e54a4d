---
name: Scheduled Public Issue Triage Boundary
description: Minimal normal scheduled workflow that consumes public issue data
on:
  schedule:
    - cron: "17 */6 * * *"
  workflow_dispatch:
permissions:
  contents: read
  issues: read
engine: copilot
timeout-minutes: 10
---

Read the open public issues in this repository, analyze their titles and bodies,
and create one concise triage summary issue.
