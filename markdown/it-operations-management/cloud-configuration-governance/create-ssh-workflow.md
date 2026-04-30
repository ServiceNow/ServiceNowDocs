---
title: Create an SSH workflow
description: Create the SSH workflow needed to power off the VM. Use the SSH custom activity that you already created.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Day 2 operations using workflows, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Create an SSH workflow

Create the SSH workflow needed to power off the VM. Use the SSH custom activity that you already created.

## Before you begin

-   Have an SSH custom activity already created
-   Role required: workflow designer or admin

## About this task

When you create a workflow, you associate it with a table and with an activity.

-   You can create the workflow on a table at the global-level or a table on the application-level. Use the global table to make the workflow available to use with all ServiceNow applications. Here, we use a table for the Cloud Provisioning and Governance, so this workflow will only be available to use with that application.
-   You can create the workflow from the Workflow Editor or from the Activity Designer. Here, the Activity Designer is used.

## Procedure

1.  From the Activity Designer, select the **Workflows** tab at the right, then click the **+** \(plus sign\) to add a new workflow.

2.  In the New Workflow window, perform these steps:

    1.  Enter a unique name for the workflow.

    2.  From the **Table** drop-down, select the table to use.

        Search for and use the **Virtual Machine instance cmdb\_ci\_vm\_instance** because we intend to use the workflow to power off a VM.

    3.  Click **Submit**.

3.  When the workflow displays in the canvas, perform these steps:

    1.  Delete the connection line between the start point and end point of the workflow.

    2.  Right-click the more info canvas and select **Edit Inputs**.

    3.  Create the following inputs:

        **Note:** Take the input names from the Column field, not from the Label field. If the workflow is associated with a global-level table, the input name in the Column field is prefixed with u\_, for example, u\_ipaddress. Here, the table is application-level, so it needs no prefix.

        |Type|Label|Column \(automatically added\)|Max Length|
        |----|-----|------------------------------|----------|
        |String|IPAddress|ipaddress|100|
        |String|CredentialTag|credentialtag|100|

    4.  Click **Submit**.

4.  Right-click the canvas and select **Add Custom Activity**.

5.  In the Versions window, search for and select the activity you created earlier in [Create the SSH custom activity](create-ssh-custom-activity.md).

6.  In the New Activity window for that activity \(Workflow Activity New record \[Diagrammer view\]\), perform these steps:

    1.  Enter a name for the activity.

    2.  In the **Host** field, type the input mapping that the activity expects.

        That is, the IP address of the host: **$\{workflow.inputs.u\_ipaddress\}**.

        Use this expression to the IP address:

        $\(Script:CMPVMUtils.getReachableIp\[arg=$\(Stack.items\[Virtual Server\].attributes\[sys\_id\]\)\]\)

    3.  In the Command field, type **shutdown -h now**

    4.  In the Credential tag field, type **$\{workflow.inputs.u\_credentialtag\}**

        Use this expression to get the credential tag:

        $\(Script:CMPVMUtils.getCredentialAlias\[arg=$\{Stack.items\[Virtual Server\].attributes\[sys\_id\]\}\]\)

    5.  Click **Submit**.

        The activity displays in the workflow canvas.

7.  Right-click the canvas, and select **Add Core Activity** to add a run script activity.

8.  In the Workflow Activity Definitions window, search for and select **Run Script**.

9.  In the New Activity: Run Script window, perform these steps:

    1.  Type a name for the activity.

    2.  Cut and paste a script \(appropriate for your environment\) in the **Script** field.

        This script updates the state of the VM after it is shut down.

        Example script:

        ```
        if ( gs.nil(data.get(3).error)) {
                            current.state = 'off';
                            current.setWorkflow(false);
                            current.update();
        }
        
        ```

    3.  Click **Submit**.

10. In the canvas, connect the connectors between the Begin point, the activity, the Run Script, and the End point.

11. Click **Publish** to make the workflow available.

12. Validate the workflow by using the workflow validation.

    **Note:** The system does not recommend the use of current.update\(\). This can be ignored.


