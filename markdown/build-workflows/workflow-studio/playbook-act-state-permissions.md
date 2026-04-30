---
title: Playbook activity state-mapping permissions
description: User permissions must be assigned to allow agents to complete or skip activities in playbook using activity state mapping.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Playbook activity state mapping, Stages and activities, Building playbooks, Use, Workflow Studio, Build workflows]
---

# Playbook activity state-mapping permissions

User permissions must be assigned to allow agents to complete or skip activities in playbook using activity state mapping.

**Can Complete** and **Can Skip** permissions in declarative action client conditions **\[sys\_declarative\_action\_assignment.list\]** are determined whenever an activity is fetched based on the following conditions:

-   **Experience Status Record** must be defined
-   Users must have write access on **Experience Status Record**
-   Activity State Mapping rule set must exist for **Experience Status Table**
-   User must have write access on **Experience Status Field** for that table
-   **Activity State to Experience Status** mapping rule must exist for that corresponding operation:

    |Playbook Activities|Activity State|
    |-------------------|--------------|
    |Can Complete|Complete|
    |Skip|Skipped|


If the permissions are not valid, users cannot perform that operation. The corresponding declarative actions that use the **Can Complete** and **Can Skip** client conditions will not display.

![Adding Can Complete or Can Skip client conditions to a declarative action](../../process-automation-designer/images/declarative-action-state-mapping-permissions.png)

**Note:** If a user does not have read access on the **Experience Status Field** of the **Experience Status Record**, the default activity state will be used instead. The default activity state is the state of the flow powering the activity.

**Parent Topic:**[Playbook activity state mapping](playbook-activity-state-mapping.md)

