---
title: Use credentials with SSH workflows
description: Add an SSH workflow with a credentials tag.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Day 2 operations using workflows, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Use credentials with SSH workflows

Add an SSH workflow with a credentials tag.

## Before you begin

-   Orchestration must be installed.
-   Role required: Cloud designer or sn\_cmp.cloud\_admin

## About this task

You can use an expression to get the Credential alias tag. See [Create an SSH activity](https://www.servicenow.com/docs/access?context=t_CreateAnSSHActivity&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for instructions.

This example uses a VM provisioned on an AWS LDC datacenter.

## Procedure

1.  In the Cloud User Portal, click **Launch a Stack** and then select the AWS VM.

2.  On the General Info tab, enter a unique and meaningful **Stack Name**, select **AWS Datacenter** for the **Location**, and then click **Next**.

3.  On the Provision tab, enter a **Virtual Server Node Name** \(the name can be the same as the stack name\) and then click **Submit**.

    The Cloud Activities page displays the VM that you requested and the status of your request. The Request Status section displays Deployment Successful when complete.

4.  In your instance, view the workflow:

    1.  Filter for workflow and then click **Workflow Editor**.

    2.  At the right of the workflow list window, filter in the Workflows tab and select the workflow to work with.

        When the workflow appears in the canvas, you can see the Execute SSH Command activity pill in the workflow.

5.  To edit the activities in the workflow, click the workflow properties icon \(circle containing an i\) and perform the following:

    1.  On the **Custom** tab at the right, go to **Custom Activities** &gt; **Global** and double-click the activity to modify.

        When the new activity opens in the Activity Designer, you can use the form to create a reusable orchestration activity.

    2.  To change from the Cloud Provisioning and Governance application to the Global application to edit the record, click "**here**" in the menu bar.

        The Global application makes the activities available across the entire platform.

6.  Edit the fields in each of the following activity tabs.

7.  Click **Continue** to move to the next tab.

8.  Follow the field description below to populate **Activity** details.

<table id="table_bck_zzr_yfb"><thead><tr><th>

Activity tab

</th><th>

Field descriptions

</th></tr></thead><tbody><tr><td>

General

</td><td>

Unique name for the activity

</td></tr><tr><td>

Inputs

</td><td>

Values for the host, type, and whether the activity is mandatory

</td></tr><tr><td>

Execution Command

</td><td>

To form the command to be executed, drag inputs from the list to the form. Available inputs:

-   **Host**, which is the IP address of the VM to connect to.
-   **Command**, which is any script or command single line to be run on the VM.
-   **Credential tag**, which is the alias for the sys\_id of the VM. You can either enter the credential tag manually or provide an expression in the resource script, which then auto-populates the Credential tag field. Script: **$\(Script:CMPVMUtils.getCredentialAlias\[arg=$\[parameter.resourceID\}\]\)**


</td></tr><tr><td>

Output

</td><td>

Name of each output, and the type of each output, for example, string

</td></tr><tr><td>

Conditions

</td><td>

Any required conditions. Conditions are optional

</td></tr></tbody>
</table>
