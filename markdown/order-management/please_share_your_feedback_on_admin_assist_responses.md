---
title: User access
description: Learn how to grant or revoke admin access for a user. Existing users have admin access by default, while new users have only end-user access.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CPQ admin settings, CPQ with other apps, Integrate, Sales Customer Relationship Management]
---

# User access

Learn how to grant or revoke admin access for a user. Existing users have admin access by default, while new users have only end-user access.

CPQ Admins can control access to the Admin interface by granting admin access only to specific users. All existing users have admin access, which can be adjusted to end-user access as needed. New users automatically receive end-user access and need to be explicitly granted admin access by a user with admin access.

**Note:** If you try to access CPQ Admin without admin access enabled, you receive the message "An unknown error occurred." If you encounter this message, ask a user who has admin access to enable your access.

![Error message](../images/cpq-error-unknown.png)

## Managing user access

Configure user access by visiting Utilities &gt; User Access.

![User access screen](../images/cpq-user-access-pane.png)

1.  Username: Email address of the user. Click to edit \(see below\)
2.  Access: The level of access a user has \(END\_USER or ADMIN\)
    -   END\_USER: Can create configurations using CPQ. Typical for sales users, partners, and so on
    -   ADMIN: Can access the administrative side of CPQ to create and modify blueprints, fields, rules, and other objects
3.  Toggle Admin Access: Select one or more users using the checkbox. Toggle Admin Access adds or removes admin access for the selected users, depending on their current access level
4.  Import: At the bottom of the user access page is a sample user access file that can be exported. After making the necessary modifications to the exported file, you can import it using the "Import” button

To edit a user, click a username in the table.

![Edit user screen](../images/cpq-user-access-edit-user.png)

1.  Username: email address of the user being edited
2.  Enable Admin Access: Toggle for controlling access to the Admin features of CPQ. The toggle to the right indicates that the user has Admin privileges
3.  Save / Cancel – Confirm changes or cancel

**Note:**

-   Users are created and show up on the User screen in CPQ the first time they access a CPQ instance and go through the authorization provider.
-   All existing users of a CPQ instance have END\_USER and ADMIN access. Admin access can be removed from users that do not require it.
-   Newly created users have END\_USER permissions only. The access level can be changed by an administrator following the above steps.
-   If you need additional assistance, please contact support or log a case.

**Related topics**  


[Using CPQ user access management](cpq-using-uam.md)

[User Access Control reference](../reference/cpq-user-access-control-ref.md)

