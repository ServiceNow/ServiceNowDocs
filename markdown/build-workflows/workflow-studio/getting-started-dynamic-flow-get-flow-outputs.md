---
title: Get started with Dynamic Flow and Get Flow Outputs
description: Create a sample flow that dynamically calls subflows for provisioning cloud services.Create a sample subflow template for provisioning cloud services.Create a sample subflow for provisioning cloud services from Jira.Create a sample subflow for provisioning cloud services from Salesforce.Create a sample flow to run your provisioning cloud services subflows.Test your sample flow for provisioning cloud services.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Building subflows, Use, Workflow Studio, Build workflows]
---

# Get started with Dynamic Flow and Get Flow Outputs

Create a sample flow that dynamically calls subflows for provisioning cloud services.

## Before you begin

Role required: flow\_designer or admin

## About this task

To understand how to use the Dynamic Flow and Get Flow Outputs flow logic together, the flow that you create in this task dynamically runs subflows that are related to provisioning cloud services. This flow does the following:

1.  Triggers when a Cloud Instance Provisioning Request record is created.
2.  Calls the appropriate subflow to create a Cloud Instance record.
3.  Gets an output from the dynamically called subflow and updates the Cloud Instance Provisioning Request record with the output's value.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **Studio**.

2.  On the Select Application screen, click **Create Application**.

3.  On the Guided App Creator welcome screen, click **Let's get started**.

4.  In the **Name** field, enter `Cloud Instance Provisioning` and then click **Create**.

5.  In the **Roles** field, enter `flow_designer` or `admin` and then click **Continue**.

6.  From the list of app formats, select **Classic** and then click **Continue**.

7.  Select **Create new table** &gt; **Create table from scratch** &gt; **Continue** to create two new tables for your application.

    -   Add the following fields for the first table and name the table `Cloud Instance`.

        |Field label|Field type|Reference|
        |-----------|----------|---------|
        |Owner|Reference|User \[sys\_user\]|
        |Instance Type|String|None|
        |Instance URL|URL|None|
        |Build Status|String|None|

    -   Add the following fields for the second table and name the table `Cloud Instance Provisioning Request`.

        |Field label|Field type|Reference|
        |-----------|----------|---------|
        |Requested Instance Type|String|None|
        |Requested by|Reference|User \[sys\_user\]|
        |Approval Status|String|None|
        |Approved Instance|URL|None|

8.  After creating both tables, click **Done with tables**.

9.  Select **Start** &gt; **Create** &gt; **Done with apps** to finish creating your application.


**Parent Topic:**[Building subflows](../concept/subflows.md)

## Create a subflow template

Create a sample subflow template for provisioning cloud services.

### Before you begin

Role required: flow\_designer or admin

### Procedure

1.  Under Business logic, process automation, and integrations, select **Go to Flow Designer**.

2.  In the Workflow Studio landing page main header, select **New** &gt; **New Subflow**.

3.  On the Subflow Properties screen, enter `TEMPLATE: Create Cloud Instance Record` in the **Name** field and then select **Submit**.

4.  Under Inputs &amp; Outputs, select the plus icon \(![Plus icon](../images/plus-icon-gray.png)\) to create two inputs for your subflow template.

    |Label|Type|
    |-----|----|
    |Requested by|Reference.User|
    |Requested Instance Type|String|

5.  Select the plus icon \(![Plus icon](../images/plus-icon-gray.png)\) to create one output for your subflow template.

    |Label|Type|
    |-----|----|
    |Instance URL|URL|

6.  Under your output, select **Done**.

7.  Select the add action, flow logic, or subflow to end of flow icon \(![Add action, flow logic, or subflow to end of flow icon](../images/plus-icon-gray.png)\) and then select **Action**.

8.  From the list of ServiceNow Core actions, select **Log**.

9.  In the data panel, drag the data pills for the `Requested by` and `Requested Instance Type` inputs you created earlier, and drop both of the pills into the **Message** field.

10. In the Subflow header, select **Save** and then select **Publish** to publish your subflow template.


## Create a subflow for Jira cloud instance provisioning requests

Create a sample subflow for provisioning cloud services from Jira.

### Before you begin

Role required: flow\_designer or admin

### Procedure

1.  In the Subflow header, select the more actions icon \(![More actions icon](../images/more-actions-menu-icon.png)\) and select **Copy subflow**.

2.  On the Copy Subflow screen, enter `Create Cloud Instance Record - Jira` in the **New Subflow Name** field, and then select **Copy**.

3.  Under the **Log** action, add a [Create Record action](../reference/create-record-flow-designer.md).

4.  In the **Table Name** field, select `Cloud Instance` and then fill in the following fields.

    |Field|Value|
    |-----|-----|
    |Owner|Select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and select **Subflow - Inputs** &gt; **Requested by**.|
    |Instance Type|Select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and select **Subflow - Inputs** &gt; **Requested Instance Type**.|
    |Instance URL|Enter `https://mycompany-`. Then, select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and select **Subflow - Inputs** &gt; **Requested by** &gt; **Name**. Finally, enter `.atlassian.net`|
    |Build Status|Enter `In Progress`.|

5.  Under the create record action, select **Add an Action, Flow Logic, or Subflow** &gt; **Flow Logic** &gt; **Assign Subflow Outputs**.

6.  Select the plus icon to add an output.

7.  For **Name**, select **Instance URL**.

