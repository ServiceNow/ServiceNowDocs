---
title: Execute a playbook from Recommended Actions
description: Launch and execute a playbook directly from the Suggested Action tab in the Recommended Actions panel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/ra-execute-playbooks.html
release: australia
topic_type: task
last_updated: "2026-07-06"
reading_time_minutes: 1
keywords: [Playbooks in Recommended Actions]
breadcrumb: [Using the Recommended Actions application, Automate and optimize, Use, Customer Service Management]
---

# Execute a playbook from Recommended Actions

Launch and execute a playbook directly from the Suggested Action tab in the Recommended Actions panel.

## Before you begin

Role required:

-   sn\_nb\_action.next\_best\_action\_user and pd\_operator for standalone playbooks.
-   sn\_nb\_action.next\_best\_action\_user for record-driven playbooks.

## About this task

When a playbook is recommended to you, it appears as an action card in the Recommended Actions panel in the Agent Workspace. Selecting the playbook action launches the playbook workflow, which guides you through a series of steps to resolve the customer issue or complete the task.

## Procedure

1.  Open a case or interaction record in the Agent Workspace.

2.  Locate the playbook action card in the Recommended Actions context side panel.

    The playbook-based recommended actions display as cards with a title, description, and Launch button. The card title matches the playbook name.

3.  Select the **Launch** button on the playbook card.

    The playbook execution initiates immediately. The playbook renders in the configured location \(contextual side panel, or related tab\).

4.  Follow the playbook workflow steps.

    The playbook guides you through a series of decision points and actions. Answer questions, select options, and complete embedded actions \(such as creating a task or escalating\) as prompted.

5.  Complete the playbook.

    When you reach the final step and confirm completion, the playbook closes. The system automatically marks the related recommended action as completed and updates the record state if configured.


## Result

The playbook execution completes successfully. After you follow the guided workflow, the system records the execution for audit and training purposes.

## What to do next

If needed, you can review the execution history of the playbook under the Recommended Actions history section to see past playbook runs, outputs, and timestamps.

If multiple team members are working on the same record, the playbook execution state is synchronized across all users. If a colleague completes the playbook, it is marked as completed for you as well.

