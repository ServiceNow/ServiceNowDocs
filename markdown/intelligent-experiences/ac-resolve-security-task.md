---
title: Resolve a security task
description: Investigate a security concern that AI Control Tower has detected on a managed AI asset, take the appropriate remediation action, and document the resolution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ac-resolve-security-task.html
release: zurich
topic_type: task
last_updated: "2026-07-16"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Security tasks, Manage tasks and approvals, Address action items, AI Control Tower, Enable AI experiences]
---

# Resolve a security task

Investigate a security concern that AI Control Tower has detected on a managed AI asset, take the appropriate remediation action, and document the resolution.

## Before you begin

Role required: sn\_ai\_asset\_mgmt.ai\_asset\_owner or sn\_ai\_governance.ai\_steward

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Activity Center** &gt; **Work** &gt; **Assigned to you**.

2.  Select the **Security tasks** sub-tab.

3.  Select the security task that you want to resolve.

    The task opens in a side panel with the affected asset, the type of security concern that triggered the task, the supporting evidence, and any recommended remediation actions.

4.  Investigate the security concern.

    Review the evidence in the task, examine the asset's security posture on the asset record's **Security** tab, and determine whether the concern is a true positive that needs remediation or a false positive that can be dismissed.

5.  Take the remediation action that addresses the security concern.

    Remediation actions vary by the type of concern. For example, a prompt injection task might require updating the agent's guardrails, while a dormant agent task might require retiring the agent or rotating its credentials.

6.  Document the resolution and update the task status.

    Record the action you took and the outcome in the task's resolution notes so the security audit trail is complete. Set the task status to **Completed** when the work is done.


## Result

The resolved security task no longer appears in the **Assigned to you** view. The asset record's **Security** tab reflects the updated security posture. If the underlying condition recurs, AI Control Tower generates a new security task.

