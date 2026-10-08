---
title: Apply runtime permissions for a stage
description: Add permission sets to one stage to give the stage different runtime access from the rest of the playbook.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/override-runtime-permissions-stage.html
release: brazil
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Runtime permissions, Managing playbook permissions, Configure, Playbooks, Workflow Studio, Build workflows]
---

# Apply runtime permissions for a stage

Add permission sets to one stage to give the stage different runtime access from the rest of the playbook.

## Before you begin

Role required: playbook.admin, pd\_author

## About this task

By default, anyone who has read or write access to a parent record has access to a stage. Restrict permissions at the stage level when one stage needs access rules that the playbook as a whole doesn't. A stage that handles sensitive data can require a role that the rest of the playbook doesn't require.

Permission sets you add at stage level must also have read access at playbook level. A user who meets the stage criteria but has no playbook-level access can't read the stage. Where a stage has no override, the playbook-level permissions apply.

## Procedure

1.  Navigate to **All** &gt; **Workflow Studio** &gt; **Playbooks**.

2.  Open the playbook that you want to work on.

3.  On the diagram view, select the stage you want to restrict.

4.  Select **Additional runtime permissions**.

    \[Omitted image "pb-run-perm-stage.png"\] Alt text: Screenshot showing the Additional runtime permissions tab.

5.  Review the inherited permissions.

6.  Add permissions to an operation and select the source.

    1.  Select **Add permission set** to restrict an operation.

        You can restrict access to the stage at the **Read the stage**, **Add optional activities**, **Restart the stage**, and **Restart the activity** operational level.

    2.  Grant the permission set by **User**, **User group**, **Roles**, or a **User criteria** record.

        \[Omitted image "pb-run-perm-stage2.png"\] Alt text: Screenshot showing the Add permission set button and the methods to choose from.

    3.  Select the Add permission set confirmation \[Omitted image "Check.png"\] Alt text: Green check mark icon.

        \[Omitted image "pb-run-perm-stage3.png"\] Alt text: Screenshot showing the Add permission set confirm action.

    4.  Select **Add permission set** for the same operation to add more permissions.

        Permissions added to one operation combine with OR, so any one of them satisfies it.

7.  Select **Add permission set** next to another operation to add permissions to a different operation.

8.  Select **Save and close** to save your work on the playbook runtime permissions.


## Result

The permissions you set on the stage further narrow the playbook-level permissions for that stage. Activities within the stage inherit the stage permissions.

## What to do next

Reactivate the playbook. Permission changes affect new executions after reactivation, not existing executions.

**Parent Topic:**[Runtime permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/runtime-permissions-playbooks.md)

**Related topics**  


[Configure runtime permissions for a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/configure-runtime-permissions-playbook.md)

