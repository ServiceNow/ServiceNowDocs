---
title: Create UI actions for your service with Universal Task
description: Create UI actions for your service so that agents can create universal tasks.
locale: en-US
release: australia
product: Universal Task
classification: universal-task
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring your service, Setting up and configuring Universal Task, Universal Task, Employee Service Management]
---

# Create UI actions for your service with Universal Task

Create UI actions for your service so that agents can create universal tasks.

## Before you begin

Role required: admin

Administrators and users with the ui\_action\_admin role can define UI actions. The UI actions must be configured for both the ServiceNow AI Platform form and the Agent Workspace form.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **UI Actions**.

2.  In the UI actions list, click **New**.

3.  Enter the name of the UI action.

    For example, enter the name as `Assign Task`.

4.  Select the service-specific table that Universal Task is being configured for.

    For example, select the Universal Request \[universal\_request\] table for placing the Assign Task UI action on the Universal Task form view or workspace.

    **Note:** For any new UI action, ensure that you always select the appropriate service table.

5.  Clear the **Show insert** check box.

    If the **Show insert** check box remains checked, the UI action to create a task is displayed even when the main ticket is being created.

6.  Select the **Form Button** check box.

7.  In the **Script** field, enter the following script.

    ```
    var gr = new GlideRecord("sn_uni_task_universal_task");
    gr.initialize();
    gr.setValue("parent",current.sys_id);
    action.openGlideRecord(gr);
    action.setReturnURL(current);
    ```

    **Important:** This script belongs in the Script field \(server-side\) of the UI Action. Do not copy it into the **Workspace Client Script** field unless you want additional client-side behavior in Workspace.

8.  On the **Workspace** tab, select the **Workspace Form Button** check box.

9.  On the form, fill in the fields.

    For more information on fields and descriptions, see Create a UI action.

10. Click **Submit**.


**Parent Topic:**[Configuring your service for Universal Task](../concept/config-service-for-ut.md)

**Previous topic:**[Assign Universal Task admin role](assign-ut-admin-role.md)

**Next topic:**[Add a Universal Task related list](create-relatedlist-ur.md)

