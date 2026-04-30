---
title: Modify email notification layout
description: Modify the email notification layout and template that is shipped with the Employee Experience Foundation \(com.snc.sn\_ex\_emp\_fd\) plugin.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Admin configurations, Configure, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Modify email notification layout

Modify the email notification layout and template that is shipped with the Employee Experience Foundation \(com.snc.sn\_ex\_emp\_fd\) plugin.

## Before you begin

Role required: admin

## About this task

Apply the layout to email notifications to elevate the look and feel, and deliver branded notifications.

**Note:** The Employee Experience Foundation \(com.snc.sn\_ex\_emp\_fd\) plugin is installed as a dependent plugin with Employee Center or Employee Center Pro. However, you can still independently install the plugin from ServiceNow Store.

The Employee Experience Foundation \(com.snc.sn\_ex\_emp\_fd\) plugin is shipped with the following.

-   Employee notification layout: Provides a Next Experience themed layout to apply to the email templates for all employee facing notifications. This layout includes best practices, standards, and styles. Use the following layout items:
    -   Header
    -   Footer
    -   Unsubscribe and Change preference links
    -   Easily modifiable brand logos
    -   Web Responsiveness
-   Employee notification template: Provides a template for Email notification layout to create reusable content for the subject line and message body. Apply the template to employee facing notifications to deliver consistent information.

View the following examples to understand how the notification looks with and without the Email notification layout.

-   **With layout**
-   **Without the layout**

**Note:** If you are an upgrade customer, to use the latest email layout, install the Employee Experience Foundation \(com.snc.sn\_ex\_emp\_fd\) app from ServiceNow® Store.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

2.  Search for the notification that you want to apply the template.

3.  Click open the notification and check if it is **Active**.

4.  On the **What it will contain** tab, select search and apply the `Email notification template` for **Email template**.

    To modify the template body, logo or any other details follow the steps.

    1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Templates**

    2.  Open the **Email layout** record to modify it.

    3.  Make your changes and **Save** or **Update** the record.

5.  Modify the email body or use it as given.

6.  **Preview Notification** and click **Update**.


## What to do next

Reuse the Employee notification layout for any of your templates to build consistent notifications.

**Related topics**  


[Configure the mail and SMS send to self](deskless-kiosk-sendtoself-sms-email.md)

