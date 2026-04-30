---
title: Build automation
description: Use the requirement diagram to build an automation.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Requirement Intake Diagram, Requirement Intake Diagram, Workflow Data Fabric]
---

# Build automation

Use the requirement diagram to build an automation.

## Before you begin

Role required: sn\_ac.automation\_technical\_user, playbook.write, playbook.activity\_def\_read, connection\_admin, or cmdb\_read

## Procedure

1.  Navigate to **Workspaces** &gt; **Automation Center Workspace**.

2.  On the **Lists** tab \(![List icon](../../automation-center/images/autocenter-list-icon.png)\), under **Build**, select **All Automation Requests**.

3.  Select an automation request for which you want to build an automation.

4.  Select **Build Automation**.

    The **Select Instance** dialog box is displayed.

    **Important:** The **Build Automation** button is available only when the automation request is in the **In progress** state.

5.  Select an instance where you want to create an automation.

    **Note:** The instances that are set up will be available in the list. For more information, see [Set up connections and credentials](set-connection-alias.md).

6.  Select **Continue**.

    The **Build automation** window is displayed.

    ![Build Automation](../images/build-auto.png)

7.  On the form, fill in the details.

<table id="table_xsg_4cv_jcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select how you want to build the automation

</td><td>

There are two options:-   **Build using diagram**: Building automation using diagram creates an end-to-end automation flow, transforming each diagram step into a corresponding automation placeholder step.
-   **Build manually**: Building automation manually does not use the diagram. It lets you create a fresh automation.


</td></tr><tr><td>

Automation name

</td><td>

The name of the automation.

</td></tr><tr><td>

Description

</td><td>

The description of the automation.

</td></tr><tr><td>

Application

</td><td>

The application scope where this automation is created.

</td></tr></tbody>
</table>8.  Select **Build Automation**.

    The requirement diagram is visible from the Workflow Studio.

    For more information about editing or creating diagrams, see [Create a playbook](https://www.servicenow.com/docs/access?context=create-process-definition&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

    At this point you must create a trigger to activate the automation.

    **Note:** When the new automation request is created, an automation with the same name is created and mapped to the automation request.


