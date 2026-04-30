---
title: Set up message authentication for Alexa
description: Define a token in your ServiceNow instance to set up a message authentication with your Alexa account.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Set up Conversational Integration with Alexa, Configure Conversational Integration with Alexa, Conversational Integration with Alexa, Conversational IVR with Amazon Connect, Virtual Agent integration with Voice channels, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Set up message authentication for Alexa

Define a token in your ServiceNow instance to set up a message authentication with your Alexa account.

## Before you begin

Role required: admin

## Procedure

1.  In the navigation filter of your ServiceNow instance, enter `message_auth.list` and click **New**.

2.  Select a message authentication type for Alexa and open the record.

    Your ServiceNow instance provides you with the following authentication types by default.

    -   **ServiceNow Virtual Agent Alexa App - Static**
    -   **ServiceNow Virtual Agent Alexa App - Hash**
3.  On the form, fill in the fields.

<table id="table_jc1_24v_nqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the record in the Message Auth \[message auth\] table. For example, **ServiceNow Virtual Agent Alexa App - Hash** or **ServiceNow Virtual Agent Alexa App - Static**

</td></tr><tr><td>

Provider

</td><td>

Provider of the auth token. Enter `Alexa`.

</td></tr><tr><td>

Inbound message verification

</td><td>

Name of the Hash or Static Message Verification record that you created for the inbound hash or static messages.Select an inbound message verification option as per the selected authentication type.

 Your ServiceNow instance provides you with the following authentication tokens by default:

-   **ServiceNow Virtual Agent Alexa App Static Token**
-   **ServiceNow Virtual Agent Alexa App Hash Token**


</td></tr><tr><td>

Outbound message creation

</td><td>

Name specified on the Token Verification form \(this token interacts with the provider on behalf of the user\). Select an outbound message option as per the selected authentication type.

 Your ServiceNow instance provides you with the following authentication tokens by default:

-   **ServiceNow Virtual Agent Alexa App Static Token**
-   **ServiceNow Virtual Agent Alexa App Hash Token**
 **Note:** Outbound message verification is not required for Alexa. However, select the same option provided for Inbound message verification because it is a required field.

</td></tr><tr><td>

Outbound service token

</td><td>

Authorized outbound service token.Navigate to the Inbound message verification record to procure the Outbound service token from the Alexa setup and provide it in the **Outbound service token** field.

</td></tr></tbody>
</table>4.  Click **Update**.


