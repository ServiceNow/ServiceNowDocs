---
title: Initiate messaging conversations from CSM Configurable Workspace
description: Compose an SMS message from CSM Configurable Workspace to interact with a customer contact or a consumer regarding customer service cases.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Using CSM Configurable Workspace in Customer Service Management, Manage cases, Using Customer Service Management, Customer Service Management]
---

# Initiate messaging conversations from CSM Configurable Workspace

Compose an SMS message from CSM Configurable Workspace to interact with a customer contact or a consumer regarding customer service cases.

## Before you begin

Ensure that an administrator has completed the following tasks:

-   Configured the Agent-Initiated Messaging Interface application. For more information, see [Agent-initiated messaging interface](https://www.servicenow.com/docs/access?context=agent-init-messg-interface&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).
-   Configured at least one qualifying messaging channel for the agent-initiated messages. For more information, see [Determine whether messaging channels are available for agent-initiated messages](https://www.servicenow.com/docs/access?context=agent-init-messg-channel-ext-pt&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).

Role required: agent\_workspace\_user

## Procedure

1.  Navigate to **All** &gt; **Workspace Experience** &gt; **Workspaces** &gt; **CSM Configurable Workspace Home**.

2.  On the CSM Configurable Workspace Home page, navigate to **Lists** &gt; **Interactions** &gt; **My Interactions**.

3.  In the My Interactions list, select the interaction number in **Number** column of the My Interactions list.

    **Note:** Ensure that the interaction type is other than messaging and the interaction state is not closed complete or closed abandoned.

4.  On the Details tab of the workspace form, fill in the details for a new interaction or modify the details.

    For more information about the form, see [CSM workspace form features](../../../administer/workspace/reference/csm-agent-workspace-agent-actions.md).

    **Note:** The user profile associated with an interaction is configured by an administrator by using the sn\_agent\_initiated.AgentInitiatedMessagingUserDocument extension point. The AgentMessagingInteractionUserDocument script include that implements the sn\_agent\_initiated.AgentInitiatedMessagingUserDocument extension point is available for the Agent-Initiated Messaging Interface application. For more information, see [Associate user profiles with agent-initiated messages](https://www.servicenow.com/docs/access?context=agent-init-messg-user-record-ext-pt&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).

5.  Click **Compose Message**.

6.  On the form, fill in the fields.

<table id="table_phb_h3p_znb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Channel

</td><td>

Messaging channel that is installed with the application available for a service channel.For example, select **SMS** to send an SMS message. The SMS messaging channel is available when an administrator has installed the [Conversational SMS service channel](https://www.servicenow.com/docs/access?context=install-conversational-sms&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) application.

 An administrator can configure whether a messaging channel is available for agent-initiated messages. For more information, see [Determine whether messaging channels are available for agent-initiated messages](https://www.servicenow.com/docs/access?context=agent-init-messg-channel-ext-pt&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).

</td></tr><tr><td>

To

</td><td>

Recipient ID of the consumer or customer contact, or when both are not available the recipient ID of the user for which the interaction was opened. The recipient ID is pre-populated from the User \[sys\_user\] table record of the consumer, customer contact, or opened for user.If the entered ID is a phone number, it must be an E.164-compliant phone number or is automatically converted to the E.164 format. For more information, see [Phone number fields](https://www.servicenow.com/docs/access?context=c_UsePhoneNumberFields&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

 An administrator can configure the format of the recipient ID based on the selected channel and associate user profiles with agent-initiated messages. For more information, see [Validate recipient IDs for agent-initiated messages](https://www.servicenow.com/docs/access?context=agent-init-messg-validate-recipient&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US) and [Associate user profiles with agent-initiated messages](https://www.servicenow.com/docs/access?context=agent-init-messg-user-record-ext-pt&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).

 If you select **Other** from the To list, you can manually enter a ID of the consumer or customer contact. Any manually entered phone number is automatically converted to the E.164 format. For more information, see [Phone number fields](https://www.servicenow.com/docs/access?context=c_UsePhoneNumberFields&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

**Note:** The **Other** list value appears only when an administrator has configured the option to enter recipient ID manually for the messaging channel. For more information, see [Set up agent-initiated message interface for a messaging channel](https://www.servicenow.com/docs/access?context=agent-init-messg-setup&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).

</td></tr><tr><td>

From

</td><td>

Provider ID of the messaging channel.-   If there is only one provider configured for the channel, the From list is automatically set to the provider ID.
-   If there are multiple providers configured for the channel, you can select an ID in the From list.


</td></tr><tr id="agent-init-message"><td>

Message

</td><td>

Message to be sent to the recipient.

</td></tr><tr><td>

Attachment

</td><td>

File to be sent as an attachment. Click **Attach File** to browse and select a file.

 **Note:** By default, you can attach only images to the message.

</td></tr></tbody>
</table>7.  Click **Send**.


## Result

The interaction record of type messaging is created or updated based on the workflow as discussed in the following table.

<table id="table_vp2_ykk_gmb"><thead><tr><th>

Workflow

</th><th>

Results

</th></tr></thead><tbody><tr><td>

No active interaction​ record available

</td><td>

-   A new interaction record of type messaging for the channel is automatically created and assigned to the agent​.
-   The agent is added to the Live Group Profile \[live\_group\_profile\] table.

</td></tr><tr><td>

An active interaction record associated with a live agent​ exists

</td><td>

-   The interaction details are appended to the existing interaction record for the channel.
-   If the message was initiated by an agent not associated with the existing interaction record, the agent is added to the Live Group Profile \[live\_group\_profile\] table. However, there's no change in assignment of the interaction.

</td></tr><tr><td>

An active interaction record associated with the virtual agent​ exists

</td><td>

-   The existing interaction record with the virtual agent is closed.
-   A new interaction record of type messaging for the channel is automatically created and assigned to the agent​.
-   The agent is added to the Live Group Profile \[live\_group\_profile\] table.

</td></tr><tr><td>

An active interaction record associated with a different user exists

</td><td>

-   The existing interaction record with the earlier user is closed.
-   A new interaction record of type messaging for the channel is automatically created and assigned to the agent​.
-   The user profile associated with the existing interaction record is deactivated.
-   The user profile associated with the new interaction record is created.
-   The agent is added to the Live Group Profile \[live\_group\_profile\] table.

</td></tr></tbody>
</table>