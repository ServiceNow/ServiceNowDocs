---
title: Security tasks
description: Address security threats, policy violations, and access issues on managed AI assets by acting on the security tasks the system generates for AI stewards and security reviewers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ac-security-tasks.html
release: australia
topic_type: concept
last_updated: "2026-04-23"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI, security task, AI security, threat detection]
breadcrumb: [Manage tasks and approvals, Address action items, AI Control Tower, Enable AI experiences]
---

# Security tasks

Address security threats, policy violations, and access issues on managed AI assets by acting on the security tasks the system generates for AI stewards and security reviewers.

A security task is a unit of work that AI Control Tower generates when it detects a security concern on a managed AI asset. Security tasks route to the AI steward or security reviewer responsible for the affected asset, where they can investigate the concern, take remediation action, and document the resolution. Security tasks give AI governance teams a consistent, traceable way to respond to AI-specific security threats.

## How security tasks are generated

AI Control Tower generates security tasks from several sources:

-   Threat detection on AI agents, including prompt injection, data exfiltration, and policy bypass attempts.
-   Access and privilege monitoring on AI agents that have unusual or excessive permissions.
-   Output deviation detection on AI agents whose responses depart from expected behavior.
-   Dormant agent detection on AI agents that have not been used for an extended period and may pose a stale-credential risk.

## Where security tasks appear

Security tasks appear in:

-   **Activity Center**

    Security tasks appear on the **Security tasks** sub-tab of the **Team**, **Assigned to you**, and **Unassigned** views, depending on assignment.


