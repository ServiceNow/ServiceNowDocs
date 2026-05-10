---
title: Script support for complex data
description: Create and reference complex data from a script. Use a script when your source data comes from a data stream, a REST step response, or a Look Up Records step.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Complex data, Build actions, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Script support for complex data

Create and reference complex data from a script. Use a script when your source data comes from a data stream, a REST step response, or a Look Up Records step.

Use script to create complex data when data comes from these sources.

|Data source|Create/map complex data from|
|-----------|----------------------------|
|Data Stream action response stream|Script Parser step|
|REST step response|Script step|
|Look Up Records step|

## Data Stream action response stream

Data Stream actions use a parser script to map stream item values to complex object values. When writing a parser script, use JavaScript methods appropriate to the data stream format. For example, use the [JSON - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/JSONScopedAPI.md) class to parse or encode a JSON data stream.

Parser scripts have access to the data stream input and output objects as well as a targetObject property. See [Data Stream actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/create-data-stream-action.md) for more information about parsing a response stream to create complex data.

## REST step response

You can convert a REST step response into one or more complex objects by parsing it with a Script step. To access a response from a Script step, you must create an input script variable and map it to the response payload from the prior REST step. See [Script step](../reference/javascript-step-action-designer.md) for more information about creating script input variables.

Write a script that maps REST response values to complex object values. When writing REST response script, use JavaScript methods appropriate to the response format such as the JSON parse\(\) method.

**Note:** When you use complex data as the source of a string input, Workflow Studio automatically converts it into a JSON string.

You do not need to use a Script step to create a REST request from complex data. You can generate complex data in a prior action or step and then map it to a string input of the REST step. At run time, the action or flow converts the complex data into a JSON representation.

For example, see the script steps used in [Get started with dynamic inputs](../task/getting-started-dynamic-input.md#) for the data gathering actions. The data gathering actions for getting table and field names both use a Script step to parse a REST response into a JSON object. Both data gathering actions also create output variables that store complex data as JSON objects.

## Look Up Records step

While flows can use **For each** flow logic to process a list of records, actions require a Script step. The Script step replaces the **For each** flow logic with JavaScript such as a `For` or `While` loop.

To access record data from a Script step, you must create an input script variable and map it to the record data from the prior look up step. See [Script step](../reference/javascript-step-action-designer.md) for more information about creating script input variables.

See [Create a custom action to generate an array of objects from a list of records](../task/create-custom-action-array-objects.md) for an example action that converts a list of user records into an array of contact objects.

**Note:** The Look Up Records action does not require a Script step to convert record data into complex data. You can create a custom action to convert a record into an object and apply **For each** flow logic to the custom action. See [Create a custom action to generate an object from a record](../task/create-custom-action-object.md) and [Create a custom flow to generate an object for each record in a list](../task/create-custom-flow-object.md) for an example of creating a complex object without using script.

## Dot-walking object structures

You can reference elements from the structure of an object by dot-walking the path of the structure. All complex data paths start with the name of the data source, which is either the global object for inputs, the global object for outputs, or the name of the array or object you created in script.

Next in the path are the names of each structural element referenced separated by period characters \(also known as dots\). Listing the names of structural elements is identical to dot-walking a reference field where you list the table structure to a particular reference field.

**Note:** A dot-walk path always lists the name of a structural element rather than its label.

For example, suppose that you define a contact object as an Output variable. The object has the following structure.

![A script step output variable containing a complex object for Contact.](../images/complex-object-contacts.png "Sample Contact object")

|Place in structure|Label|Name|Type|
|------------------|-----|----|----|
|Parent|Contact|contact|Object|
|Child|First name|first\_name|String|
|Child|Last name|last\_name|String|
|Child|Email Addresses|email\_addresses|Array.Object|
|Grandchild|Email Address|email\_address|Object|
|Great grandchild|Type|type|Choice|
|Great grandchild|Email|email|String|
|Child|Telephone|telephone\_number|Array.Object|
|Child|Mailing Addresses|mailing\_address|Array.Object|

The dot-walk path to the **First name** structural element would be `outputs.contact.first_name` while the path to the **Email** structural element would be `outputs.contact.email_addresses[0].email` since you must specify an individual element of the array by its JavaScript index value.

**Note:** A dot-walk path omits the name of the repeated element within the array. For example, an array of objects does not have to specify the object element name. However, since objects are containers for other elements, you can specify a child element of the object within a dot-walk path.

## General guidelines

Keep these general guidelines in mind when scripting with complex data.

-   **Use string inputs to convert complex data into a JSON string**

    When you map complex data to a string input, Workflow Studio automatically converts it into a JSON string. Instead of writing a script, you can add a string input to a REST step and map it to complex data from a prior action or step.

-   **Save your objects as templates**

    Save your objects as templates so you can reuse them in other actions, flows, and Script steps.

-   **Create script input variables to access prior data**

    Create a script input variable for any data you want to access from the action input or a prior step. Map the script input variable to the input or step data pill. For example, map the script input variable to a list of user records you looked up in a prior step.

-   **Create a script output variable to store complex data**

    Create a script output variable to store any complex data your script creates. The script output variables must match the values defined in the script. For example, create a contacts array of objects to store multiple contact objects. Save the contact object as a template so you can reuse it.

-   **Map the action output to the script output variable**

    When you want a custom action to output complex data, add an action output and map it to the data pill for your Script step output variable. For example, create a contacts array and load the contact object template you saved earlier. Map the action output to the contacts array produced by your Script step.


-   **[Create a custom action to generate an array of objects from a list of records](../task/create-custom-action-array-objects.md)**  
Generate an array of objects from a list of User records. Learn how to use a Script step to iterate through a list of records.
-   **[Create a custom action to generate an array of strings from a list of records](../task/create-custom-action-array-strings.md)**  
Generate an array of strings from a list of User Role records. Learn how to use a Script step to iterate through a list of records.

**Parent Topic:**[Complex data](complex-data.md)