8.  For **Data**, select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and then **2 - Create Record -** &gt; **Cloud Instance Record** &gt; **Instance URL**

9.  In the Subflow header, select **Save** and then **Publish** to publish the subflow.


## Create a subflow for Salesforce cloud instance provisioning requests

Create a sample subflow for provisioning cloud services from Salesforce.

### Before you begin

Role required: flow\_designer or admin

### Procedure

1.  In the Subflow header, select the more actions icon \(![More actions icon](../images/more-actions-menu-icon.png)\) and select **Copy subflow**.

2.  On the Copy Subflow screen, enter `Create Cloud Instance Record - Salesforce` in the **New Subflow Name** field, and then select **Copy**.

3.  Expand the **Create Cloud Instance Record** action and replace the `.atlassian.net` value for the **Instance URL** field with `.salesforce.com`

4.  In the Subflow header, select **Save**, accept the data change warning message, and then **Publish** to publish the subflow.


## Create a flow that runs your subflows dynamically

Create a sample flow to run your provisioning cloud services subflows.

### Before you begin

Role required: flow\_designer or admin

### Procedure

1.  Under the Workflow Studio header, select the **Create flow, subflow, or action**\(![Create flow, subflow, or action icon](../images/create-flow-subflow-or-action-icon.png)\) icon and select **Flow**.

2.  On the Flow Properties screen, enter `Process Cloud Instance Provisioning Request` in the **Name** field, and then select **Submit**.

3.  Under Trigger, select the plus icon ![Plus icon](../../../build/app-engine-studio/image/plus-icon.png)\) to add a trigger to your flow, and then fill out the following fields.

    |Field|Value|
    |-----|-----|
    |Trigger|Select **Created**.|
    |Table|Enter **Cloud Instance Provisioning Request \[x\_cloud\_instance\_p\_cloud\_instance\_provisioning\_request\]**.|

4.  Under Actions, select the plus icon ![Plus icon](../images/plus-icon-gray.png)and then select **Flow Logic** &gt; **Dynamic Flow**.

5.  Fill in the following fields.

    |Field|Value|
    |-----|-----|
    |Flow Template|Select **TEMPLATE: Create Cloud Instance Record**|
    |Flow|Enter `Create Cloud Instance Record -` and then select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and select **Trigger - Record Created** &gt; **Cloud Instance Provisioning Request Record** &gt; **Requested Instance Type**.|
    |Wait for completion|Enable this option to run your subflow dynamically first before other actions in your flow occur.|
    |Requested by|Select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and select **Trigger - Record Created** &gt; **Cloud Instance Provisioning Request Record** &gt; **Requested by**.|
    |Requested Instance Type|Select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and select **Trigger - Record Created** &gt; **Cloud Instance Provisioning Request Record** &gt; **Requested Instance Type**.|

6.  Under your **Dynamic Flow** flow logic, add the Get Flow Outputs flow logic, and then fill in the following fields.

7.  For **Flow Template**, select **TEMPLATE: Create Cloud Instance Record**

8.  For **Context**, select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and select **1 - Dynamic Flow -** &gt; **Context**.

9.  Under your **Get Flow Outputs** flow logic, select the plus icon \(![Plus icon](../images/plus-icon-gray.png)\) and then select **Action** &gt; **Update Record** to add an [Update Record action](../reference/update-record-flow-designer.md) to your flow.

10. Fill in the following fields.

    |Field| |
    |-----|---|
    |Record|Select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and select **Trigger - Record Created** &gt; **Cloud Instance Provisioning Request Record**.|
    |**Fields** &gt; **Approved Instance**|Select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and select **2 - Get Flow Outputs -** &gt; **Instance URL**.|
    |**Fields** &gt; **Approval Status**|Enter `Approved`.|

11. Select **Save**.


## Test your flow

Test your sample flow for provisioning cloud services.

### Before you begin

Role required: flow\_designer or admin

### Procedure

1.  In the Flow header, select **Test** to test your flow.

2.  On the Test Flow screen, select the Create new record \(![Create new record icon](../images/create-new-record-icon.png)\) icon to create a new record.

3.  For **Requested By**, select the Lookup using list icon \(![Lookup using list icon](../images/lookup-using-list-icon.png)\) and select any user from the list.

4.  For **Requested Instance Type**, enter either `Jira` or `Salesforce`.

    The value you enter determines which subflow runs dynamically at runtime. Entering `Jira` runs the **Create Cloud Instance Record - Jira** subflow, and entering `Salesforce` runs the **Create Cloud Instance Record - Salesforce**.

5.  Select **Submit**.

6.  Select **Run Test**, and when the flow finishes running, select **Your test has finished running. View the flow execution details.**

    Your flow runs successfully if the values in the State column for each step in your flow shows **Completed** and each step's runtime value populates appropriately.

7.  Select the tab for your **Process Cloud Provisioning Requests** flow and close the Test Flow modal.

8.  In the Flow header, select **Activate** to make your flow accessible within the Cloud Instance Provisioning [Application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=zurich&pubname=zurich-application-development&ft:locale=en-US).


### Result

When a user in your instance creates a new record in the Cloud Provisioning Request table, your Process Cloud Provisioning Requests flow runs automatically. This flow dynamically creates the proper Cloud Instance record that is based on the requested instance type. It also generates a cloud instance URL, which populates in the Cloud Instance Provisioning Request record.

