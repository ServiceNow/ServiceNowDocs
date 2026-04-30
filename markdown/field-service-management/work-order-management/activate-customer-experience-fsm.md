---
title: Activate Field Service Management Customer Experience
description: Activate the Field Service Management Customer Experience plugin \(com.snc.fsm\_customer\_experience\) to use the Customer Experience feature with Field Service Management.
locale: en-US
release: xanadu
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Field Service Management Customer Experience, Setting up work orders and tasks, Configuring Field Service Management, Field Service Management]
---

# Activate Field Service Management Customer Experience

Activate the Field Service Management Customer Experience plugin \(com.snc.fsm\_customer\_experience\) to use the Customer Experience feature with Field Service Management.

## Before you begin

Role required: wm\_admin

## About this task

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

    Provides support for enabling and configuring customer SMS and email notifications For more information about activating Notify, see [Notify](https://www.servicenow.com/docs/access?context=notify-landing-page&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).


The following items are installed with Field Service Management Customer Experience:

-   Tables
-   Properties
-   Business rules

For more information, see [Customer Experience components](../reference/customer-experience-components.md).

## Procedure

1.  Navigate to **All** &gt; **Application** &gt; **System Definition** &gt; **Plugins**.

2.  Search for the plugin com.snc.fsm\_customer\_experience.

3.  Click **Activate**.


