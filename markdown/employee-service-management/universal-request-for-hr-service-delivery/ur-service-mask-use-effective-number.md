---
title: Use effective number in email subject
description: Modify the email subject to display the relevant ticket number by using the task effective number. For example, if your service ticket is associated with a universal request, then you must mask the service ticket number and show the UR number.
locale: en-US
release: yokohama
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Email notification preferences for your service, Unified ticket experience setting, Configure service to use Universal Request, Setting up and configuring Universal Request, Universal Request, Employee Service Management]
---

# Use effective number in email subject

Modify the email subject to display the relevant ticket number by using the task effective number. For example, if your service ticket is associated with a universal request, then you must mask the service ticket number and show the UR number.

## Before you begin

Role required: admin

## About this task

The **task\_effective\_number** is a dynamic field value that displays the UR number when the service ticket is associated with UR and displays the actual service ticket number when there is no UR associated.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Notifications**.

2.  Open your service specific notification that you want to customize.

3.  In the **When it will contain** tab, in the **Subject** field use the **task\_effective\_number**.

    For example, in the Incident Opened and Unassigned notification, in the **Subject** field, enter **Incident $\{task\_effective\_number\} - open and unassigned**.

    ![Use effective number in email subject](../images/ur-effective-number.png)

4.  Click **Update**.


**Parent Topic:**[Email notification preferences for your service](../concept/ur-customize-email-notifcations.md)

