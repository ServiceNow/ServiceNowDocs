---
title: Create or Update Record step
description: Create or update a record in a ServiceNow table using a single operation. Update a record that exists, or create a record using the values provided.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Steps, Flows, subflows, and actions reference, Reference, Workflow Studio, Build workflows]
---

# Create or Update Record step

Create or update a record in a ServiceNow table using a single operation. Update a record that exists, or create a record using the values provided.

## Identification of existing records

The Create or Update Record step identifies existing records by searching for matching values in the fields that you select as unique identifiers. For example, you can specify that the short description and priority fields uniquely identify an incident. When the step finds an incident with a matching short description and priority, it updates the matching record rather than creating a new record.

**Note:**

-   If no field is selected as a unique identifier, the step creates a record with the field values provided.
-   If more than one record matches the value of the unique identifiers, the step doesn't update any records and displays an error message in the flow execution details.

## Roles and availability

Available as an Workflow Studio action step. Users with the action\_designer role can create a custom action with one or more action steps.

## Inputs

Provide a value for each input that your action needs. To add dynamic values, you can also drag and drop pills from the Data panel or select them from the pill picker.

-   **Table**

    Data type: **Table Name**

    Table in which to create or update a record.

-   **Fields**

    Data type: **Template Values**

    Field values to set or update for the record. For example, to set the short description to a certain value, select **Short description** and set the desired value.

    **Important:** The system does not support updating multiple journal fields such as the additional comments or work notes of a task record.

    If adding the action to a subflow, you can [Create a template value input](../task/template-value.md). Dynamically set field values can trigger server-side validation rules but cannot trigger UI policies.

-   **Determines uniqueness**

    Data type: **True/False**

    Option for selecting the field as a unique identifier, which determines when to update or create a record. A record is updated when the incoming field value matches an existing record field value. A record is created when the incoming field value does not match an existing record field value. This option appears when the required table name and fields are selected.

-   **If this step fails**

    Data type: **Choice**

    Option to continue running the next step or go to error evaluation. This option has no effect on the Step Status output. Choices include:

    -   **Don't stop the action and go to the next step**: Continues running the action at the next step.
    -   **Go to Error Evaluation**: Stops running the action and goes to the Error Evaluation section.

## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your action.

-   **Record**

    Data type: **Record**

    Reference to record created or updated.

-   **Table**

    Data type: **Table Name**

    Table where record was created or updated.

-   **Error Message**

    Data type: **String**

    Error message produced when the record operation fails.

-   **Status**

    Data type: **Choice**

    Completion status of the action. The flow execution details page displays one of these values.

    -   Created \[created\]: The action created a record.
    -   Updated \[updated\]: The action updated a record.
    -   Error \[error\]: The action produced an error.
-   **Step Status**

    Data type: **Object**

    Object data pill containing runtime details about the step. Each step in an action returns a Step Status.

-   **Step Status Code**

    Data type: **Integer**

    Integer data pill indicating whether the step produced an error. A step returns a value of 1 when it produces an error for any reason. For example, a step can produce an error if it is missing mandatory input data or returns output in the wrong data type. A step returns a value of 0 when it runs successfully. You cannot customize these codes.

    -   Success \[0\]: The step succeeded.
    -   Error \[1\]: The step produced an error.
-   **Step Status Message**

    Data type: **String**

    String data pill containing the error message produced by the step or system operation. You cannot customize the step status message.


## Create or update a problem record

![Configuration of the Create or update record step](../images/example-create-update-record-step.png)

This action has two inputs. There is a string input for a description, and a reference input for a User record. The Create or Update Record step uses these inputs to create or update a problem record. The Problem statement and Opened by fields determine uniqueness. When the input values match, the step performs an update operation instead of a create operation.

**Parent Topic:**[Workflow Studio steps](../concept/steps.md)

