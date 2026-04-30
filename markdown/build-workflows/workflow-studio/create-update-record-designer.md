---
title: Create or Update Record action
description: Create or update a record in a ServiceNow table using a single operation. Update a record that exists, or create a record using the values provided.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Workflow Studio actions, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Create or Update Record action

Create or update a record in a ServiceNow table using a single operation. Update a record that exists, or create a record using the values provided.

## Identification of existing records

The Create or Update Record action identifies existing records by searching for matching values in the fields that you select as unique identifiers. For example, you can specify that the short description and priority fields uniquely identify an incident. When the action finds an incident with a matching short description and priority, it updates the matching record rather than creating a new record.

**Note:**

-   If no field is selected as a unique identifier, the action creates a record with the field values provided.
-   If more than one record matches the value of the unique identifiers, the action doesn't update any records and displays an error message in the flow execution details.

## Roles and availability

Available as a Workflow Studio ServiceNow core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

## Inputs

Provide a value for each input that your flow needs. To add dynamic values, you can also drag and drop pills from the Data panel or select them from the pill picker.

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


## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your flow.

-   **Record**

    Data type: **Record**

    Reference to record created or updated.

-   **Table**

    Data type: **Table Name**

    Table where record was created or updated.

-   **Status**

    Data type: **Choice**

    Completion status of the action. The flow execution details page displays one of these values.

    -   Created \[created\]: The action created a record.
    -   Updated \[updated\]: The action updated a record.
    -   Error \[error\]: The action produced an error.
-   **Error Message**

    Data type: **String**

    Error message produced when the record operation fails.


## Update problem record from inbound email

![Inputs used for create or update problem record.](../images/example-create-update-record.png "Inputs used for create or update problem record")

**Parent Topic:**[Workflow Studio actions](../concept/flow-actions.md)

