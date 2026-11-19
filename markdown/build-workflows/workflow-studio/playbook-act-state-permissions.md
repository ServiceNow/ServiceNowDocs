---
title: Playbook activity state-mapping permissions
description: User permissions must be assigned to allow agents to complete, skip, or restart activities in playbook using activity state mapping.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/build-workflows/workflow-studio/playbook-act-state-permissions.html
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Playbook activity state mapping, Stages and activities, Building playbooks, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Playbook activity state-mapping permissions

User permissions must be assigned to allow agents to complete, skip, or restart activities in playbook using activity state mapping.

**Can Complete**, **Can Skip**, and **Can Restart** permissions are determined whenever an activity is fetched based on the following conditions:

-   **Experience Status Record** must be defined
-   Users must have write access on **Experience Status Record**
-   Activity State Mapping rule set must exist for **Experience Status Table**
-   User must have write access on **Experience Status Field** for that table
-   **Activity State to Experience Status** mapping rule must exist for that corresponding operation:

    |Playbook Activities|Activity State|
    |-------------------|--------------|
    |Can Complete|Complete|
    |Skip|Skipped|
    |Restart|In Progress|


If the permissions are not valid, users cannot perform that operation. The corresponding declarative actions that use the **Can Complete**, **Can Skip**, and **Can Restart** client conditions will not display.

**Note:** If a user does not have read access on the **Experience Status Field** of the **Experience Status Record**, the default activity state will be used instead. The default activity state is the state of the flow powering the activity.

**Parent Topic:**[Playbook activity state mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/playbook-activity-state-mapping.md)

