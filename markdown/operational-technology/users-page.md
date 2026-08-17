---
title: Users page
description: The Users page shows the lists of both active and inactive users in your Discovery Console for OT system. You can access the Discovery Console for OT through user accounts available in the system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/users-page.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use the Console pages, Discovery Console for OT, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Users page

The Users page shows the lists of both active and inactive users in your Discovery Console for OT system. You can access the Discovery Console for OT through user accounts available in the system.

## User overview

The following user accounts are available in the system.

-   Administrator accounts, which have full access to the Discovery Console for OT's functionality and features
-   Non-administrator accounts, which have limited access to the Discovery Console for OT

**Note:** Each user who needs access to the console is given a user account with private credentials. The Console application records user activity in the system. Sharing accounts or account passwords prevents an accurate audit of system activity.

## Registering the initial user

When the Discovery Console for OT is accessed for the first time after installation, the console guides the operator through the initial user registration process. The initial user account is created as an administrator account and has access to all features of the application.

The following sections describe how to create and register the initial user.

**Step 1: Accepting the End User License Agreement**

You must read and accept the End-User License Agreement \(EULA\) before you can set up the initial user. Confirm that an individual with legal authority and authorization has also reviewed the EULA before accepting the agreement.

**Step 2: Creating the Initial User**

After you accept the EULA, you're prompted to register the initial user. A username, password, and email address are required to complete the account setup. You must complete all of the fields before you can register the user.

The initial user is automatically assigned the administrator role and has full access to the system. Save the password for the initial user account in a secure place. The administrator account is necessary to create accounts for additional users.

**Note:** If all administrator accounts are inaccessible, contact your Discovery Console for OT representative for assistance.

## Managing user accounts

On the Users page, you can view all of the users in the system. Administrators are the only users that can list, create, or view information and update another user’s information in the system. Administrators can also force a user to change their password on their next log in.

To view a user's information, you can select the user on the Users page.

## User roles

When creating user accounts, you can assign the following roles.

**Note:** You can assign more than one role to a user.

|Role|Description|
|----|-----------|
|Admin|Can access the full functionality of the Discovery Console for OT. Can create, edit, and remove user accounts.|
|Reader|Can view the Discovery Console for OT with read-only permissions.|
|User|Can access the Discovery Console for OT with limited permissions.|

**Note:** For more information, see [Set up a Microsoft Entra ID](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/users-entra-id-setup.md) next.

-   **[Set up a Microsoft Entra ID](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/users-entra-id-setup.md)**  
This section describes how a Discovery Console for OT user can set up an **Microsoft Entra ID** integration.
-   **[Create a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/create-user-ot-console.md)**  
Create a user account that can access the Discovery Console for OT.
-   **[Edit a user's information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/edit-user-information.md)**  
Edit a User's information and keep the user account up to date.
-   **[Force a password reset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/reset-users-password.md)**  
Force a user to reset their password.
-   **[Deactivate a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/remove-user.md)**  
Deactivating a user verifies that they can't access the Discovery Console for OT.

**Parent Topic:**[Use the Discovery Console for OT pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/using-discovery-console.md)

