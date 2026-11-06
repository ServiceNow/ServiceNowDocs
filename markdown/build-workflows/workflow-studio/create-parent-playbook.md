---
title: Create a parent playbook to host a nestable child playbook
description: After you have created a nestable child playbook, then you can create a parent playbook to host the child playbook.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/build-workflows/workflow-studio/create-parent-playbook.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-10-16"
reading_time_minutes: 2
breadcrumb: [Nested Playbooks, Playbooks patterns, Playbooks, Workflow Studio, Build workflows]
---

# Create a parent playbook to host a nestable child playbook

After you have created a nestable child playbook, then you can create a parent playbook to host the child playbook.

## Before you begin

Role required: admin, playbook.admin, or playbook.write

## Procedure

1.  Navigate to **All** &gt; **Workflow Studio** &gt; **Playbooks**.

2.  In the workspace window, select **New** &gt; **Playbook**.

3.  In the **New Playbook** window:

    1.  Make sure that **Standard playbook** is selected as the **Type**.
    2.  Enter a **Playbook name**.
    3.  Enter a **Description** that helps you identify the playbook.
    4.  Select an **Application** scope.
    5.  Select **Record driven** for **Execution type**.
    6.  Select a **Parent table**.
    7.  Select **Build playbook**.
4.  In the Diagram view of the parent playbook you just created, select the plus sign between **Start** and **End**, and then select **Create a stage to put your activities in**.

5.  In the center of the stage you just added, select the plus sign, and then select the **Add a playbook** icon:

    \[Omitted image "add-nested-playbook-icon.png"\] Alt text: Image of Playbook stage user interface showing the "Add a playbook" option.

6.  In the **Add playbook** dialog box, search for and select the nestable child playbook you just created in the previous step.

    The child playbook is added to the stage as a child playbook activity that shows the name of the child playbook.

7.  Complete the **Child properties** options:

    |Property|Description|
    |--------|-----------|
    |Label|Provide a name for your child activity.|
    |Description|Type a description of the activity.|
    |Playbook|Select the Open playbook icon \[Omitted image "launch-web-UI.png"\] Alt text: Launch web UI icon to open the web UI of the instance to define the activity for your child playbook.|
    |Schedule|Select when the child playbook activity starts or whether it starts after specific activities occur.|

8.  Select **Show additional options** to configure the following options:

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
</table>9.  Select the **Automation** tab of your nested playbook activity and map a value to each input of the child playbook.

    Select a source for each input:

    -   A fixed value.
    -   A data pill for the trigger record or the parent table.
    -   A data pill for the output of an earlier activity.
10. Where you want to use a value that the child playbook returns, select the data pill picker icon \[Omitted image "data-pill-picker-icon.png"\], and then select the child output.

    You can use child outputs in the inputs of later activities, in experience properties, and in conditions. Only activities that start before the target activity appear in the data pill picker. The child returns only the outputs that are declared on its **Inputs &amp; Outputs** tab and set by a **Set Playbook Outputs** activity. To see which outputs a child returns, open the properties of the child playbook.

11. Select **Test**.

    Test the parent playbook process on a sample record to make sure that the process is configured correctly. When the child returns more than one true or false output, test each combination of values. For example, test all true, some true, and none true, to confirm that the outputs reach the parent and that the branches rejoin as expected. When the testing completes successfully, select **Done** to close the **Test your process** dialog box.

12. Select **Activate** to make sure that your parent playbook is ready to process records.

13. Select **Save and close**.


