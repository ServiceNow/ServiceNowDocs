---
title: Complex data
description: Use a graphical interface to work with collections of complex structured data. Help design users understand the organization of structured data, and add, remove, or configure its individual elements.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Build actions, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Complex data

Use a graphical interface to work with collections of complex structured data. Help design users understand the organization of structured data, and add, remove, or configure its individual elements.

Complex data allows you to encode and store structured data in a machine-readable format such as JavaScript Object Notation \(JSON\) or eXtensible Markup Language \(XML\). You can use the Workflow Studio interface to view and understand the organization of structured data as well as create data structures. For example, you can create a contact data structure consisting of information you look up from a user record such as first name, last name, and email address.

You can create complex data from these Workflow Studio interfaces.

<table id="table_t4t_qfz_4hb"><thead><tr><th>

Workflow Studio interface

</th><th>

Example usage

</th></tr></thead><tbody><tr><td>

Action inputs and outputs

</td><td>

Create an action that generates an object from record data. Populate the object using record data the action looks up. See [Create a custom action to generate an object from a record](../task/create-custom-action-object.md)

</td></tr><tr><td>

Script step input and output variables

</td><td>

Write a script to create an array of objects from a list of records. See [Create a custom action to generate an array of objects from a list of records](../task/create-custom-action-array-objects.md).

 Write a script to parse a JSON document into an output of type Object.

</td></tr><tr><td>

Subflow inputs and outputs

</td><td>

Create a subflow that accepts an object as an input and uses it to call an external service.

</td></tr><tr><td>

XML parser step Target field configurations

</td><td>

Parse an XML payload into a complex data object using the XML parser step.

</td></tr><tr><td>

REST API Trigger Body field

</td><td>

Parse an inbound REST API request into a complex data object and use the values in a flow. See REST API trigger.

</td></tr></tbody>
</table>## Benefits

Complex data offers these benefits.

-   Parse and format data without having to write code. For example, create data variables to parse a response message or format a request message.
-   Create arbitrary data structures. For example, create an issue data structure that combines information from existing interaction and incident records, or create a data structure to support a custom integration.
-   View the organization of data structures. For example, an issue data structure might consist of a user object to describe who to contact about the issue and a history object to describe the work done to resolve it. You could configure a notification action with the path to the email address listed in the user object, and call an escalate issue subflow with the path to the status or reassign count from the history object.
-   Allow access to data structure from API calls. For example, call an action or subflow from a script and use the predefined data structure as input values.
-   Save and reuse data structures as templates. For example, save the user object as a template data structure for reuse in other actions and flows.

## Data structure

A data structure is a collection of related data elements organized into a hierarchy. Each element in a data structure has its own data type and its own unique position in the hierarchy.

The Editor pane displays data structure hierarchy with indentation. The indentation level identifies whether an element is a parent, child, or sibling in the hierarchy. Parent elements have children indented underneath them, and siblings have the same indentation level.

**Note:** The Workflow Studio interface allows you to create hierarchies with an unlimited number of child levels, but you may have to scroll horizontally to see them.

For example, this data structure consists of an Employee parent element with four child elements for ID Number, Name, Start Date, and Contact Email. The Contact Email element is also a parent element with one child.

![Sample inputs for an Employee object. The Employee object is the parent item. There are child inputs for ID Number, Name, Start Date, and Contact Email.](../images/complex-data-employee-object.png "Sample inputs for an Employee object")

The data panel displays data structure hierarchy as a tree of collapsible and expandable data pills just like it does with record variables. Parent elements have an arrow icon to collapse or expand the hierarchy.

For example, here is the Employee data structure as seen from the data panel.



![Sample data pill for the Employee object. The Employee object is the parent item. There are child inputs for ID Number, Name, Start Date, and Contact Email.](../images/complex-data-employee-object-data-pill.png)

You can use the data panel or Data picker to select specific values from a data structure. Data structures are similar to data pills for records in that you can dot-walk or navigate to specific elements within the structure. When you select a data element, Workflow Studio displays the path to it as a data pill just like any other data element selection. For example, if you select the Start Date data element, the path is **\[Input-&gt;Employee-&gt;Start Date\]**.

You can use an element data path the same way you can an XPath or JPath. Sometimes you may even convert the data pill path into one of these path notations.

## Complex data types

You build data structures using one or more Array or Object variables. Only these variable data types support child variables.

An Array variable contains values for one type of item. The parent variable is always of an Array data type, and there is always only one child variable, which is one instance of the data type supported by the array. Create Array variables when an input or output accepts multiple values of the same data type.

For example, you could create a Contact Email array to list all the email addresses associated with a given person.

|Component label|Data Type|Sample Data|
|---------------|---------|-----------|
|Contact Email|Array.String|beth.anglin@example.com and beth@anglin.com|
|Contact Email\_child0|String|

An Object variable contains any number and arrangement of child variables that each have their own data type and values. Nesting Object variables allows you to create complex data structures similar to a table schema where one table has related records in another table. Create Object variables when an input or output accepts one or more related properties.

For example, you can create an Employee object to define information about the people who work at a company.

|Component label|Data Type|Sample Data|
|---------------|---------|-----------|
|Employee|Object| |
|ID Number|Integer|20190304000101|
|Name|String|Beth Anglin|
|Start Date|Date/Time|March 4, 2019|
|Contact Email|Array.String|beth.anglin@example.com and beth@anglin.com|

