---
title: Change access settings for a role
description: Control the application permissions for a role in App Engine Studio \(AES\).
locale: en-US
release: zurich
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Add application security, Enhance your app, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Change access settings for a role

Control the application permissions for a role in App Engine Studio \(AES\).

## Before you begin

Role required: admin, sn\_app\_eng\_studio.user, or delegated\_developer

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  From the My Apps page, open your application.

3.  Next to a role, select the menu icon \(![](../image/menu-icon.png)\) and then select **Edit**.

    ![Editing a role](../image/edit-role.png "Editing a role")

    A new tab opens to edit the role.

4.  In the Experience section, select the experiences that users with the role can access.

5.  In the Data section, set the access controls for each available table.

    -   **Create**

        Users with the role can create new records on the data table.

    -   **Read**

        Users with the role can read the data that is stored in the table.

    -   **Write**

        Users with the role can update existing records in the table.

    -   **Delete**

        Users with the role can delete table records.

6.  Select **Save**.


**Parent Topic:**[Add application security](../concept/add-security.md)

