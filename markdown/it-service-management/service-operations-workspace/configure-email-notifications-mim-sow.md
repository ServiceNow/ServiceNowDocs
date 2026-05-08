---
title: Configure email notifications in Major Incident Management
description: Configure the automated email notification alerts that are sent to major incident managers in the various stages of the major incident process. These stages include a change of state, assignment, or user group for a major incident.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Major Incident Management in Service Operations Workspace, Setting up Major Incident Management in Service Operations Workspace, Getting started with Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure email notifications in Major Incident Management

Configure the automated email notification alerts that are sent to major incident managers in the various stages of the major incident process. These stages include a change of state, assignment, or user group for a major incident.

## Before you begin

The Major Incident Management plugin must be activated in Service Operations Workspace. For more information, see [Activate Major Incident Management in Service Operations Workspace](install-mim-sow.md).

Consider the following items when you create or update a notification:

-   Your notification recipients must be active users and have a valid email address defined.

    ServiceNow® users or members of groups must be defined as active users in the User \[sys\_user\] table. They must also have a valid email address defined for their primary device in the Notification Device \[cmn\_notif\_device\] table. If users don’t have an active profile and a valid email address, they don’t receive notifications.

-   Your notification recipients must have the appropriate notification preferences enabled.

    Each user or group member must have the option to subscribe to the notification. They should have that option enabled in their notification preferences, along with the devices through which they want to receive the notification. Admins can impersonate users to review and configure their notification preferences. For more information, see Setting notification preferences in Core UI

-   To have your email notification also send as an SMS notification, recipients must subscribe to the notification on an SMS channel. For more information on creating an SMS channel, see Create notification channels.
-   After you create or update the notification, use the **Preview Notification** option to examine it. For example, you can test links that you have added and verify the notification recipients. For details, see Preview email notifications.

Role required: admin

## About this task

Use the following tabs in the Notification form to configure an email notification:

-   When to send — Conditions required to send the notification.
-   Who will receive — Recipients of the notification.
-   What it will contain — Contents of the notification.
-   What a digest will contain — Contents of the email digests if the notification can be delivered in a digest. For more information, see Email digests.

**Note:** If you don’t see all the fields on the form, select the **Advanced** view option in the related link section.

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace** &gt; **Configurations**.

2.  On the Admin Center page, navigate to the configuration page for Major Incident Management through either the **Overview** tab or the **Configurations** tab.

    -   In the **Overview** tab, select **Configure** for Major Incident Management.
    -   In the **Configurations** tab, select **Major Incident Management**.
    The configuration page displays all configurable features in Major Incident Management. In the Email notifications section, you can view the number of email notifications configured and in active status.

3.  On the Email notification section, select **Configure** to display the list of available email notifications.

4.  Select **New**.

5.  On the Notification form, fill in the fields.

    For a description of the field values, see Create an email notification.

6.  Select **Submit**.


## What to do next

Use the **Preview Notification** option to preview what notifications look like before you actually enable the instance to send them. For example, you can see:

-   How the **Subject** and **Message** fields are displayed.
-   Which users do or don’t receive the notification, including the reasons why the users don’t receive it.

For more information, see Preview email notifications.

