---
title: Playbook activity state mapping
description: Use playbook activity state mapping to override the status of a playbook card.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/build-workflows/workflow-studio/playbook-activity-state-mapping.html
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Stages and activities, Building playbooks, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Playbook activity state mapping

Use playbook activity state mapping to override the status of a playbook card.

## Overview

A playbook card's state comes from the Activity State by default. Activity states come from the Sub Flow or Flow Action powering the activity.

Activity Definition authors can specify a record to provide the status shown in playbook cards. This record is referred to as an **Experience Status Record**. It is specified within an Activity Definition's experience properties.\[Omitted image "experience-status-record.png"\] Alt text: Experience status record tab

Any record from any table can be used as an Experience Status Record. Default activity definitions use **sys\_flow\_data** records as their Experience Status Record.

\[Omitted image "playbook-activity-states-card.png"\] Alt text: Playbook activity states shown in card view

## Default Activity States

|Status|Flow State|
|------|----------|
|Pending|Flow has not started|
|In Progress|Flow is running|
|Complete|Flow has finished|
|Skipped|Flow was skipped due to conditions|
|Error|Flow encountered an error|

Activity states are used in the following:

-   Declarative Action conditions
-   Activity Override conditions
-   Animations
-   Card visual experience

## Exceptions

Business logic doesn't always align one-to-one with the flow. The following are examples of exceptions:

-   An agent clicks **Skip** on an instructional card. The flow displays as complete, but the business logic is skipped.
-   An agent clicks **Restart** on a completed instructional card. The flow does not restart the flow, just update the **Flow Data** record.
-   A flow may never complete if a task is waiting for input from an agent to restart a loop. The associated task is effectively complete in this state.

-   **[Playbook activity state-mapping rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/playbook-activity-state-mapping-rules.md)**  
Use activity state-mapping rules to control which activity state is shown in a card for a given experience status record.
-   **[Playbook activity state-mapping permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/playbook-act-state-permissions.md)**  
User permissions must be assigned to allow agents to complete, skip, or restart activities in playbook using activity state mapping.

**Parent Topic:**[Stages and activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/process-automation-designer-lanes-activities.md)

**Related topics**  


[Add and configure a stage in a playbook]()

[Activity definitions]()

[Add and configure an activity in a playbook]()

[Automation Assets]()

[Start with delay input properties]()

[Optional activities]()

[Decision activities]()

[Questionnaire activity]()

[Parallel branches]()

[Add dynamic inputs to an activity]()

