---
title: Playbook activity state mapping
description: Use playbook activity state mapping to override the status of a playbook card.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/playbook-activity-state-mapping.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Stages and activities, Understanding the playbook components, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Playbook activity state mapping

Use playbook activity state mapping to override the status of a playbook card.

A playbook card's state comes from the Activity State by default. Activity states come from the Sub Flow or Flow Action powering the activity.

Activity Definition authors can specify a records to provide the status shown in playbook cards. This record is referred to as an **Experience Status Record**. It is specified within an Activity Definition's experience properties.

\[Omitted image "activity-definition-tables-records.png"\] Alt text: Tables and records for an activity definition

Any record from any table can be used as an Experience Status Record. Default activity definitions use **sys\_flow\_data** records as their Experience Status Record.

\[Omitted image "playbook-activity-card-states.png"\] Alt text: Playbook activity states shown in card view

## Default Activity States

|Status|Flow State|
|------|----------|
|Pending|Flow has not started|
|Ready|Flow is|
|In Progress|Flow is running|
|Complete|Flow has finished|
|Skipped|Flow was skipped due to conditions|
|Error|Flow encountered an error|
|Canceled|Flow was canceled|

Activity states are used in the following:

-   Declarative Action conditions
-   Activity Override conditions
-   Animations
-   Card visual experience

## Exceptions

Business logic doesn't always align one-to-one with the flow. The following are examples of exceptions:

-   An agent clicks **Skip** on an instructional card. The flow displays as complete, but the business logic is skipped.
-   A flow may never complete if a task is waiting for input from an agent to restart a loop. The associated task is effectively complete in this state.

-   **[Playbook activity state-mapping rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/playbook-activity-state-mapping-rules.md)**  
Map playbook activity states to states from the given experience record.
-   **[Playbook activity state-mapping permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/playbook-act-state-permissions.md)**  
User permissions must be assigned to allow agents to complete or skip activities in playbook using activity state mapping.

**Parent Topic:**[Stages and activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/process-automation-designer-lanes-activities.md)

