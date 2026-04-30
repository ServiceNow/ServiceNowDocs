---
title: Remove a developer
description: Removing a user as a developer prevents the user from developing, changing, or deploying the application in the current instance.
locale: en-US
release: yokohama
product: Delegated Development and Deployment
classification: delegated-development-and-deployment
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Delegate development and deployment permissions to personnel, Using Delegated Development, Delegated Development, Planning your application, Building applications]
---

# Remove a developer

Removing a user as a developer prevents the user from developing, changing, or deploying the application in the current instance.

## Before you begin

Role required: admin or application administrator

If [Application administration](../concept/application-administration.md) is enabled, only an application administrator of the target application can delegate developers to an application. If application administration is not enabled, an admin user can delegate developers.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **Applications**.

2.  Select the application name of the application from which you are removing developers.

    The system opens the application record.

3.  Select **Manage Developers**.

    **Note:** If the App Collaboration Component is installed, the link appears as **Manage Collaborators**.

    The system displays the Developer Permissions window.

4.  Point to the developer you want to remove.

    The system displays a minus icon next to the developer name.

    ![Manage developers](../image/RemoveDeveloper.png)

5.  Select the minus icon next to the developer name.

    The system removes the developer and any associated application roles.


