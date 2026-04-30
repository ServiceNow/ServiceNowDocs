---
title: Using CPQ user access management
description: Manage access to the ServiceNow CPQ Admin interface. Grant or remove admin rights and troubleshoot access issues.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-09-09"
reading_time_minutes: 2
breadcrumb: [ServiceNow CPQ admin settings, ServiceNow CPQ with other apps, Integrate, Sales Customer Relationship Management]
---

# Using CPQ user access management

Manage access to the ServiceNow CPQ Admin interface. Grant or remove admin rights and troubleshoot access issues.

The User Access utility allows managing access to selected areas of ServiceNow CPQ Admin. Admin users have full admin access unless their access level is modified via CSV import.

**Note:** The User Access utility is enabled via a support request.

ServiceNow CPQ Admins can control access to the ServiceNow CPQ Admin interface by granting admin access only to specific users. All existing users have admin access, which can be adjusted to end-user access as needed. New users automatically receive end-user access and need to be explicitly granted admin access by a user with admin access.

**Note:** If a message appears that says "An unknown error occurred" when you try to access ServiceNow CPQ Admin, admin access may not be toggled on. If you encounter this message, contact a user with ServiceNow CPQ admin access to enable your access.

## Setting up user access

Admin users can modify access via CSV upload \(Admin &gt; Utilities &gt; User Access\)

The User Access window displays the users currently in the system. To view a user's access, move the cursor over the user. The access is displayed in a tooltip.

To add, change, or delete users, create a CSV file and import the file into Admin Assist.

-   Username: Email address of the user, click to open a modal window for editing access. See 'Edit User' section, below.
-   Access: Level of access a user has, can be END\_USER or ADMIN,END\_USER
    -   END\_USER: Can create configurations using ServiceNow CPQ. This is for sales users, partners, and similar roles.
    -   ADMIN: Can access the administrative side of ServiceNow CPQ to create and modify blueprints, fields, rules, and other items.
-   Toggle Admin Access: Select one or more users using the check box. Toggle Admin Access adds or removes admin access for the selected users, depending on their current access level.
-   Import: At the bottom of the user access page is an exportable sample user access file. After making the necessary modifications to the exported file, you can import it using the **Import** button.

## Editing a user

Individual users can be edited by clicking their username in the table, which launches an Edit User window.

-   Username: email address of the user being edited.
-   Enable Admin Access: Toggle for controlling access to the Admin features of ServiceNow CPQ. The toggle to the right indicates that the user has Admin privileges.
-   Save / Cancel: Confirm any changes made or cancel to not save.

## Additional considerations

Users are created and show up on the User screen in ServiceNow CPQ the first time they access a ServiceNow CPQ instance and go through the authorization provider.

All existing users of a ServiceNow CPQ instance have END\_USER and ADMIN access. Admin access can be removed from users that do not require it.

Newly created users have END\_USER permissions only. The access level can be changed by an administrator following the above steps.

## Troubleshooting

-   Once granted access, new users may need to do one or mor of the following:
    -   Restart the browser
    -   Clear the browser cache
    -   Remove ServiceNow CPQ session cookies before accessing ServiceNow CPQ Admin
-   If users experience login issues after a CSV import, verify that the user names in the CSV match the case used in the user records. If ServiceNow CPQ is integrated with Salesforce, user names should be all lowercase to align with system requirements, as Salesforce does not allow user names to be uppercase.

    If necessary, edit the CSV so that user names are in lowercase, and import the user again.


