---
title: Using variables in a workflow
description: Within workflow there are several different types of variables that are available.Activity variables are properties specifically associated with a workflow activity.Workflow variables are external values that are passed into and referenced by a workflow during its execution.After being declared in a workflow, values can be assigned to the variables from where the workflow is kicked off.Store and share string-based variables as name-value pairs between workflow activities.Current is the database GlideRecord that kicked off the workflow, either by association to the table in the Workflow properties table or by being associated with a catalog item.
locale: en-US
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Workflow management, Classic Workflow, Build workflows]
---

# Using variables in a workflow

Within workflow there are several different types of variables that are available.

Some variables define, describe, or compose the pieces of the workflow \(such as [workflow activities](c_WorkflowActivities.md)\). Some variables are available specifically to facilitate the execution of a workflow \(such as scratchpad variables\). Some variables define, describe, or compose the data records being manipulated by the workflow process \(for example, the elements of a Glide Record that are defined in a dictionary.xml file describing a record, such as an incident\).

**Parent Topic:**[Workflow management](../../workflow-administration/concept/managing-workflows.md)

## Activity variables

Activity variables are properties specifically associated with a workflow activity.

### Before you begin

Role required: admin

### About this task

These are the inputs that appear on the activity definition when a specific activity is dragged onto the workflow canvas. These variables are properties that define, compose or describe the workflow activity, or the work it is designed to perform.

Activity variables are declared in a related list within the Workflow Activity Definition.

To add, view, or modify a variable:

### Procedure

1.  Navigate to **All** &gt; **Workflow** &gt; **Activity Definitions**.

2.  Select a workflow activity, such as **Approval - User**.

3.  In the **Activity Variables** section or tab, add, view, or modify the variables. Activity variables are defined using the same fields as [System dictionary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_SystemDictionary.md).

    **Note:** If defining a new activity variable that is dependent on another activity variable, put the prefix "vars." before the name of the parent activity variable. For example, if the child field is dependent on a field named **parent**, put the value `vars.parent` in the **Dependent** field.

    To control the visibility of an activity variable on the workflow canvas after the activity has been dragged to the canvas, use a UI policy on the wf\_activity table.

    To access the variables or assign values to these variables within the workflow activity, use the *vars* variable of the workflow activity.

    ```
     activity.vars.variable_name = new_variable_value 
    ```


## Workflow input variables

Workflow variables are external values that are passed into and referenced by a workflow during its execution.

### Before you begin

Role required: admin

### About this task

Workflow variables can be declared externally in a script and passed into a main workflow or they can be declared within a main workflow and passed as inputs to a subflow.

**Note:** There is a specific kind of input variable for any workflow that is declared against the table Requested Item \[sc\_request\_item\]. To understand the use of these variables, see [Workflow catalog variables](c_WorkflowCatalogVariables.md#).

Workflow variables are declared in a form available from the Workflow Editor gear menu.

### Procedure

1.  Navigate to **All** &gt; **Workflow** &gt; **Workflow Editor**.

2.  Edit and check out a workflow.

3.  Select the Workflow Activities menu and select **Edit Inputs**.

4.  Select an existing variable or select **New**.

    Note the **Column name** field. Use this value when accessing the variable from a script.

    Workflow variables do not appear on the workflow canvas, they are only available for view from the Workflow Activity menu.

    The input variables are available to use in scripts. To access an input variable from a script:

    ```
    var input  = workflow. variables. variableName //*get the workflow variable identified by column name*.
    ```


## Assigning values to variables from outside of workflow

After being declared in a workflow, values can be assigned to the variables from where the workflow is kicked off.

The following example demonstrates how a workflow variable's value can be set in a script include, business rule, or UI action:

```
 
//Declare an instance  of workflow.js 
var wf  = new Workflow ( ) //Get the workflow id 
var  wfId  = wf. getWorkflowFromName ( "Workflow Name" ) ; 
//Start workflow, passing along name : value pair(s) for mapping to variable 
//where input_var_name is the name of the variable declared in gear menu 
//and input_var_value is whatever that value should be for this execution of 
//workflow
wf. startFlow (wfId , null , "Workflow Name" , {input_var_name : input_var_value } ) ;
```

Another example that demonstrates a more readable way of passing multiple variables involves declaring an object, adding the names/values to the object, and passing it:

```
//Declare an instance  of workflow.js 
var wf  = new Workflow ( ) 
//Get the workflow id 
var  wfId  = wf. getWorkflowFromName ( "Workflow Name" ) ; 
//Start workflow, passing along object containing name/value pairs mapping to inputs expected by the workflow 
var vars  = { } ;
vars. input_var_name1 = input_var_value1 ;
vars. input_var_name2 = input_var_value2 ; 
// add as many variables as your workflow is expecting, then pass the object
wf. startFlow (wfId , null , "Workflow Name" , vars ) ;
```

### Assigning Values for Subflow Inputs from inside of a Main Workflow

If a workflow that accepts inputs is called from within another workflow, those input values can be set from the workflow canvas within the UI of the workflow activity. Each input variable declared for a subflow will have a text box input area displayed on the activity. Within these text boxes, the variables can be set with any value either from the scratchpad or from within the current record.

For more information, see [Workflows used as subflows](../../workflow-activities/reference/workflows-as-subflows.md).

### Reading the Value of a Workflow Input Variable

The value of a Workflow input variable is accessible anywhere within the workflow that accepts javascript by dot walking the current workflow object:

```
var readValue = workflow.inputs.variable_name;
```

## Workflow scratchpad variables

Store and share string-based variables as name-value pairs between workflow activities.

The scratchpad is global to the instance of the running workflow and as such, is available equally to all activities.

### Declaration

The scratchpad itself is automatically available to an executing workflow and requires no specific declaration. Variables are declared and stored in the scratchpad simultaneously by referencing it. For example:

```
workflow.scratchpad.variableName = variableValue;
```

### Display

View activity scratchpad values from the Workflow Activity History Scratchpad \[wf\_history\_scratchpad\] table. Workflow Activity History Scratchpad is also an embedded list in Worfklow Activity History records.

![](../image/wf_history_scratchpad.png "Sample Workflow Activity History Scratchpad records")

### Access and Assignment

Use standard JavaScript object notation to access or assign scratchpad values. For example, use this format to assign a particular scratchpad variable value.

```
workflow.scratchpad.variableName = variableValue;
```

Use this format to assign a JavaScript variable to a scratchpad variable.

```
var myValue = workflow.scratchpad.variableName;
```

## Current variables

Current is the database GlideRecord that kicked off the workflow, either by association to the table in the Workflow properties table or by being associated with a catalog item.

### Declaration

Variables in current are the columns that are defined in the `dictionary.xml` file that support the database record. There is no way at runtime to add variables to the current record.

### Display

Variables of a current record are displayed on the Glide Forms and Lists throughout the applications that use them.

### Access and Assignment

To access the variables or assign values to the variables within the workflow activity, get the value from the current record by referencing the Glide Element.

```
var myVarValue = current.getElement(nameOfTheField);
```

or

```
var myVarValue = current.fieldName;
```

or

```
current.variableName.setValue( "A Variable Value");
```

