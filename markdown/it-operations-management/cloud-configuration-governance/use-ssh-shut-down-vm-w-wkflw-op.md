---
title: Use SSH to shut down a VM using workflow type operation
description: Use SSH to remotely shut down a VM using a workflow type operation. Follow this use case to step through all of the tasks required to accomplish this type of shutdown.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Day 2 operations using workflows, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Use SSH to shut down a VM using workflow type operation

Use SSH to remotely shut down a VM using a workflow type operation. Follow this use case to step through all of the tasks required to accomplish this type of shutdown.

## Before you begin

Role required: workflow designer or sn\_cmp.cloud\_admin

## Procedure

1.  To create the SSH custom activity, follow these steps:

    1.  Navigate to **Admin Portal** &gt; **Workflows** &gt; **Workflow Editor**.

    2.  Click the **Custom** tab, and then click **+** \(plus sign\) to create a new custom activity.

    3.  From the list of types of activities, choose **SSH**.

        ![Choose SSH as the custom activity type](../image/custom-tab-choose-ssh.png)

    4.  The Activity Designer opens with the General tab displayed

        Enter a unique name for the activity, then click **Continue**.

    5.  In the Inputs tab, add the input variables with the following steps, then click **Continue**:

    6.  In the Input table, click the **+ in a circle** to create a new input variable.

    7.  Click to the right of ABC in the **Name** column, and type the input name.

        Inputs vary according to the object to be impacted. You can stop an activity to stop a VM, so the inputs reflect the values needed to accomplish that action.

        The **Type** and **Mandatory** columns populate automatically according to input you enter.

    8.  Create a new input object for each input in the following table, and then click **Continue**:

        |Input variable|Type|Mandatory|
        |--------------|----|---------|
        |Host|String|No|
        |Command|String|No|
        |CredentialTag|String|No|

    9.  On the Execution Command tab, perform the following:

    10. In the Output table, click the **+ in a circle** to create a new output variable.

    11. Click to the right of ABC in the **Name** column, and type the output name.

        The output variables reflect the possible outcomes when the workflow attempts to SSH to the VM. The **Type** column populates automatically.

        |Outputs|Type|
        |-------|----|
        |error|String|
        |output|String|

    12. Click and drag the **error** variable to the Variable name field in the Parsing rules table.

    13. In the Parsing rule for error dialog, in the Parsing source drop-down, select the appropriate source; in this case, executionResult.errorMessages.

    14. Repeat for the output variable, selecting executionResult.output as the Parsing source, then click **Submit**.

        ![Outputs display in Parsing rules](../image/outputs-display-in-parsing-rules.png)

    15. Click **Continue**.

        Conditions are optional.

    16. Click **Save**, and then click **Publish** to make the activity available to use in the workflow.

2.  To create the SSH workflow needed to power off the VM, follow theses steps:

    When you create a workflow, you associate it with a table and with an activity.

    -   You can create the workflow on a table at the global-level or a table on the application-level. Use the global table to make the workflow available to use with all ServiceNow applications. Here, we use a table for the Cloud Provisioning and Governance, so this workflow will only be available to use with that application.
    -   You can create the workflow from the Workflow Editor or from the Activity Designer. Here, the Activity Designer is used.
    1.  From the Activity Designer, select the **Workflows** tab at the right, then click the **+** \(plus sign\) to add a new workflow.

    2.  In the New Workflow window, enter a unique name for the workflow.

    3.  From the **Table** drop-down, select the table to use.

        Search for and use the **Virtual Machine instance cmdb\_ci\_vm\_instance** to use the workflow to power off a VM.

    4.  Click **Submit**.

    5.  When the workflow displays in the canvas, delete the connection line between the start point and end point of the workflow.

    6.  Delete the connection line between the start point and end point of the workflow.

    7.  Right-click the more info canvas and select **Edit Inputs**.

    8.  Create the following inputs:

        **Note:** Take the input names from the Column field, not from the Label field. If the workflow is associated with a global-level table, the input name in the Column field is prefixed with u\_, for example, u\_ipaddress. Here, the table is application-level, so it needs no prefix.

        |Type|Label|Column \(automatically added\)|Max Length|
        |----|-----|------------------------------|----------|
        |String|IPAddress|ipaddress|100|
        |String|CredentialTag|credentialtag|100|

    9.  Click **Submit**.

    10. Right-click the canvas and select **Add Custom Activity**.

    11. In the Versions window, search for and select the activity you created initially in this use case.

    12. In the New Activity window for that activity \(Workflow Activity New record \[Diagrammer view\]\), enter a name for the activity.

    13. In the **Host** field, type the input mapping that the activity expects.

        Here, that is the IP address of the host: **$\{workflow.inputs.u\_ipaddress\}**. Use this expression to get the IP Address:

        $\(Script:CMPVMUtils.getReachableIp\[arg=$\(Stack.items\[Virtual Server\].attributes\[sys\_id\]\)\]\)

    14. In the Command field, type **shutdown -h now**

    15. In the Credential tag field, type **$\{workflow.inputs.u\_credentialtag\}**

        Use this expression to get the credential tag:

        **$\(Script:CMPVMUtils.getCredentialAlias\[arg=$\{Stack.items\[Virtual Server\].attributes\[sys\_id\]\}\]\)**

    16. Click **Submit**.

        The activity displays in the workflow canvas.

    17. Right-click the canvas, and select **Add Core Activity** to add a run script activity.

    18. In the Workflow Activity Definitions window, search for and select **Run Script**.

    19. In the New Activity: Run Script window, type a name for the activity.

    20. Cut and paste a script \(appropriate for your environment\) in the **Script** field.

        This script updates the state of the VM after it is shut down.

        Example script:

        ```
        if ( gs.nil(data.get(3).error)) {
                            current.state = 'off';
                            current.setWorkflow(false);
                            current.update();
        }
        
        ```

    21. Click **Submit**.

    22. In the canvas, connect the connectors between the Begin point, the activity, the Run Script, and the End point.

    23. Validate the workflow by using the workflow validation.

        **Note:** The system does not recommend the use of **current.update\(\)**. This can be ignored.

