---
title: Initiate SMS conversations from CSM Agent Workspace
description: Compose an SMS message from CSM Agent Workspace to interact with a customer contact or a consumer regarding customer service cases.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Using CSM Configurable Workspace in Customer Service Management, Manage cases, Using Customer Service Management, Customer Service Management]
---

# Initiate SMS conversations from CSM Agent Workspace

Compose an SMS message from CSM Agent Workspace to interact with a customer contact or a consumer regarding customer service cases.

## Before you begin

Role required: agent\_workspace\_user

Ensure that an administrator has configured the Conversational SMS Integration with Twilio application. For more information, see [Conversational SMS Integration with Twilio](https://www.servicenow.com/docs/access?context=sms-twilio-store-app&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Workspace Experience** &gt; **Workspaces** &gt; **Agent Workspace Home**.

2.  On the Agent Workspace Home page, navigate to **Agent Workspace** &gt; **Lists** &gt; **Interactions** &gt; **My Interactions**.

3.  In the My Interactions list, modify an existing interaction or create another interaction.

    -   To modify an existing interaction, select the interaction number in **Number** column of the My Interactions list.
    -   To create another interaction, click **New** in the My Interactions list.
4.  On the Details tab of the workspace form, fill in the details for a new interaction or modify the details.

    For more information about the form, see [CSM workspace form features](../../../administer/workspace/reference/csm-agent-workspace-agent-actions.md).

    **Note:** The user profile associated with an interaction is configured by an administrator by using the AgentInitiatedConversationUtil extension point. By default, the AgentInitiatedMessagingUtilExtPointImpl script include that implements the AgentInitiatedConversationUtil extension point is available for the Conversational SMS Integration with Twilio application. For more information, see [Associate user profiles on messaging interactions](https://www.servicenow.com/docs/access?context=associate-user-profiles-messaging-interactions&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

5.  Click **Compose SMS**.

6.  On the form, fill in the fields.

<table id="table_phb_h3p_znb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

From

</td><td>

Provider phone number of the SMS channel.-   If there is only one provider phone number, the From list is automatically set to the provider phone number.
-   If there are multiple providers configured for the SMS channel, you can select a phone number in the From list.


</td></tr><tr><td>

To

</td><td>

Phone number of the consumer or customer contact. The phone number is in the E.164 format and automatically set to the phone number of the consumer or customer contact associated with the interaction record.

 By default, the user profiles for consumers and customer contacts and the format of their phone numbers are validated for the SMS channel.

 If you select **Other** from the To list, you can manually enter a phone number of the consumer or customer contact. Any manually entered phone number is automatically converted to the E.164 format. For more information, see [Phone number fields](https://www.servicenow.com/docs/access?context=c_UsePhoneNumberFields&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

</td></tr><tr id="agent-init-message"><td>

Message

</td><td>

Message to be sent to the consumer or customer contact.

</td></tr><tr id="agent-init-attachment"><td>

Attachment

</td><td>

File to be sent as an attachment. Click **Attach File** to browse and select a file.

 **Note:** By default, you can attach only images to the message. However, an administrator can configure the Attachment API to upload more file types. For more information, see [Attachment - POST /now/attachment/upload](https://www.servicenow.com/docs/access?context=c_AttachmentAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

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

-   A new interaction record of type messaging for the SMS channel is automatically created and assigned to the agent​.
-   The agent is added to the Live Group Profile \[live\_group\_profile\] table.

</td></tr><tr><td>

An active interaction record associated with a live agent​ exists

</td><td>

-   The interaction details are appended to the existing interaction record for the SMS channel.
-   If the message was initiated by an agent not associated with the existing interaction record, the agent is added to the Live Group Profile \[live\_group\_profile\] table. However, there's no change in assignment of the interaction.

</td></tr><tr><td>

An active interaction record associated with the virtual agent​ exists

</td><td>

-   The existing interaction record with the virtual agent is closed.
-   A new interaction record of type messaging for the SMS channel is automatically created and assigned to the agent​.
-   The agent is added to the Live Group Profile \[live\_group\_profile\] table.

</td></tr><tr><td>

An active interaction record associated with a different user exists

</td><td>

-   The existing interaction record with the earlier user is closed.
-   A new interaction record of type messaging for the SMS channel is automatically created and assigned to the agent​.
-   The user profile associated with the existing interaction record is deactivated.
-   The user profile currently associated with the new interaction record is created.
-   The agent is added to the Live Group Profile \[live\_group\_profile\] table.

</td></tr></tbody>
</table>