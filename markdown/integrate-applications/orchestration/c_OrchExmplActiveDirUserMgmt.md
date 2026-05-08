---
title: Active Directory automation example
description: A set of six Orchestration Active Directory activities enables organizations to automate their on-boarding/off-boarding processes with auditable, self-documenting workflows that save time and eliminate mistakes.An organization plans to make their ServiceNow instance the single system of record for user account data and wants to update Active Directory with the latest changes.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Orchestration examples, Classic Orchestration, Workflow Data Fabric]
---

# Active Directory automation example

A set of six Orchestration Active Directory activities enables organizations to automate their on-boarding/off-boarding processes with auditable, self-documenting workflows that save time and eliminate mistakes.

The activities in the Active Directory activity pack are designed to manage user accounts and reset user passwords. The following activities cover the most common use cases administrators encounter when managing Active Directory user accounts:

-   Create AD User Account
-   Update AD User Account
-   Remove AD User Account
-   Disable AD User Account
-   Query AD
-   Reset AD User Password.

These activities share a common design, have complementary functionality, and share a common set of parameters. They can be used singly or together to create consistent workflows for provisioning and de-provisioning user accounts.

**Parent Topic:**[Orchestration examples](c_OrchestrationExamples.md)

## Update Active Directory with Orchestration

An organization plans to make their ServiceNow instance the single system of record for user account data and wants to update Active Directory with the latest changes.

### About this task

The solution is to create an Orchestration workflow that pushes changes from the ServiceNow user record down to the Active Directory to create a new user record or update an existing record. This is accomplished by creating an Orchestration workflow that can create and update records in Active Directory based on the data in the ServiceNow User \[sys\_user\] table.

**Note:** This example workflow assumes that ServiceNow is configured for LDAP and an LDAP server is configured to accept the new user accounts. The Active Directory user management activities are not dependent on LDAP, but the presence of LDAP makes this example workflow much easier. You must provide the domain controller's IP address to the workflow, either by hardcoding it, adding another workflow input, or using a script to look it up from the CMDB.

### Procedure

1.  Navigate to **All** &gt; **Workflow** &gt; **Workflow Editor**.

2.  In the **Workflow** tab, click the **+** icon to create a new workflow using these variables:

    -   Name: Sync AD User
    -   Table: Global \[global\]
3.  Click **Submit**.

    A basic workflow with a Begin and End point appears on the canvas.

4.  Click the menu icon in the upper left corner of the canvas and select **Edit Inputs** from the context menu.

    ![Editing workflow inputs](../image/WorkflowEditInputs.png "Editing workflow inputs")

5.  In the Workflow Inputs form, click **New** in the **Variables** record list, and create a new variable, using the fields in the table.

    |Field|Value|
    |-----|-----|
    |Type|Reference|
    |Label|User|
    |Column name|u\_user|
    |Reference Specification &gt; Reference|User \(sys\_user\)|

6.  Click **Submit**.

7.  In the **Custom** tab, expand **Custom Activities** &gt; **Active Directory**.

8.  Drag and drop the Update AD Object activity onto the transition line between the Begin and End points of the new workflow.

    This action automatically links the activity with the end point and opens the Workflow Activity property form.

9.  Complete the form using the fields in the table.

<table id="table_qxs_p3r_gq"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a logical name such as **Update user data**.

</td></tr><tr><td>

Domain controller

</td><td>

The ServiceNow LDAP integration adds a reference to the LDAP server to which the user's account is linked. To identify the LDAP server, enter the following statement:`${workflow.inputs.u_user.ldap_server.server_url}`

</td></tr><tr><td>

Type

</td><td>

Type of AD object. In this case, the type is **User**, which is the default.

</td></tr><tr><td>

Object name

</td><td>

This example assumes that the ServiceNow user name matches the Active Directory sAMAccountName. Enter the following:`${workflow.inputs.u_user.user_name}`

</td></tr><tr><td>

Object data

</td><td>

Updates the user's account in Active Directory, if the user exists. In this example, the user's title is updated:`{"title" : "QA"}`

</td></tr></tbody>
</table>10. Click **Submit**.

    The workflow looks like this:

    ![Updating AD user](../image/WorkflowExample1.png "Updating an AD user")

11. Attach both activity outcomes \(Success and Failure\) to the end point.

    At this point, the workflow takes a ServiceNow user record as input and updates the First Name, Last Name, and Title of the corresponding Active Directory account. If the account does not exist in Active Directory, the workflow fails.

    **Note:** In a normal workflow, some type of alternate action is desirable upon failure. For example, you might send an Email and SMS notifications if the workflow failed to update the record.

