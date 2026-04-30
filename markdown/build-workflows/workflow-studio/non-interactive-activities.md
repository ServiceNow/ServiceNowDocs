---
title: Non-Interactive activities
description: A non-interactive activity runs entirely behind-the-scenes on the ServiceNow AI Platform and doesn't require any user input.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Playbooks reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Non-Interactive activities

A non-interactive activity runs entirely behind-the-scenes on the ServiceNow AI Platform® and doesn't require any user input.

A non-interactive activity is an entirely automated operation on the ServiceNow AI Platform which doesn't require any user input to proceed to completion. Non-interactive activities still render in a playbook, but only display information to agents. Configure the activity inputs for an interactive activity so that the activity is a fully automated operation on the ServiceNow AI Platform.

When non-interactive activities run, they automatically proceed to completion or are skipped. For example, if your activity automatically updates the Assigned To user for a record, the Playbook card can display the newly updated Assigned To user's name to the playbook agent, but the card's status is automatically set to Complete.

![Non-interactive activity become a card.](../images/non-interactive-activity-overview.png "Non-interactive activities")

Non-interactive activities turn into activity cards that are collapsed and marked complete in a playbook. The playbook continues running without any input from the playbook agent.

To learn how to design a playbook with non-interactive activities, see [design an automated process](../task/design-automated-process.md).

-   **[Automated Create Record activity](../reference/automated-create-record-activity.md)**  
Create a record without pausing the playbook to ask for user input. When the activity runs, it immediately creates the record and continues to the next activity in the playbook. The record must meet server-side validation rules such as data policies, business rules and dictionary-defined mandatory fields but ignores UI policies.
-   **[Automated Send Email activity](../reference/automated-send-email-activity.md)**  
Create an email from previously gathered or generated data without pausing the playbook to ask for user input. When the activity runs, it immediately sends the email and continues to the next activity in the playbook.
-   **[Automated Update Record activity](../reference/automated-update-record-activity.md)**  
Update a record without pausing the playbook to ask for user input. When the activity runs, it immediately updates the record and continues to the next activity in the playbook. The record must meet server-side validation rules such as data policies, business rules and dictionary-defined mandatory fields but ignores UI policies.
-   **[Autocompleting User Form](../reference/autocompleting-user-form.md)**  
Display a form during runtime to collect input values for your playbook.
-   **[Look Up Records activity](../reference/look-up-records-activity.md)**  
Find system records that match a set of conditions.
-   **[Make a Decision-First Match activity](../reference/make-decision-first-match-activity.md)**  
Execute rules in a decision table. When this activity runs, it will immediately finish and continue the process execution. The activity returns the result of the first matching decision rule, based on the rank of the rules. To return results from all matching rules, add the decision table to a subflow.

**Parent Topic:**[Playbooks reference](../reference/process-automation-designer-reference.md)

