---
title: Using the activity stream within a playbook
description: Add comments or notes, and view communication and task history for a parent or associated record using the activity stream. The activity stream is available only on cards where an administrator has configured it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/build-workflows/workflow-studio/activity-stream-in-playbook.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-10-15"
reading_time_minutes: 1
breadcrumb: [Running Playbook Experience, Playbooks, Workflow Studio, Build workflows]
---

# Using the activity stream within a playbook

Add comments or notes, and view communication and task history for a parent or associated record using the activity stream. The activity stream is available only on cards where an administrator has configured it.

An administrator makes the activity stream available on a playbook card by creating an action assignment. The render mode selected for that action determines how agents open the stream: as a button on the card, as an icon in the card header, or as an item in the card header drop-down list.

An administrator can also set conditions on the action, so that the activity stream appears only for specific tables, form views, or workspaces. If no action assignment applies to a card, the activity stream isn't available on it.

## What the activity stream shows

The history displayed depends on the level at which the action is configured. Playbook actions and stage actions display the history of the parent record, such as the case or incident that the playbook runs on. Activity actions display the history of the record associated with that activity.

The stream records work notes, comments, emails, and field changes against that record, including updates made by automated activities and AI agents. Each update is attributed to the user or agent who made it.

## Playbook activity stream examples

To open the activity stream within a playbook, select **View activity** on the card, or select **View History** from the card header drop-down list, depending on how the action was configured.

\[Omitted image "view-activity-card.png"\] Alt text: Playbook card displaying a View activity button.

\[Omitted image "playbook-view-history.png"\] Alt text: Playbook card displaying a View History item in the card header drop-down list.

## Activity stream modal

View tabs for comments and work notes related to a parent or associated record. You can use the **Compose** text box to post new comments or work notes.

\[Omitted image "playbook-activity-stream-modal.png"\] Alt text: Activity stream modal displayed within a playbook.

You can view previous activity by scrolling down to the **Activity** section.

**Parent Topic:**[Running Playbook Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/playbook-agents-and-fulfillers.md)

