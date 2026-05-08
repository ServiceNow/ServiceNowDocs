---
title: Remediate Scan Engine findings with Now Assist
description: The Remediate Scan Engine findings with Now Assist feature accelerates technical debt resolution by providing AI-generated code fixes for leading practice violations. Developers can track and resolve issues in their code throughout the end-to-end workflow by reviewing and applying AI-recommended fixes.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [Now Assist for Platform Health, Platform Health, Using Impact, Impact]
---

# Remediate Scan Engine findings with Now Assist

The Remediate Scan Engine findings with Now Assist feature accelerates technical debt resolution by providing AI-generated code fixes for leading practice violations. Developers can track and resolve issues in their code throughout the end-to-end workflow by reviewing and applying AI-recommended fixes.

For findings already identified by the scan engine, developers can generate AI-recommended fixes in bulk, review proposed changes, and apply fixes.

Goals:

-   Accelerate technical debt reduction across your instance with reduced time spent manually researching and writing code fixes.
-   Maintain code quality by aligning fixes with ServiceNow leading practices.
-   Keep developers in control with an AI code review before implementing suggestions.

## Remediation workflow

Once the Scan Engine returns findings, the Developers can view findings that are assigned to them and evaluate the AI generated suggestions.

![Demonstrates the workflow from Scan Engine findings and a developer using the Resolve Scan Engine findings for code fixes and issue resolution.](../image/remediation-agent-workflow-2.png)

## Resolve Scan Engine findings fix statuses

|Status|Description|
|------|-----------|
|Pending Review|AI fix has been generated and is awaiting developer review|
|In Review|Developer has opened the fix for review|
|Accepted|Developer accepted the fix as-is; code has been updated|
|Accepted with Modifications|Developer accepted the fix with edits; code has been updated|
|Rejected|Developer rejected the fix; finding requires manual resolution|
|Error|AI was unable to generate a fix for this finding|

