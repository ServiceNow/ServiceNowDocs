---
title: Compose an SMS conversation
description: An agent can compose an SMS to interact with a customer for resolving various issues. If the interaction is not messaging type, you see the Compose SMS option.
locale: en-US
release: australia
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Compose an SMS conversation

An agent can compose an SMS to interact with a customer for resolving various issues. If the interaction is not messaging type, you see the **Compose SMS** option.

## Before you begin

Role required: agent\_workspace\_user

A provider is configured for SMS messaging type channel.

## About this task

As an agent, you can compose and send an SMS to an ongoing interaction which is not messaging type.

## Procedure

1.  Click **Compose SMS**.

    The Send via SMS screen is displayed.

2.  Select a phone number from the **Send from:** drop-down list.

    -   If there is only one provider phone number this field is pre-populated with the number.
    -   If there are multiple provider profiles available for SMS channels, you can choose from the drop-down list.
3.  Select a phone number from the **Send to:** drop-down list.

    -   The phone numbers are pre-populated from the consumer or contact records.
    -   If both are not populated, the system looks for the number from the opened for record in the sys\_user table.
    -   If there is already a channel user profile associated with a consumer or contact, the phone number is pre-populated.
    1.  Choose **Other** and select a phone number in the drop-down list.

    **Note:** All phone numbers must be in the E.164 format. For more information, about phone number and channel user profile validation, see [Phone number validation](../concept/agent-initiated-sms-store-app.md#phone_number_profile_validation).

    If there is already an ongoing SMS type of interaction with the same or different consumer, you can view the interaction card in the same screen. The interaction card for the consumer number you have selected contains interaction number, message type, last updated time, consumer, and assigned to information.

4.  Enter your message in the **Message** field.

5.  Click **Attach file**, browse, select the file and attach.

    **Note:** You can attach only image files to the message. For more information about the REST API for uploading attachments, see [Attachment - POST /now/attachment/upload](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/c_AttachmentAPI.md).

6.  Click **Send**.

    For more information, see [Agent initiated SMS conversations](../concept/agent-initiated-sms-store-app.md#section_ung_ccm_3mb).


