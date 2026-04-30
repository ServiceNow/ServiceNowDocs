---
title: Workflow Studio input and output data variables
description: Actions and subflows use variables to store input and output data. The variable data type determines what kind of data it stores and its advanced configuration options.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2024-11-04"
reading_time_minutes: 4
breadcrumb: [Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Workflow Studio input and output data variables

Actions and subflows use variables to store input and output data. The variable data type determines what kind of data it stores and its advanced configuration options.

## Data variables available for actions

The Workflow Studio UI displays action inputs as data pills in the Input Variables section of the Data pane. Action outputs are listed as data pills in the Output Variables section of the Data pane.

Workflow Studio does not display step input variables in the data pane. The output variables produced by each step are available in the data pane as part of the step that created them. For more information on using input and output variables to create a custom action, see [Building actions](../concept/actions.md).

![Screen shot of the Workflow Studio data panel. The Input Variables section contains a record data pill labelled Incident. The Output Variables section contains a record data pill labelled Problem.](../images/action-input-outputs-data-pane.png "Sample Workflow Studio data panel")

Each data pill consists of a label and a data type description. For example, the Incident input variable uses the Record data type to store an incident Sys ID. The Problem output variable uses the Record data type to store a problem Sys ID. You can expand data pills to see the contents and hierarchy of any child elements.

## Data variables available for flows and subflows

The Workflow Studio UI displays the flow trigger as a data pill in the data pane, and displays subflow inputs as data pills in the Subflow Inputs section of the Data pane. Subflow outputs are listed as data pills in the Subflow Outputs section of the Data pane.

Workflow Studio does not display action input variables in the data pane. The output variables produced by each action are available in the data pane as part of the action that created them. For more information on using input and output variables to create a flow, see [Building flows](../concept/flows.md).

## Supported variable data types

Workflow Studio supports variable data types to store ServiceNow AI Platform record data and complex data. Variables that store record data must have a data type matching the ServiceNow AI Platform [field type](https://www.servicenow.com/docs/access?context=r_FieldTypes&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) of the source data. Variables for [complex data](../concept/complex-data.md) must match the type of complex data stored, either an array or an object.

**Note:** This reference documentation doesn't list all possible ServiceNow AI Platform data types available to actions and flows. Instead, the reference information focuses on the data types used by ServiceNow provided actions and flows. For a list and descriptions of available ServiceNow AI Platform data types, see [field type](https://www.servicenow.com/docs/access?context=r_FieldTypes&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

-   **[Approval rules data type](approval-rules-data.md)**  
Store the conditions for approving or rejecting an approval requests.
-   **[Array.Boolean data type](array-boolean-data.md)**  
Store a sequence of true or false values in an array.
-   **[Array.Choice data type](array-choice-data.md)**  
Store a sequence of choice list values in an array.
-   **[Array.Datetime data type](array-datetime-data.md)**  
Store a sequence of date-time values in an array.
-   **[Array.Integer data type](array-integer-data.md)**  
Store a sequence of numeric integer data in an array.
-   **[Array.Object data type](array-object-data.md)**  
Store a sequence of JavaScript objects in an array.
-   **[Array.String data type](array-string-data.md)**  
Store a sequence of alphanumeric text values in an array.
-   **[Choice data](choice-data.md)**  
Store choice list values for a specific choice field.
-   **[Conditions data type](conditions-data.md)**  
Store a set of conditions for a specific type of record. You must select a source table to define the conditions.
-   **[Datetime data type](datetime-data.md)**  
Store date-time values.
-   **[File attachment data type](file-attachment-data-type.md)**  
Store a single file attachment as part of the action or flow's associated record rather than a record in the system Attachment table.
-   **[Integer data type](integer-data.md)**  
Store numeric integer data. Integers are whole numbers only. Fractions and decimals values are not supported.
-   **[JSON data type](json-data-type.md)**  
Store JSON formatted text values. JSON values can be generated by integration steps or by scripts.
-   **[List.\[Table\] data type](list-table-data.md)**  
Stores a list of record Sys IDs associated to a specific table. This variable supports ServiceNow AI Platform List field options such as default records and reference qualifiers.
-   **[Object data type](object-data.md)**  
Store a JavaScript object.
-   **[Password \(2 Way Encrypted\) design considerations](password-2-data.md)**  
Store encrypted password data that can be decrypted.
-   **[Records.\[Table\] data type](records-data.md)**  
Stores one or more Sys ID references to records in a specific table. The Records data format is also known as a Glide List since it stores a list of GlideRecord Sys ID values.
-   **[Reference.\[Table\] data type](reference-data.md)**  
Store a single Sys ID reference to a record in a specific table.
-   **[String data type](string-data.md)**  
Store alphanumeric text values using JavaScript data conventions.
-   **[Table name data type](table-name-data.md)**  
Store a table name value as specified in the database dictionary. Table names are always alphanumeric strings.
-   **[True/false data type](true-false-data.md)**  
Store true or false values using JavaScript data conventions.
-   **[Variables.\[Table\] data type](variables-data-type.md)**  
Store a reference to a specific table of Glide variables such as a decision input variable.

**Parent Topic:**[Flows, subflows, and actions reference](flow-designer-reference.md)

