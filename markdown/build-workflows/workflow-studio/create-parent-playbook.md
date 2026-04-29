---
title: Create a parent playbook to host a nestable child playbook
description: After you have created a nestable child playbook, then you can create a parent playbook to host the child playbook.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Nested Playbooks, Design Playbook Experience, Playbooks, Workflow Studio, Build workflows]
---

# Create a parent playbook to host a nestable child playbook

After you have created a nestable child playbook, then you can create a parent playbook to host the child playbook.

## Before you begin

Role required: admin, playbook.admin, or playbook.write

## Procedure

1.  Navigate to **All** &gt; **Workflow Studio**.

2.  The **Playbooks** pill should be selected, if it isn't, select it.

3.  In the workspace window, select **New** &gt; **Playbook**.

4.  In the **New Playbook** window:

    1.  Make sure that **Standard playbook** is selected as the **Type**.
    2.  Enter a **Playbook name**.
    3.  Enter a **Description** that helps you identify the playbook.
    4.  Select an **Application** scope.
    5.  Select **Record driven** for **Execution type**.
    6.  Select a **Parent table**.
    7.  Select **Build playbook**.
5.  In the Diagram view of the parent playbook you just created, select the plus sign between **Start** and **End**, and then select **Create a stage to put your activities in**.

6.  In the center of the stage you just added, select the plus sign, and then select the **Add a playbook** icon:

    ![Image of Playbook stage user interface showing the "Add a playbook" option.](../images/add-nested-playbook-icon.png)

7.  In the **Add playbook** dialog box, search for and select the nestable child playbook you just created in the previous step.

8.  Complete the **Child properties** options:

    |Property|Description|
    |--------|-----------|
    |Label|Provide a name for your child activity.|
    |Description|Type a description of the activity.|
    |Activity definition|Select the icon \(![Launch web UI icon](../images/launch-web-UI.png)\) to open the web UI of the instance to define the activity for your child playbook.|
    |Schedule|Select when the child playbook activity starts or whether it starts after specific activities occur.|

9.  Select **Show additional options** to configure the following options:

<table id="table_chp_grk_23c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display order

</td><td>

Order in which the activities display.

</td></tr><tr><td>

Start with delay

</td><td>

This option enables you to delay the start of the child playbook activities. Define conditions that determine when the child playbook activities start.

</td></tr><tr><td>

Restart rules

</td><td>

Select when the child playbook activity restarts. Select from:

 -   Skip on restart
-   Run always
-   Skip on first run


</td></tr></tbody>
</table>10. Select **Test**.

    Selecting this option enables you to test the child playbook process on a sample record to make sure that the process is configured correctly. When the testing completes successfully, select **Done** to close the **Test your process** dialog box.

11. Select **Activate** to make sure that your child playbook is ready to process records.

12. Select **Save and close**.


