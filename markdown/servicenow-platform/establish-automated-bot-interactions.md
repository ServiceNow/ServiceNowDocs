---
title: Configure a contact flow for an automated caller interaction
description: Invoke an automated caller interaction with bots to fulfill the caller's request within the ServiceNow instance.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Integrate ServiceNow Voice with Amazon Connect, Integrating with applications, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure a contact flow for an automated caller interaction

Invoke an automated caller interaction with bots to fulfill the caller's request within the ServiceNow instance.

## Before you begin

Role required: sn\_cti\_core.admin

## About this task

When a caller contacts the call center, using the voice or dual-tone multi frequency \(DTMF\) inputs from caller, a contact flow is invoked in the Amazon Connect instance based on the caller context. The contact flow contains nodes that act as integration points between Amazon services and the ServiceNow instance. Based on the nodes defined in the contact flow, the corresponding operation handlers are triggered in the ServiceNow instance. The caller then gets the response that is defined in the operation handler. For information about contact flows, see the Amazon [documentation](https://docs.aws.amazon.com/connect/latest/adminguide/connect-contact-flows.html).

In the ServiceNow base system, a few operation handlers are available by default. For information on operation handlers, see [ServiceNow Voice reference](../reference/ccc-reference.md).

## Procedure

1.  If you do not want to use a default operation handler, create and configure an operation handler in the ServiceNow instance.

    1.  Navigate to **ServiceNow Voice - Core** &gt; **Operation Handlers**.

    2.  Click **New**.

    3.  On the form, fill in the fields.

<table id="table_mty_vhv_glb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Operation Name

</td><td>

Name of the operation that you want to automate.

</td></tr><tr><td>

Type

</td><td>

Type that specifies how the operation is implemented.-   Script: Implementation is included in a script.
-   Forward to Handler: Request is forwarded to an operation handler, which is invoked by lookup on the sys\_id of that handler. This scenario is possible when you have different intents for similar operations, for example, Create an HR incident and Create incident.
-   Forward to Operation: Request is forwarded to an operation handler, which is invoked by lookup on the name of the handler and then name resolution to find the handler.
-   Integration Hub - Action: Calls an Integration Hub action.
-   Integration Hub - Subflow: Calls an Integration Hub flow or subflow.


</td></tr><tr><td>

Application

</td><td>

Application associated with the operation handler.

</td></tr><tr><td>

Domain

</td><td>

Domain associated with the operation handler.

</td></tr><tr><td>

Active

</td><td>

Option to activate the operation handler.

</td></tr><tr><td>

Require Authentication

</td><td>

Option to enable authentication for the operation handler.**Note:** If this option is selected, the corresponding operation is invoked only when a valid authentication token is passed in the request. It is supported by an authentication operation handler that supports pin-based authentication, which can be leveraged in your contact flows. For information about configuring the PIN, see [Configuring a phone PIN](../concept/set-pin-ccc.md#).

</td></tr><tr><td>

Description

</td><td>

Summary about the operation handler.

</td></tr><tr><td>

Script

</td><td>

Script that contains the operation implementation and the response for the caller. This field appears when **Script** is selected for **Type**.

</td></tr><tr><td>

Forward To

</td><td>

Operation handler to which you want to forward the request. This field appears when **Forward to Handler** or **Forward to Operation** is selected for **Type**.

</td></tr><tr><td>

Integration Hub - Action

</td><td>

Integration Hub action that you want to call to complete the request. This field appears when **Integration Hub - Action** is selected for **Type**.

</td></tr><tr><td>

Integration Hub - Flow/SubFlow

</td><td>

Integration Hub flow or subflow that you want to call to complete the request. This field appears when **Integration Hub - Subflow** is selected for **Type**.

</td></tr></tbody>
</table>    4.  Click **Submit**.

2.  Create a contact flow in Amazon Connect to define an end-to-end customer experience.

    For information about creating a contact flow, see the Amazon [documentation](https://docs.aws.amazon.com/connect/latest/adminguide/create-contact-flow.html).

    When building a contact flow within Amazon Connect, use any of these nodes to trigger operation handlers defined in the ServiceNow instance. These nodes act as integration points between Amazon services and the ServiceNow instance.

<table id="table_q4j_1tt_ymb"><thead><tr><th>

Node

</th><th>

Description

</th><th>

Configuration

</th></tr></thead><tbody><tr><td>

Get Customer Input

</td><td>

Invokes a Lex Bot. The operation handler that is triggered is based on the name of the intent associated with the Lex Bot. For information about this node, see the Amazon [documentation](https://docs.aws.amazon.com/connect/latest/adminguide/get-customer-input.html).**Note:** This node can be used when the integration is between Amazon Lex and the ServiceNow instance.

</td><td>

1.  Create an intent for the required Lex Bot in your Amazon Connect instance. For information about creating an intent, see the Amazon [documentation](https://docs.aws.amazon.com/lex/latest/dg/gs2-create-bot-intent.html).
2.  Specify the following information in the intent.
    -   Intent name: Name of the intent.

**Note:** This intent name should match an operation handler in the ServiceNow instance with the same name, or name + ‘\_&lt;suffix&gt;’ where suffix can contain any five uppercase alpha characters.

    -   Sample utterances: Caller utterances that trigger the operation handler.
    -   Lambda initialization and validation: If the operation handler being invoked requires authentication, select the **Initialization and validation code hook** check box and select the deployed AWS Lambda function.
    -   Lambda function: Deployed AWS Lambda function that is invoked.
3.  Save, build, and publish the intent.
4.  Open the required contact flow in the contact flow designer in your Amazon Connect instance.
5.  Click the Get Customer Input node and specify the Lex Bot details in the **Amazon Lex** section.
6.  Click **Save**.


</td></tr><tr><td>

Invoke AWS Lambda Function

</td><td>

Invokes an AWS Lambda function. The operation handler that is triggered is based on the **sn\_operation** parameter set on the node in the contact flow. For information about this node, see the Amazon [documentation](https://docs.aws.amazon.com/connect/latest/adminguide/invoke-lambda-function-block.html).**Note:** This node can be used to for data dips \(for example, authorizing a caller\) where the integration is between the call center and the ServiceNow instance. The data dip configuration allows a caller to enter information, such as an account number, to route calls to a particular queue. Using this number, you can look up the first name of the caller and create an interaction record after the call is initiated. Also, you can customize the greeting with the caller name later in the flow.

</td><td>

1.  Open the required contact flow in the contact flow designer in your Amazon Connect instance.
2.  Click the Invoke AWS Lambda Function node and specify the following input parameters.
    -   Destination key: sn\_component, Value: Component from where the Lambda function is invoked. For example, sn\_aws\_connect\_lambda\_proxy\_component.
    -   Destination key: sn\_operation, Value: Name of the operation handler that you want to invoke. For example, interactionEvent.
    -   \(optional\) Destination key: queueName, Value: Name of the queue that you want to transfer the flow to.

**Note:** This parameter is used to invoke the workItemEvent operation handler.

    -   \(optional\) Destination key: queueId, Value: ARN of the queue that you want to transfer the flow to.

**Note:** This parameter is used to invoke the workItemEvent operation handler.

    -   \(optional\) Destination key: authToken, Value: AuthToken received via authentication call. This parameter is required for invoking an operation handler that requires authentication.
    -   \(optional\) Destination key: interactionId, Value: Interaction ID received via interactionEvent call.
3.  Click **Save**.


</td></tr></tbody>
</table>3.  Ensure that a caller’s phone number is associated with the contact flow after it is created and published.

    This process ensures that each time the caller calls, the corresponding contact flow is invoked. For information about associating a phone number with a contact flow, see the Amazon [documentation](https://docs.aws.amazon.com/connect/latest/adminguide/associate-phone-number.html).

    **Note:** For a sample implementation of invoking operation handlers in a contact flow, you can refer to the default contact flows. For information on default contact flows, see [Components installed with ServiceNow Voice for ITSM](../reference/instld-with-cloud-call-center-itsm.md) and [Components installed with ServiceNow Voice for CSM](../reference/instld-with-ccc-csm.md).


**Parent Topic:**[Integrate ServiceNow Voice with Amazon Connect](integrate-ccc-amazonconnect.md)

