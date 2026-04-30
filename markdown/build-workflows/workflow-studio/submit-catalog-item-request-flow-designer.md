---
title: Submit Catalog Item Request action
description: Create a requested item \[sc\_req\_item\] on a Service Catalog Request \[sc\_request\].
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Workflow Studio actions, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Submit Catalog Item Request action

Create a requested item \[sc\_req\_item\] on a Service Catalog Request \[sc\_request\].

## Roles and availability

Available as a Workflow Studio ServiceNow core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

## Inputs

<table id="table_n5q_qhn_tkb"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Catalog Item

</td><td>

Name of the requested catalog item.

 Extra inputs may be added dynamically, depending on which catalog item is selected. For example, when the requested catalog item is a new email account, a field for **Preferred Email address** appears.

 **Note:** The following Service Catalog variable types are not supported.

-   list collector
-   lookup multiple choice
-   lookup select box

</td></tr><tr><td>

Quantity

</td><td>

Number of items requested.

</td></tr><tr><td>

Special Instructions

</td><td>

Text describing any special instructions about the item request.

</td></tr><tr><td>

Delivery Address

</td><td>

Location where the requested item should be delivered.

</td></tr><tr><td>

Requested for

</td><td>

User that the item is requested for.

</td></tr><tr><td>

Don't fail on error

</td><td>

Option to determine whether to fail the flow if the action produces an error.

</td></tr><tr><td>

Wait for Completion

</td><td>

Option to force the flow to wait until the action has been completed before continuing.

</td></tr><tr><td>

Enable timeout

</td><td>

Option to limit the amount of time that the flow waits for the action to be completed before continuing.

**Note:** Use the **Enable timeout** option to prevent this action from continuing to run. If the condition to continue is never met, a timeout value specifies when the system skips the Wait for Condition action and go to the next item in the flow. You must set a Duration value to enable a timeout. You can also select a Schedule if you want to compute the duration end date based on a specific work schedule.

 This field appears only when the **Wait for Completion** option is selected.

</td></tr><tr><td>

Duration

</td><td>

Amount of time that the flow waits before continuing when the **Enable timeout** option is selected. Enter the time to wait in hours, minutes, and seconds. If you leave this field empty, the flow does not wait.

 This field appears only when the **Wait for Completion** option is selected.

</td></tr><tr><td>

Schedule

</td><td>

Schedule used to compute the timeout duration when the **Enable timeout** option is selected. For example, waiting for 10 hours as part of an 8-5 weekdays schedule causes the flow to wait for one or more business days. If you leave this field empty, the timeout runs without a schedule.

 This field appears only when the **Wait for Completion** option is selected.

</td></tr></tbody>
</table>## Output

<table id="table_nb4_g3n_tkb"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Data Type

</th></tr></thead><tbody><tr><td>

Error Message

</td><td>

Message that displays if the action produces an error.

</td><td>

String

</td></tr><tr><td>

Requested Item

</td><td>

Document ID for the requested item.

</td><td>

Document ID

</td></tr><tr><td>

Status

</td><td>

The completion status of the action as a numeric value.-   0 \(success\)
-   1 \(error\)
-   2 \(timeout\)

</td><td>

Choice

</td></tr></tbody>
</table>## Example

![Example Submit Catalog Item Request action in a flow.](../images/submit-catalog-item-request.png)

## Design considerations

Follow these design considerations when creating flows that contain Submit a Catalog Item Request actions.

-   **Escape quotation marks from string data pills with the String Replace transform function**

    Complex string variables are converted into JSON format when stored in the system. To prevent any JSON formatting errors, you can use a Replace String transform function to escape the quotation marks present in any string data pills you use for catalog variables. See [String transform functions](string-transform-functions.md).

-   **Use transform functions to validate data pills**

    Whenever you use a data pill to provide data for an action input, you can use a transform function to validate the data. See [Transform functions](../concept/transform-functions.md) for a list of available transform functions.


**Parent Topic:**[Workflow Studio actions](../concept/flow-actions.md)

