---
title: Interactive activities
description: An interactive activity prompts a user for input in your playbook as it runs.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Playbooks reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Interactive activities

An interactive activity prompts a user for input in your playbook as it runs.

An interactive activity requires user input to complete. Agents can provide the input within the activity card during the playbook run. For example, if your activity requires a user to enter work notes for a record, you can configure the activity inputs to prompt a playbook agent to add work notes information in the playbook card.

![Activities turn into cards.](../images/interactive-activity-overview.png "Interactive activities")

Interactive activities turn into activity cards that require user input in a Playbook experience. Playbook agents must interact with these cards so that the playbook can continue running.

To learn how to design a playbook with interactive activities, see [design an automated process](../task/design-automated-process.md).

-   **[Adobe Acrobat Sign activities](../reference/pad-activities-adobe-sign.md)**  
Enable agents and fulfillers to collect electronic signatures during a playbook run, via Workflow Data Fabric's Adobe Acrobat Sign spoke.
-   **[Advanced Instruction activity](../reference/advanced-instruction-activity.md)**  
Display detailed instructions to guide end users through your playbook.
-   **[Checklist Task from Template activity](../reference/checklist-task-template-activity.md)**  
Prompt an agent to complete all items in a task checklist.
-   **[Checklist Task activity](../reference/checklist-task-activity.md)**  
Prompt an agent to complete all items in a task checklist.
-   **[Collect User Data activity](../reference/collect-user-data-activity.md)**  
Collects inputs from a user during a playbook run to use later in the playbook.
-   **[Create Record activity](../reference/create-record-activity.md)**  
Pause the playbook and prompt the end user to create a record in a form view. Use this activity to allow the end user to create a record. This activity requires you to configure the desired table for which record to create, and the desired form view that the end user will see when creating the record.
-   **[Create Child Case activity](../reference/create-child-case-activity.md)**  
Enable agents and fulfillers to create a child case during a playbook run.
-   **[Create Child Task activity](../reference/create-child-task-activity.md)**  
Enable agents and fulfillers to create a child task during a playbook run.
-   **[Docusign activities](../reference/pad-activities-docusign.md)**  
Enable agents and fulfillers to collect electronic signatures during a playbook run, via Workflow Data Fabric's Docusign spoke.
-   **[Guided Decision activity](../reference/guided-decision-activity.md)**  
Choose a decision tree from your Guided Decisions framework to step agents through how to proceed with a task.
-   **[Invoke PaCE activity](../reference/invoke-pace-policies.md)**  
Enable the Policy as Code Engine \(PaCE\) activity in Playbooks to develop playbook processes.
-   **[Microsoft Teams activities](../reference/pad-activities-ms-teams.md)**  
Enable agents and fulfillers to send direct messages and post in Microsoft Teams channels during a playbook run, via Workflow Data Fabric's Microsoft Teams spoke.
-   **[Request Multi-Level Approval activity](../reference/req-multi-lvl-approvals-activity.md)**  
Enable agents and fulfillers to submit an approval requests to first and second-level managers during a playbook run.
-   **[Request Ad Hoc Approval activity](../reference/request-adhoc-approval-activity.md)**  
Enable agents and fulfillers to specify which user\(s\) should complete approval request\(s\) during a playbook run.
-   **[Request Manager Approval activity](../reference/request-mgr-approval-activity.md)**  
Enable agents and fulfillers to submit an approval request to a manager during a playbook run.
-   **[Send Email activity](../reference/send-email-activity.md)**  
Create an email from previously gathered or generated data. Use this activity to send an email. This activity requires the playbook author to define who the email should be sent to, the subject, and the body. This activity surfaces the pre-defined content for the email to the end user so that the end user can confirm before sending the email.
-   **[Show Knowledge Article activity](../reference/show-knowledge-article-activity.md)**  
Display a knowledge article to end users.
-   **[Show List of Records activity](../reference/show-list-of-records-activity.md)**  
Display a list records that match a set of conditions.
-   **[Slack activities](../reference/pad-activities-slack.md)**  
Enable agents and fulfillers to send direct messages and post in Slack channels during a playbook run, via Workflow Data Fabric's Slack spoke.
-   **[Two Step Instruction activity](../reference/two-step-instruction-activity.md)**  
Display a different message to end users based on the current activity state. You can specify an initial state message, a skipped state message, and a completed state message.
-   **[Update Record activity](../reference/update-record-activity.md)**  
Update a record with the field values you specify.
-   **[View Approval Requests activity](../reference/view-approval-reqs-activity.md)**  
Display a list of approval requests from within Playbook Experience.
-   **[Wait For Condition activity](../reference/wait-for-condition-activity.md)**  
Pause the playbook until a record has field values that match a set of conditions.

**Parent Topic:**[Playbooks reference](../reference/process-automation-designer-reference.md)