12. To prevent the workflow from failing, add a Create AD Object activity to the transition lines between Begin and the Update AD Object activity.

13. Complete the Workflow Activity property form using the fields in the table.

    |Field|Value|
    |-----|-----|
    |Name|Enter a logical name such as **Create user data**.|
    |Domain controller|Same as for the update activity. `${workflow.inputs.u_user.ldap_server.server_url}`|
    |Ou|The organizational unit to which this object belongs. For the purpose of this example, you can enter **OU=HQ,OU=Managed Objects**|
    |Object name|Same as for the update activity. `${workflow.inputs.u_user.user_name}`|
    |Object data|Creates an account with only the user name in it. For the purpose of this example, you can enter `{"givenName" : "${workflow.inputs.u_user.first_name}", "SN" : "${workflow.inputs.u_user.last_name}" }`|

14. Click **Submit**.

15. Connect the Failure outcome of the Create AD Object activity to End.

    For this example, we are ignoring errors. The workflow now looks like this:

    ![Creating an AD user](../image/WorkflowExample2.png "Creating an AD user")

    This procedure builds a simple workflow that creates a bare-bones Active Directory account consisting of a user name only. The workflow then updates that account with additional information provided by the ServiceNow User \[sys\_user\] table. However, we do not want to execute the Create AD Object activity if the user account already exists. The workflow needs to query Active Directory for matching user records and then branch the workflow based on the results of the query. If an account already exists, then the workflow should update the account. If the account does not exist, then the workflow should create the account in Active Directory.

16. Drag and drop the Query AD activity onto the transition between Begin and Create AD Object.

17. Complete the Workflow Activity property form using the fields in the table.

<table id="table_ncz_3pr_gq"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a logical name such as **Search for existing account**.

</td></tr><tr><td>

Domain controller

</td><td>

`${workflow.inputs.u_user.ldap_server.server_url}`

</td></tr><tr><td>

Properties

</td><td>

A comma-separated list of Active Directory properties to return. For example, givenName, SN, title. If the parameter field is blank, then all properties are returned. In this workflow, we leave the field blank.

</td></tr><tr><td>

Search filter

</td><td>

An LDAP filter string that defines the search parameters. Use any valid LDAP filtering criteria. To find user accounts matching the input record, we use: `(samaccountname=${workflow.inputs.u_user.user_name})`

</td></tr></tbody>
</table>18. Click **Submit**.

19. Connect the Failure outcome for the query activity to the End point.

    Remember that we are ignoring errors in this workflow.

20. Connect the Success outcome of the query activity to the Update AD Object activity.

    The workflow now looks like this:

    ![Querying AD for user accounts](../image/WorkflowExample3.png "Querying AD for user accounts")

    The Query AD activity returns its results as a JSON string in the workflow [data bus](../../../administer/orchestration-activity-designer/concept/c_OrchestrationDatabus.md#). This JSON string is always an array of objects. Each object corresponds to an Active Directory entry that matched the query. Our workflow should branch, whether that array is empty or not.

21. Drag a standard If activity from the Conditions folder in the **Core** tab and drop it onto the transition between Query AD and Update AD Object.

22. Complete the Workflow Activity properties form using the fields in the table.

<table id="table_ib2_qqr_gq"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a logical name such as **Account exists**.

</td></tr><tr><td>

Advanced

</td><td>

Select this check box to open the Script field.

</td></tr><tr><td>

Script

</td><td>

For the If activity to work correctly, we must return a **yes** or **no** in the answer variable \(var\) which corresponds to the Yes and No outcomes of the query activity. Line 1 converts the Query AD results from a JSON string into a Javascript array called queryResults. Line 2 checks the length of that array. If the array is more than 0, a match to the account was found, and we set our answer to yes. Otherwise, the answer is no.`var queryResults=new JSON().decode(data.get(5).output);`

 `answer = ( queryResults.length>0 ? 'yes' : 'no' );`

</td></tr></tbody>
</table>    **Note:** The expression `data.get(5)` in this script identifies the Query AD output in the Databus by order number, since it was the fifth activity added to the workflow.

    ![Query AD outputs in the Databus](../image/WorkflowExampleOrderNum.png "Query AD outputs in the Databus")

23. Click **Submit**.

24. In the canvas, create a transition from the Yes outcome of the If activity to the Update AD Object activity.

25. Create a transition from the No outcome of the If activity to the Create AD Object activity.

    This is the final step. This workflow will query Active Directory to determine if an account already exists. If an account exists, the workflow updates that account. If an account does not exist, the workflow creates the account and then updates the Active Directory with the configured user data set.

    ![Creating the conditional paths](../image/WorkflowExample4.png "Creating the conditional paths")


