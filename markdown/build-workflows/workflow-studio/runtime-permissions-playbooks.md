---
title: Runtime permissions
description: Runtime permissions restrict who can read, restart, cancel, and add optional activities to a running playbook.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/runtime-permissions-playbooks.html
release: brazil
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Managing playbook permissions, Configure, Playbooks, Workflow Studio, Build workflows]
---

# Runtime permissions

Runtime permissions restrict who can read, restart, cancel, and add optional activities to a running playbook.

By default, access to a running playbook follows the parent record. Users who can read the parent record can read the playbook, and users who can write to the parent record can restart it.

This default grants wider access than some processes require. For example, every agent who can read a case can also read every stage of every playbook running on that case.

Runtime permissions let a playbook author add further restrictions during playbook design. Configure permissions at the playbook level, then override them at the stage level where different access is needed.

**Note:** Runtime permissions only narrow access. The default parent record requirements always remain in effect and can't be removed. Any permissions you add are additional conditions, so a playbook with runtime permissions configured is always more restrictive than one without.

## How conditions combine

Default permissions are required and combine with AND logic, meaning all conditions must be satisfied. Permissions that you add to an operation combine with OR logic, meaning any one condition is sufficient.

If a playbook author adds two roles to the Read operation, users need read access on the parent record AND membership in the first role OR the second role.

## Operations you can restrict

|Operation|Configurable at|Governs|
|---------|---------------|-------|
|Read|Playbook, stage|Viewing the playbook or stage at runtime|
|Restart|Playbook, stage|Restarting the playbook or stage|
|Cancel|Playbook|Canceling a running playbook|
|Add optional activity|Stage|Adding an optional activity to a stage at runtime|

## Grouping settings

Grouping settings apply a permission across an entire level rather than to each item individually.

-   Restart for all stages in a playbook
-   Add optional activity for all stages in a playbook
-   Restart for all activities in a playbook or a stage

## Permission sources

|Source|Grants the permission to|
|------|------------------------|
|User|A named user|
|User role|Users holding the specified role|
|User group|Members of the specified group|
|User criteria|Users matching the specified user criteria record|

The two record access sources can point at any record, not only the parent record of the playbook.

## Overrides

Permissions configured at a lower level override those at the level above. A stage overrides the playbook. Where no override exists, the permissions from the level above apply.

Use an override when one part of a playbook requires different access from the rest. For example, a stage that handles payment details can require a role that the playbook as a whole doesn't.

-   **[Configure runtime permissions for a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/configure-runtime-permissions-playbook.md)**  
Add permission sets to a playbook to restrict who can view and act on it at runtime.
-   **[Apply runtime permissions for a stage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/override-runtime-permissions-stage.md)**  
Add permission sets to one stage to give the stage different runtime access from the rest of the playbook.

**Parent Topic:**[Managing playbook permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/playbook-permissions.md)

