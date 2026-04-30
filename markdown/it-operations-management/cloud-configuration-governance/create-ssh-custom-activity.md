---
title: Create the SSH custom activity
description: Create an SSH custom activity so you can use it in your workflow.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Day 2 operations using workflows, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Create the SSH custom activity

Create an SSH custom activity so you can use it in your workflow.

## Before you begin

Role required: cloud designer or admin

## Procedure

1.  Navigate to **All** &gt; **Admin Portal** &gt; **Workflows** &gt; **Workflow Editor**.

2.  Click the **Custom** tab, then click + \(plus sign\) to create a new custom activity.

3.  From the list of types of activities, choose **SSH**.

    ![Choose SSH as the custom activity type](../image/custom-tab-choose-ssh.png)

4.  When the Activity Designer opens with the General tab displayed, enter a unique name for the activity and then click **Continue**.

5.  In the Inputs tab, add the input variables with the following steps, then click **Continue**:

    1.  In the Input table, click the **+ in a circle** to create a new input variable.

    2.  Click to the right of ABC in the **Name** column, and type the input name.

        Inputs vary according to the object to be impacted. Here, we're creating an activity to stop a VM, so the inputs reflect the values needed to accomplish that action.

        The **Type** and **Mandatory** columns populate automatically according to input you enter.

    3.  Create a new input object for each input in the following table, then click **Continue**:

        |Input variable|Type|Mandatory|
        |--------------|----|---------|
        |Host|String|No|
        |Command|String|No|
        |CredentialTag|String|No|

6.  On the Execution Command tab, perform the following:

    1.  Click and drag the input variables from the left to the template fields at the right.

        This step creates the expressions that will be used.

    2.  Check the **Must Sudo** box so that you can later log in to the virtual server.

    3.  Click **Continue**.

        ![Add inputs to the Execution Command](../image/execution-command-tab.png)

7.  On the Outputs tab, add the output variables with the following steps:

    1.  In the Output table, click the **+ in a circle** to create a new output variable.

    2.  Click to the right of ABC in the **Name** column, and type the output name.

        The output variables reflect the possible outcomes when the workflow attempts to SSH to the VM. The **Type** column populates automatically.

        |Outputs|Type|
        |-------|----|
        |error|String|
        |output|String|

    3.  Click and drag the **error** variable to the Variable name field in the Parsing rules table.

    4.  In the Parsing rule for error dialog, in the Parsing source drop-down, select the appropriate source; in this case, executionResult.errorMessages.

    5.  Repeat for the output variable, selecting executionResult.output as the Parsing source, then click **Submit**.

        ![Outputs display in Parsing rules](../image/outputs-display-in-parsing-rules.png)

    6.  Click **Continue**.

        Conditions are optional.

    7.  Click **Save**, then click **Publish** to make the activity available to use in the workflow.


## What to do next

You have now created a custom activity that exists as a container until you add in the input mappings to it. The mappings tell the activity where the information it needs is coming from. You enter the input mappings during the workflow creation procedure. See [Create an SSH workflow](create-ssh-workflow.md).