3.  To add the operation to a resource block, following these steps:

    You can select from the existing operations in a resource block to work with your workflow or you can create a custom operation.

    1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Resource Blocks**.

    2.  Select a resource block, for example **Virtual Server**.

    3.  Move the state of the resource block from **Published** to **Draft** to make it editable.

    4.  Select the **Operations** tab, and then from the Interface drop-down field, select an interface that is available to the user.

        The default interface is **Virtual Server Interface**.

    5.  Click **+** to the right of the Operation field, then in the Add Operation dialog, enter a meaningful and unique name.

    6.  Select an operation from the Operation Type drop-down.

    7.  Select **Public** from the Access Type field.

    8.  Fill in the form, and then click **Submit**.

<table id="table_b5p_hk1_bgb"><tbody><tr><td>

Operation Type

</td><td>

Select the operation to perform.

</td></tr><tr><td>

Access Type

</td><td>

For the user to see the operation at the Resources level during provisioning, select **Public**. Operations set to **Private** are not visible during provisioning.

</td></tr></tbody>
</table>        The operation is available on the resource when you select the resource for your workflow.

    9.  To add a resource operation step to invoke the workflow, still in the Operations tab, click **Steps** &gt; **Add Step**.

        To enable the workflow to be exported as part of the update sets, you must create an extension interface and add the new operation. See [Extend Cloud Provisioning and Governance resource blocks with an override operation](extend-cloud-management-entities.md) for details.

    10. In the Add Operation Steps popup, select **Invoke Workflow**for **Operation Type**.

    11. Select the **Workflow** from the list of workflows that you created.

        The system can filter the list using tags. To add a tag:

        1.  Navigate to **System Properties**.
        2.  Locate and select the system property **sn\_cmp.workflow\_tag\_filter**.
        3.  Edit the property. Add a tag or comma-separated list of tags.
        4.  Click **Save**.
    12. To filter the workflows:

        1.  On the workflow table, open the workflow.
        2.  Click **Add Tag**.
        3.  Enter the value that you provided earlier in the property **sn\_cmp.workflow\_tag\_filter**
        4.  Click **Enter** to add the value as a tag to the workflow. The new step appears after the software generates the new Day 2 Operation Catalog.
    13. Workflows can exist that are created on tables other than global.

        You can add a workflow created on such a table. To execute operations on this type of workflow, you need the sys\_id of the record in which the workflow is executing to create the current record. So when the designer adds a workflow that is on table other than global, the system creates a **wf\_current** parameter in the operation input parameter. You can then write an expression to map the sys\_id of the resource in which the operation is executing. Once this is completed, the designer can use the ‘current’ key word in workflow scripts.

        To add the workflow:

        1.  After you create the step, the system adds the workflow inputs to the operation input parameters. You can then provide the mapping for these parameters, if needed.
        2.  Click the **Generate Catalog** button to create the catalog item for the operation.
        3.  After the catalog generates, you can add from the load and field change rules to the catalog items.
    14. Set the resource block to the **Published** state to make the workflow available in the Cloud User Portal.

4.  To execute the operation from the User Portal, follow these steps:

    1.  Provision a simple AWS VM from the portal.

    2.  After the VM provisioning completes, navigate to the stack &gt; VM Resource.

    3.  In the Select Resource Operation option, select the custom stop activity you created earlier in this use case, then click OK.

        The operation executes after the RITM is created and the VM state changes in the AWS console.

    4.  Navigate to **Operate** &gt; **Trails** to view the trail logs and trace the operation steps.

5.  To troubleshoot, if needed, follow these steps:

    1.  Use the request item \(RITM\) and navigate to the RootCauseAnalysis Dashboard.

        The RITM has the link to the workflow context of the currently executed operation.

    2.  Check for these common errors:

<table id="table_e3l_5gc_2gb"><thead><tr><th>

Symptom

</th><th>

Error message

</th></tr></thead><tbody><tr><td>

VM shuts down but there has been an issue with the SSH connection

</td><td>

"Error; job finished with status ERROR: Problem in SSH session, job aborted: Connection unexpectedly closed by SSH server: \\n",

</td></tr><tr><td>

VM is already shutdown / not able to reach the VM

</td><td>

"Cannot connect, status is TCP\_CONNECTION\_FAILURE. Timed out while waiting for TCP to connect to 10.198.252.224:22: \\n",**Note:** Confirm that the IP address of the VM in the wf\_context is the appropriate address. The VM might have been already shutdown. Confirm the IP address is accessible.

</td></tr><tr><td>

Root access unavailable

</td><td>

"Failed to issue method call: Access denied\\nMust be root.\\nExit status: 1\\n\\n",**Note:** Confirm that the **Must Sudo** box is checked in the SSH activity at the beginning of this use case.

</td></tr></tbody>
</table>
