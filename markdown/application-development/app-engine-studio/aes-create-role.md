---
title: Build a new role for your application
description: Create a custom role for your application in App Engine Studio \(AES\).
locale: en-US
release: zurich
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Add application security, Enhance your app, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Build a new role for your application

Create a custom role for your application in App Engine Studio \(AES\).

## Before you begin

Role required: admin, security admin, or delegated\_developer \(with the **Security Management** permission\)

**Note:** If you are an admin, be sure to elevate your role.

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  From the My Apps page, open your application.

3.  In your application, next to Security, select the add icon \(![Add icon](../image/plus-icon.png)\).

4.  Select **Build a new role** and then select **Continue**.

    ![Option to build a new role](../image/build-new-role-purple.png "Option to build a new role")

5.  Enter a name and description for your role, and then select **Continue**.

    **Tip:** For consistency with existing role names, enter a role name that is all lower-case and uses underscores instead of spaces. For example, for an office art requester role, you would enter `office_art_requester`.

6.  For each table in your application, select one or more access controls for your role.

    -   **Create**

        Users with the role can create new records on the data table.

    -   **Read**

        Users with the role can read the data that is stored in the table.

    -   **Write**

        Users with the role can update existing records in the table.

    -   **Delete**

        Users with the role can delete table records.

7.  Select the **Experience** tab, and then select the experiences that users with the role can access.

8.  Select **Continue**, and then select **Done** on the summary screen.


**Parent Topic:**[Add application security](../concept/add-security.md)

