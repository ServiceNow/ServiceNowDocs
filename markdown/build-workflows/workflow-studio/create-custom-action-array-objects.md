---
title: Create a custom action to generate an array of objects from a list of records
description: Generate an array of objects from a list of User records. Learn how to use a Script step to iterate through a list of records.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Script support for complex data, Complex data, Building actions, Use, Workflow Studio, Build workflows]
---

# Create a custom action to generate an array of objects from a list of records

Generate an array of objects from a list of User records. Learn how to use a Script step to iterate through a list of records.

## Before you begin

Role required: admin of flow\_designer

## About this task

Use this example to see demonstrations of these operations and steps.

-   Create an action input for a Department record.
-   Look up a maximum of three User records for the Department action input.
-   Configure a Script step to process a list of User records.
-   Create a script input variable containing the list of User records.
-   Write script that creates an empty contacts array.
-   Write script that iterates through the list of User records.
-   Write script that creates a contact object and maps User record field values to the contact object.
-   Write script that populates the contacts array with the current contact object.
-   Create script output variables for the contacts array and child contact object.
-   Save the contact object as a template.
-   Output the generated contacts array of objects as a data pill.
-   Test the action with a sample department.

## Procedure

1.  Create an application to store your work.

    You can use App Engine Studio to plan, create, and deploy applications. For more information about building a custom application, see [Building apps in App Engine Studio](https://www.servicenow.com/docs/access?context=aes-app-creation&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

    For example, create an application called `My Application`.

2.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

3.  On the homepage, select **Actions**.

4.  Select **New** &gt; **Action**

    The system displays the Action Properties dialog.

5.  Enter these sample values.

    |Field|Value|
    |-----|-----|
    |Name|Create Contacts Array Of Objects|
    |Application|Global|
    |Accessible From|All application scopes|

    **Note:** If you created an application to store and deploy your custom action, use that application instead of global.

6.  Select **Build action**.

    The system displays the Workflow Studio interface.

7.  From the Action Outline, select **Inputs** &gt; **Create Input**

    The system displays a new action input.

8.  Configure the action input with these values.

    ![Create an action input that stores a department record.](../images/array-objects-config-inputs.png)

    |Field|Value|
    |-----|-----|
    |Label|Department|
    |Type|Reference.Department \[Reference.cmn\_department\]|
    |Mandatory|True|

9.  From the Action Outline, select **Add a new step**.

    The system displays a list of available steps.

10. Select **Look Up Records**

11. Configure the step with these values.

    ![Configure the Look Up Records step condition to use the department input variable.](../images/array-objects-config-look-up-records-step.png)

<table id="table_cvp_l5p_lhb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Table

</td><td>

User \[sys\_user\]

</td></tr><tr><td>

Conditions

</td><td>

\[Department\]\[is\]\[action-&gt;Department\]**Note:** Select the Department data pill from the Input Variables.

</td></tr><tr><td>

Order by

</td><td>

Name

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

    ![Configure the Script step input variable to use the User records data pill from the Look Up Records step.](../images/array-objects-config-script-step-variable.png)

<table id="table_uby_5zp_lhb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

userRecords

</td></tr><tr><td>

Value

</td><td>

\[step-&gt;Look Up Records step-&gt;User Records\]**Note:** Select the User records data pill from the Look Up Records step.

</td></tr></tbody>
</table>    **Note:** You can select the **User records** data pill from the data panel or from the Data Pill Picker button.

16. For **Script**, enter the following text.

    ```
    (function execute(inputs, outputs) {
      //Create an empty array
      var contactsArray = [];
      var i = 0;
      //Iterate through the list of User records
      while(inputs.userRecords.next()) {
        //Create an empty object for each iteration
        var contactObject = {};
        //Query User records to assign object values
        contactObject.first_name = inputs.userRecords.getValue('first_name');
        contactObject.last_name = inputs.userRecords.getValue('last_name');
        contactObject.email_address = inputs.userRecords.getValue('email');
        //Add current object to array
        contactsArray[i] = contactObject;
        i += 1;
      }
      outputs.contacts = contactsArray;
    })(inputs, outputs);
    ```

17. From Output Variables, select **Create Variable**.

18. Configure the output variable with these values.

    ![Create an array of objects called contacts. Within the array create an object called contact. Within contact object create three strings variables for first name, last name, and email address.](../images/array-objects-config-script-step-output-variables.png)

    |Label|Name|Type|Mandatory|
    |-----|----|----|---------|
    |contacts|contacts|Array.Object|True|

19. Expand the contacts Array.Object, and rename the child object to `contact`.

20. From the row for the contact object, select the **Add Child Item** icon ![](../images/icon-add-child-item.png).

21. Configure the child item with these values.

    |Label|Name|Type|Mandatory|
    |-----|----|----|---------|
    |first name|first\_name|String|True|

22. From the row for the contact object, select the **Add Child Item** icon ![](../images/icon-add-child-item.png).

23. Configure the child item with these values.

    |Label|Name|Type|Mandatory|
    |-----|----|----|---------|
    |last name|last\_name|String|True|

24. From the row for the contact object, select the **Add Child Item** icon ![](../images/icon-add-child-item.png).

25. Configure the child item with these values.

    |Label|Name|Type|Mandatory|
    |-----|----|----|---------|
    |email address|email\_address|String|True|

26. From the row for the contact Object, select **Toggle Advanced Inputs**.

27. From the Advanced Options, select **Save As Template**.

    The system displays the Save As Template dialog.

28. For **Enter a Name**, enter `contact`.

    ![Save the object template with the name contact.](../images/array-objects-config-script-step-output-variable-template.png)

29. Click **Save**.

30. From the Action Outline, select **Outputs** &gt; **Create Output**.

31. Configure the Action Output with these values.

    ![Create an action output called contacts to store an array of objects.](../images/array-objects-config-outputs.png)

    |Label|Name|Type|Mandatory|
    |-----|----|----|---------|
    |contacts|contacts|Array.Object|True|

32. Expand the contacts Array.Object.

33. From the row for the contact Object, select **Toggle Advanced Inputs**.

34. From the Advanced Options, select **Structure** &gt; **Start from Template**.

    The system displays **Template**.

35. For **Template**, select the template you previously saved.

    For example, select **Global: contact**.

36. Select **Exit Edit Mode**.

    The System displays the output fields you created.

37. For **contacts**, select **\[step-&gt;Script step-&gt;contacts\]**.

    ![Configure the action output variable to use the contacts data pill from the Script step.](../images/array-objects-config-outputs-contacts.png)

    **Note:** You can select the Script step **contacts** data pill from the data panel or from the Data Pill Picker button.

38. Click **Save**.

39. Select **Test**.

    The system displays the Test Action dialog.

40. Enter the following test value:

    ![Select the Development department to test your action.](../images/array-objects-test-action-department.png)

    |Input|Value|
    |-----|-----|
    |Department|Development|

41. Select **Run Test**.

    The system runs the action with the test values provided.

42. Select **Your test has finished running. View the Action execution details.**

    The system displays the action execution details.

43. Review the runtime value for the action Output data.

    ![Execution details page for the test results of your custom action.](../images/array-objects-execution-details-page.png)

    Although the execution details display the output data as a JSON formatted string, the actual output data type is an array of objects. If you need a string version of your output, you can convert the object into a string using the JSON class. For more information about converting a JSON object into a string, see [Scoped JSON - stringify\(Object jsonObject\)](https://www.servicenow.com/docs/access?context=JSONScopedAPI&version=zurich&pubname=zurich-api-reference&section=JSONScoped-stringify_O&ft:locale=en-US).

    For this example, the contacts object contains an array of contact objects with first name, last name, and email information for three users in the Development department.

    ```
    {
        "contacts": 
            "contact": [
                {
                    "email_address": "allyson.gillispie@example.com",
                    "first_name": "Allyson",
                    "last_name": "Gillispie"
                },
                {
                    "email_address": "alva.pennigton@example.com",
                    "first_name": "Alva",
                    "last_name": "Pennigton"
                },
                {
                    "email_address": "andrew.och@example.com",
                    "first_name": "Andrew",
                    "last_name": "Och"
                }
            ]
        }
    }
    
    ```


## Result

You have a custom action that looks up the Users for a given department and converts those users into an array of contact objects.

## What to do next

Customize this action to use your own logic.

**Parent Topic:**[Script support for complex data](../concept/script-support-complex-data.md)

