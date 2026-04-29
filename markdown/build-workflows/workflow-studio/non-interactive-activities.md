---
title: Non-Interactive activities
description: A non-interactive activity runs entirely behind-the-scenes on the ServiceNow AI Platform and doesn't require any user input.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Playbooks reference, Playbooks, Workflow Studio, Build workflows]
---

# Non-Interactive activities

A non-interactive activity runs entirely behind-the-scenes on the ServiceNow AI Platform® and doesn't require any user input.

A non-interactive activity is an entirely automated operation on the ServiceNow AI Platform which doesn't require any user input to proceed to completion. Non-interactive activities still render in a playbook, but only display information to agents. Configure the activity inputs for an interactive activity so that the activity is a fully automated operation on the ServiceNow AI Platform.

When non-interactive activities run, they automatically proceed to completion or are skipped. For example, if your activity automatically updates the Assigned To user for a record, the Playbook card can display the newly updated Assigned To user's name to the playbook agent, but the card's status is automatically set to Complete.

![Non-interactive activity become a card.](../images/non-interactive-activity-overview.png "Non-interactive activities")

Non-interactive activities turn into activity cards that are collapsed and marked complete in a playbook. The playbook continues running without any input from the playbook agent.

To learn how to design a playbook with non-interactive activities, see [design an automated process](../task/design-automated-process.md).

