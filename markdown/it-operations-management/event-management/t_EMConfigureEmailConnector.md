---
title: Configure event collection from email
description: Configure an inbound email action to send email notifications when events and alerts are triggered.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure event collection from email

Configure an inbound email action to send email notifications when events and alerts are triggered.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

When you add an inbound email action to send email, Event Management uses inbound email actions to process inbound email in the same manner as any external event. The email content is used to generate and update events, use rules to generate alerts, or change event severity. The severity is updated after the impact calculation and stored in the em\_impact\_status table.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **Email Properties**.

2.  In the **Inbound Email Configuration** section, in the **Email receiving enabled** option, select **Yes** to enable the collection of events from email.

3.  To configure the email information to pass to Event Management for event and alert processing, navigate to **System Policy** &gt; **Email** &gt; **Inbound Actions** and in the list of Inbound Email Actions records search for and open the default **create event** form.

    1.  On the **Inbound Email Actions** form, specify these values.

        |Field|Value|
        |-----|-----|
        |Active|Select the check box to enable the email notification.|
        |Target table|Select **Event \[em\_event\]**.|
        |Action type|Select **Record Action**.|

    2.  Select the **Description** tab and enter a description for the email message.

    3.  Select the **Actions** tab and select these **Field Actions**.

        -   **\[Severity\] \[To\] \[&lt;the event severity&gt;\]**
        -   **\[Type\] \[From email\] \[&lt;portion of the email&gt;\]**

            For example, you can select **Subject** as the portion of the email to use.

4.  To customize the inbound parameters and map the text to event variables, add a **Script**.

    For example:

    ```
    
    current.source = 'email';
    current.event_class = 'email';
    current.description = email.body_text;
    current.time_of_event = new GlideDateTime();
    current.insert();
    
    ```

5.  From the instance, send an email that contains matching data, and then confirm that the event or alert information appears in Event Management.

    For more information sending email messages to create an instance, see [Inbound email actions](https://www.servicenow.com/docs/access?context=c_InboundEmailActions&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

    **Note:** Ensure that the user who sends the email has the role **evt\_mgmt\_integration**.

6.  Select **Submit**.


## Result

The inbound email is sent to the em\_event table and regular Event Management processes continue, for example, event rules and alert management rules run.

**Parent Topic:**[Configure Event Management connectors](../reference/connectors-and-listeners.md)

