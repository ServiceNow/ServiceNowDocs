---
title: Specify an outbound email address for a particular language
description: You can specify a different email address for each language your instance supports.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create an email notification, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Specify an outbound email address for a particular language

You can specify a different email address for each language your instance supports.

## Before you begin

Role required: admin

## Procedure

1.  Create or copy a notification record for the desired event.

2.  In the **What will it contain** section, enter a new email address in the **From** field.

3.  Create the **Subject** and **Message** content in the desired language.

4.  In the **When to send** section, create a condition as follows:

    1.  In the list of **Condition** fields, select **Show Related Fields** from the bottom of the choice list.
    2.  From the choice list of **Related Fields**, select the field that identifies the recipient.

        For example, select **Caller** &gt; **User** fields to send the notification to the user who called in an incident, or **Assigned to** &gt; **User** fields to send the notification to the user to whom an incident is assigned.

    3.  From the choice list of user fields, select **Language**.
    4.  Select the **is** operator.
    5.  Complete the condition by selecting the language of the desired user.
5.  Click **Update**.

    All notifications for that event originate from the specified email address and go out in the language of the recipient.


**Parent Topic:**[Create an email notification](t_CreateANotification.md)

