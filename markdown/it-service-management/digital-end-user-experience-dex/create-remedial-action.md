---
title: Create a remedial action
description: Create your custom remedial actions from Check Definitions to resolve end-point related issues using Playbook.
locale: en-US
release: xanadu
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [DEX remedial actions, Configuring Digital End-User Experience, Digital End-User Experience, IT Service Management]
---

# Create a remedial action

Create your custom remedial actions from Check Definitions to resolve end-point related issues using Playbook.

## Before you begin

Role required: admin, dex\_admin

**Note:** To learn more about different remedial actions, see .

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Services Operations Workspace** &gt; **DEX Administration**.

2.  Select **Create new** in the Create Remedial Actions section.

3.  Select **Create new** or **Map to an existing remedial action** according to the requirement.

    |Option|Description|
    |------|-----------|
    |**Create net new action**|Select this option to create a net new remedial action from a Check Definition.|
    |**Map to an existing remedial action**|Select this option when a remedial action exists for a particular operating system \(OS\) and you want to map the same action to another OS by choosing a Check Definition.|

4.  Enter a name in **Remedial action name** if you choose to create a net new action.

5.  If you choose to map to an existing remedial action, select from the existing remedial actions.

6.  Add a short description.

7.  Select the roles for those who can execute the remedial action.

    This option is available for sn\_dex.engineer and sn\_dex.service\_desk\_user.

8.  Select the origin of remediation.

    This setting indicates where the remedial action should be executed from the device health page or alert details.

9.  Select the **Remedial Action** check box if it’s available for bulk remediation.

10. Select the operating system of the impacted device from the drop-down menu.

11. Select the base Check Definition for this remedial action and select **Save**.

    **Note:**

    -   Confirm that the selected Check Definition is applicable for the selected OS.
    -   Depending on the Check Definition selected, the related Check Definition parameters are listed.

