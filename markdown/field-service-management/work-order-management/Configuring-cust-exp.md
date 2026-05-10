---
title: Configuring Field Service Management Customer Experience
description: Configure the Field Service Management Customer Experience application to enable sending notifications to your customers through email and SMS.Activate the Field Service Management Customer Experience plugin \(com.snc.fsm\_customer\_experience\) to use the Customer Experience feature with Field Service Management.Set up notification messages and emails to update customers about the status of their work order tasks.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up work orders and tasks, Configure, Field Service Management]
---

# Configuring Field Service Management Customer Experience

Configure the Field Service Management Customer Experience application to enable sending notifications to your customers through email and SMS.

## Configuration Overview

The steps for setting up Field Service Management Customer Experience are:

1.  [Activate Field Service Management Customer Experience](Configuring-cust-exp.md#)

    Activate the Field Service Management Customer Experience plugin \(com.snc.fsm\_customer\_experience\) to use the Customer Experience feature with Field Service Management.

2.  [Customer notifications for work order tasks](Configuring-cust-exp.md#)

    Set up notification messages and emails to update customers about the status of their work order tasks.


## Activate Field Service Management Customer Experience

Activate the Field Service Management Customer Experience plugin \(com.snc.fsm\_customer\_experience\) to use the Customer Experience feature with Field Service Management.

### Before you begin

Role required: wm\_admin

### About this task

The Field Service Management - Customer Experience plugin \(com.snc.fsm\_customer\_experience\) includes demo data and activates these related plugins if they are not already active.

<table id="table_xcn_jxw_jyb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Customer Service with Field Service Management.\[com.snc.csm\_fsm\_integration\].

</td><td>

Provides an integration between the Customer Service Management and Field Service Management applications.

</td></tr><tr><td>

Notify - Twilio Direct Driver\[com.snc.notify.twilio\_direct\].

</td><td>

Provides APIs and workflow activities for applications to handle various notification features, such as SMS.

</td></tr></tbody>
</table>Field Service Management Customer Experience requires the following plugins. Ensure that these plugins are activated before you install Field Service Management Customer Experience.

-   **Notify**

    Provides support for enabling and configuring customer SMS and email notifications For more information about activating Notify, see [Notify](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/notify/notify-landing-page.md).


The following items are installed with Field Service Management Customer Experience:

-   Tables
-   Properties
-   Business rules

For more information, see [Customer Experience components](../reference/customer-experience-components.md).

### Procedure

1.  Navigate to **All** &gt; **Application** &gt; **System Definition** &gt; **Plugins**.

2.  Search for the plugin com.snc.fsm\_customer\_experience.

3.  Click **Activate**.


## Customer notifications for work order tasks

Set up notification messages and emails to update customers about the status of their work order tasks.

Customers can receive notifications about the work order tasks created for them. Customers can unsubscribe to stop receiving any notifications.

Customer notifications for work order tasks use the Field Service Management - Customer Experience plugin to send both SMS and email notifications on the registered mobile number and email address. Users with the system administrator role can enable and configure customer SMS and email notifications. For more information, see [Notify Twilio Direct driver](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/notify/Notify-TwilioDirectDriver.md).

Customers are notified when one of the following activities is performed to the work order task:

-   Work order task is created
-   Work order task is assigned
-   Work order task is reassigned
-   Work order task is rescheduled
-   Work order task is completed
-   Work order task is canceled
-   Agent starts to travel to the work order task location
-   Agents reaches to the work location
-   Appointment booking is confirmed
-   Appointment booking is rescheduled
-   Appointment booking is canceled

