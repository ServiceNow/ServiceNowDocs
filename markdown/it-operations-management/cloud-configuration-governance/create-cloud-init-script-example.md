---
title: Example: Post-provision cloud script
description: This example shows a cloud script that runs after a user provisions a virtual machine.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Cloud scripts and cloud script templates, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Example: Post-provision cloud script

This example shows a cloud script that runs after a user provisions a virtual machine.

## Before you begin

-   Role required: cloud\_admin
-   OS resource profile that is mapped to an image template. The user provisions a resource using the profile. You must add [basic authentication credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r_BasicAuthCredentialsForm.md) to the image.
-   Compute resource profile that is mapped to a hardware type.

## About this task

In this example, you create a cloud init script, customize a resource block, and provision a VM from the Cloud User Portal.

## Procedure

1.  Create a cloud script template and a cloud script that refers to the template.

2.  Open the virtual server resource block, and then follow these steps:

    1.  Set the **Draft/Published** switch to **Draft**.

        ![Virtual Server](../image/virtual-server-rb.png)

    2.  On the **Operations** tab, select **Virtual Server Interface** from the **Interface** list.

        ![Virtual Server Interface](../image/virtual-server-interface.png)

    3.  In the **Operation** field, verify that these operations exist:

        -   **Block Until Ready**
        -   **Execute Script**: This operation tells the blueprint to run a script.
        ![Block Until Ready](../image/blockuntilready-operation.png)

        ![Execute Script operation](../image/execute-script-operation.png)

    4.  Click the **Input Parameters** tab to view the inputs for each operation.

    5.  On the **Steps** tab, add steps as needed.

    6.  For the **Script** parameter on each step, clear the **Script** check box and change the expression in the **Mapping** column to the following text: `$(CloudScript.scripts.scriptname)`, where `scriptname` is the name of the script, not the script template, that you created earlier.

        ![Script parameter](../image/script-parameters-input-parameters.png)

3.  Publish the virtual server resource block, and use it in a blueprint that in turn is published to a catalog item.

4.  Launch a new stack to provision a VM and specify the OS profile and Compute profile that you created as a prerequisite.


## Result

The Stack Status page runs through the **CreateNode**, **BlockUntilReady**, and **ExecuteShellScript** operations. The last operation kicked off the script you created.

