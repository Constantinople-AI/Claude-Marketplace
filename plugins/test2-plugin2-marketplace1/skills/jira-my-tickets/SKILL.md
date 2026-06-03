---
description: List all Jira tickets currently assigned to you
disable-model-invocation: true
---

Use the Jira MCP tool to fetch all issues currently assigned to the authenticated user. Steps:
1. Get the current user's Jira account ID
2. Search for issues with JQL: `assignee = currentUser() AND resolution = Unresolved ORDER BY updated DESC`
3. For each issue, display:
   - Issue key (e.g. PROJ-123) as a link if possible
   - Summary
   - Status
   - Priority
   - Project name

Group results by project. If no tickets are found, say so clearly.
