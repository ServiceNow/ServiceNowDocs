---
title: Compose an SMS message from a chat in HR Service Delivery Agent Workspace
description: Create and send an outbound SMS message to a recipient directly from a chat interaction. Access interactions assigned to you to follow up via SMS message when you need more details from the employee.
locale: en-US
release: australia
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [SMS conversations in HR Service Delivery Agent Workspace, Using Agent Workspace for HR Case Management, Agent Workspace, HR Service Delivery, Employee Service Management]
---

# Compose an SMS message from a chat in HR Service Delivery Agent Workspace

Create and send an outbound SMS message to a recipient directly from a chat interaction. Access interactions assigned to you to follow up via SMS message when you need more details from the employee.

## Before you begin

Role required: sn\_hr\_core.case\_writer

## About this task

An interaction is a request for assistance made through chat, phone, or in person. Interaction records are automatically created when you are using agent chat.

The **Compose SMS** option is only enabled for active chat interactions. For more information about interactions in HR Service Delivery, refer to .

## Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **HR Agent Workspace**.

2.  Select the ![List icon](../reference/images/IconList.png) HR case list icon and navigate to **Interactions** &gt; **Assigned to me**.

3.  Select an active chat interaction for which you would like to respond to the recipient via an SMS message.

4.  In the chat interaction modal, click the ![more options menu item](../../../common/image/icon-ellipses.png) more options icon and select **Compose SMS** to initiate an SMS conversation with the recipient.

    The **Send via SMS** modal launches with **Send from** and **Send to** fields.

5.  Use the drop-down **Send to** field to select the SMS recipient.

    You can choose an automatically populated phone number or choose **Other** to enter the phone number manually in the **Other number** field. Automatically populated phone numbers display based on the following criteria:

    The **Opened for** field is populated on the interaction with phone number.

    The phone numbers as specified on the HR Profile record. The label for each phone number on the **Send via SMS** modal will match the label for the **Phone number** field on HR Profile record.

    If a manually added phone number is not associated with an existing active channel user profile record, the record is created automatically when you send the SMS message.

    **Note:** When an interaction is created with phone number p1, not associated with an existing HR Profile, a channel user profile is be created as a Guest. When the user updates an HR Profile, HRP1, with a phone number p1, the user is treated as HRP1.

6.  Compose the SMS message, add an attachment if necessary, and send to the employee.

    You can also select the ![HR Agent Workspace - Quick action icon](../reference/images/quick-action-icon.png) quick action icon, or enter a back slash \(/\) in the chat area, to use quick actions for SMS messaging. See [Agent Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/agent-chat/ci-agent-chat-exploring.md) for more information.

    You will receive a confirmation when the SMS message is sent. Click the confirmation to view the interaction details,if desired.

    **Note:** For complete details regarding initiating SMS conversations in Agent Workspace, refer to [Agent initiated SMS conversation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/agent-initiated-sms-store-app.md). For details about using Agent Workspace with HR Service Delivery, refer to .


