---
title: Create a custom action to generate an array of strings from a list of records
description: Generate an array of strings from a list of User Role records. Learn how to use a Script step to iterate through a list of records.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Script support for complex data, Complex data, Build actions, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Create a custom action to generate an array of strings from a list of records

Generate an array of strings from a list of User Role records. Learn how to use a Script step to iterate through a list of records.

## Before you begin

Role required: admin of flow\_designer

## About this task

Use this example to see demonstrations of these operations and steps.

-   Create an action input for a Role record.
-   Look up a maximum of three User Role records that have the Role action input.
-   Configure a Script step to process a list of User Role records.
-   Create a script input variable containing the list of User Role records.
-   Write script that creates an empty users array.
-   Write script that iterates through the list of User Role records.
-   Write script that populates the users array with the current user field value.
-   Create script output variables for the users array and child user string.
-   Output the generated users array of strings as a data pill.
-   Test the action with three sample users.

## Procedure

1.  Create an application to store your work.

    You can use App Engine Studio to plan, create, and deploy applications. For more information about building a custom application, see Building apps in App Engine Studio.

    For example, create an application called `My Application`.

2.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

3.  On the homepage, select **Actions**.

4.  Select **New** &gt; **Action**

    The system displays the Action Properties dialog.

5.  Enter these sample values.

    |Field|Value|
    |-----|-----|
    |Name|Create Users With Role Array Of Strings|
    |Application|Global|
    |Accessible From|All application scopes|

    **Note:** If you created an application to store and deploy your custom action, use that application instead of global.

6.  Select **Build action**.

    The system displays the Workflow Studio interface.

7.  From the Action Outline, select **Inputs** &gt; **Create Input**

    The system displays a new action input.

8.  Configure the action input with these values.

    ![Create an action input that stores a role record.](../images/array-strings-config-inputs.png)

    |Field|Value|
    |-----|-----|
    |Label|Role|
    |Type|Reference.Role \[Reference.sys\_user\_role\]|
    |Mandatory|True|

9.  From the Action Outline, select **Add a new step**.

    The system displays a list of available steps.

10. Select **Look Up Records**

11. Configure the step with these values.

    ![Configure the Look Up Records step condition to use the role input variable.](../images/array-strings-config-look-up-records-step.png)

<table id="table_cvp_l5p_lhb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Table

</td><td>

User Role \[sys\_user\_has\_role\]

</td></tr><tr><td>

Conditions

</td><td>

\[Role\]\[is\]\[action-&gt;Role\]**Note:** Select the Role data pill from the Input Variables.

</td></tr><tr><td>

Order by

</td><td>

Role

</td></tr><tr><td>

Sort Type

</td><td>

a to z

</td></tr><tr><td>

Max Results

</td><td>

3

</td></tr></tbody>
</table>    **Note:** This example limits the **Max Results** setting to three records just for demonstration purposes.

12. From the Action Outline, select **Add a new step**.

    The system displays a list of available steps.

13. Select **Script**.

14. From the Input Variables section, select **Create Variable**.

15. Configure the input variable with these values.

    ![Configure the Script step input variable to use the User Role records data pill from the Look Up Records step.](../images/array-strings-config-script-step-input-variable.png)

<table id="table_uby_5zp_lhb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

userRoleRecords

</td></tr><tr><td>

Value

</td><td>

\[step-&gt;Look Up Records step-&gt;User Role records\]**Note:** Select the User Role records data pill from the Look Up Records step.

</td></tr></tbody>
</table>    **Note:** You can select the **User Role records** data pill from the data panel or from the Data Pill Picker button.

16. For **Script**, enter the following text.

    ```
    (function execute(inputs, outputs) {
      //Create an empty array
      var usersArray = [];
      var i = 0;
      //Iterate through the list of User Role records
      while(inputs.userRoleRecords.next()) {
        //Query User Role records for user field value
        var user = inputs.userRoleRecords.getDisplayValue('user');
        //Add current user name to array
        usersArray[i] = user;
        i += 1;
      }
      outputs.users = usersArray;
    })(inputs, outputs);
    ```

17. From Output Variables, select **Create Variable**.

18. Configure the output variable with these values.

    ![Create an array of strings called users. Within the array create a string variable called user.](../images/array-strings-config-script-step-output-variable.png)

    |Label|Name|Type|Mandatory|
    |-----|----|----|---------|
    |users|users|Array.String|True|

19. Expand the users Array.String, and rename the child string to `user`.

20. Configure the child item with these values.

    |Label|Name|Type|Mandatory|
    |-----|----|----|---------|
    |user|user|String|False|

21. From the Action Outline, select **Outputs** &gt; **Create Output**.

22. Configure the Action Output with these values.

    ![Create an action output called users to store an array of strings.](../images/array-strings-config-outputs.png)

    |Label|Name|Type|Mandatory|
    |-----|----|----|---------|
    |users|users|Array.String|True|

23. Expand the users Array.String, and rename the child string to `user`.

24. Configure the child item with these values.

    |Label|Name|Type|Mandatory|
    |-----|----|----|---------|
    |user|user|String|False|

25. Select **Exit Edit Mode**.

    The System displays the output fields you created.

26. For **users**, select **\[step-&gt;Script step-&gt;users\]**.

    ![Configure the action output variable to use the users data pill from the Script step.](../images/array-strings-config-outputs-users.png)

    **Note:** You can select the Script step **users** data pill from the data panel or from the Data Pill Picker button.

27. Click **Save**.

28. Select **Test**.

    The system displays the Test Action dialog.

29. Enter the following test value:

    ![Select the admin role to test your action.](../images/array-strings-test-action-role.png)

    |Input|Value|
    |-----|-----|
    |Role|admin|

30. Select **Run Test**.

    The system runs the action with the test values provided.

31. Select **Your test has finished running. View the Action execution details.**

    The system displays the action execution details.

32. Review the runtime value for the action Output data.

    ![Execution details page listing three user names in the users array.](../images/array-strings-execution-details.png)

    The system displays output data in JSON format.

    For this example, the users array contains three users who have the admin role.

    ```
    {
        "users": [
            "System Administrator",
            "Rob Phillips",
            "Fred Luddy"
        ]
    }
    
    ```


## Result

You have a custom action that looks up the Users who have a given role and converts those users into an array of user name strings.

## What to do next

Customize this action to use your own logic.

**Parent Topic:**[Script support for complex data](../concept/script-support-complex-data.md)