Only these variable data types can be parents.

|Data type|Description|
|---------|-----------|
|Array.Array|A container for arrays. Adds a read-only child item of type Array.|
|Array.True/False|A container for true/false values. Adds a read-only child item of type True/False.|
|Array.Choice|A container for choice values. Adds a read-only child item of type Choice.|
|Array.Date/Time|A container for date/time values. Adds a read-only child item of type Date/Time.|
|Array.Integer|A container for integer values. Adds a read-only child item of type Integer.|
|Array.Object|A container for objects. Adds a read-only child item of type Object, which displays the **Add Child Item** option.|
|Array.String|A container for string values. Adds a read-only child item of type String.|
|Object|A container for other data elements. Displays the **Add Child Item** option.|

Array and Object variables only support these child data types.

-   Array
-   True/False
-   Choice
-   Date/Time
-   Integer
-   Object
-   String

**Note:** The data types in array and object variables are not Glide elements. There may not be complete compatibility between these items and Now platform types.

## Advanced options

Object variables have advanced options to save and load data structures. These options allow you to reuse a data structure defined in one location in another. For details on advanced options see [action variable data types](../reference/action-inputs-outputs.md).

## Data structure templates

Data structure templates allow you to reuse Object variables in multiple actions or subflows. For example, you can create a data structure to parse a response and then later reuse that same data structure to format a request. A template stores the list of child variables and their structure within an object. Each Object variable has an Advanced Option to save it as a template.

When you apply a template, you are creating a copy of the original structure. Any changes you make after applying a template do not affect the template, nor do they affect other actions that use the template.

## Array data pills

Objects that contain array data may require **For Each** flow logic to process. For example, a user object that contains an array of email addresses would require a **For Each** flow logic loop to send a notification to each email address.

## Object data pills

You can design actions that accept object data pills as input values. For example, you might create a notification action that accepts a user object as an input. If the user object consists of values for first name, last name, and addresses, then the notification action has access to all these values. To configure an action input with an object data pill, you must create an object earlier in the flow.

![A sample action in a flow. There are inputs for User, First name, Last name, Addresses, and Address 1.](../images/action-inputs-accepts-object.png "Sample action that accepts an object data pill")

You can use an object data pill or any of its child elements to configure an input. When you configure an input value with an object data pill, Workflow Studio makes any child elements of the object read-only, and the action uses the values provided by the object. For example, you can create a flow where one action generates a user object and another action sends a notification to the user specified in the object.

![A sample action in a flow. There are inputs for User, First name, Last name, Addresses, and Address 1. The User input contains the data pill [2->User Object].](../images/action-inputs-configured-with-object.png "Sample action configured to use an object data pill")

When you configure the child elements of an object, you must manually provide data pills for each child element of the object. For example, you can manually configure the user object with record values from an earlier action.

## Script support

Create and reference complex data from a script. Use a script when your source data comes from a data stream, a REST step response, or a Look Up Records step. See [Script support for complex data](script-support-complex-data.md) for more information about scripting with complex data.

## Update set support

Update sets include complex objects as part of the flow, subflow, or action where they are defined. Any change to the parent flow, subflow, or action automatically captures its associated complex data.

## General guidelines

Follow these general guidelines to create reusable and maintainable data structures.

-   **Minimize the number of child levels in the hierarchy**

    The more child levels a data structure has, the more difficult it is to view and select a data variable from the hierarchy. While you can build data structures with any number of child levels, it becomes difficult to navigate and understand data structures with more than seven child levels. For the best user experience, avoid creating data structures that have so many child levels you must scroll horizontally to see and populate them.

-   **Create a separate object for each type of record data**

    Most Workflow Studio data is record data whether it is from an instance or an external system. This design method ensures that you know what the object contains and where the data came from.

-   **Recreate record data structures**

    When building objects that receive or transmit record data, review the database dictionary entries for these records and create matching object data structures. For example, suppose that you want an object to contain data from Incident and Configuration Item tables. You might create a string element for the Short description field in the Incident table, and an array of strings element for the Class field in the Configuration Item table.

-   **Create objects to combine different types of records**

    If you need information from multiple types of records, create an object that contains all the information you need. You can then use the object to format or parse data in Workflow Studio.


-   **[Create data structure](../task/create-data-structure.md)**  
Organize multiple data variables into a structure to process them as a unit and identify the individual items within it.
-   **[Save data structure](../task/save-data-structure.md)**  
Save the data structure of child variables within an Object variable for later reuse.
-   **[Load data structure](../task/load-data-structure.md)**  
Load a data structure of child variables within an Object variable.
-   **[Create a custom action to generate an object from a record](../task/create-custom-action-object.md)**  
Generate an object from a User record. Learn how to use an Action output to create an object from record values.
-   **[Create a custom flow to generate an object for each record in a list](../task/create-custom-flow-object.md)**  
Generate an object for each User record in a list. Learn how to use flow logic to iterate through a list of records.
-   **[Script support for complex data](script-support-complex-data.md)**  
Create and reference complex data from a script. Use a script when your source data comes from a data stream, a REST step response, or a Look Up Records step.

**Parent Topic:**[Building actions](actions.md)

