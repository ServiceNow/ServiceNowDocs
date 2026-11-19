---
title: User access
description: Learn how to grant or revoke admin access for a user. Existing users have admin access by default, while new users have only end-user access.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/order-management/please\_share\_your\_feedback\_on\_admin\_assist\_responses.html
release: zurich
topic_type: reference
last_updated: "2025-10-08"
reading_time_minutes: 2
breadcrumb: [ServiceNow CPQ admin settings, ServiceNow CPQ with other apps, Integrate, Sales Customer Relationship Management]
---

# User access

Learn how to grant or revoke admin access for a user. Existing users have admin access by default, while new users have only end-user access.

ServiceNow CPQ Admins can control access to the Admin interface by granting admin access only to specific users. All existing users have admin access, which can be adjusted to end-user access as needed. New users automatically receive end-user access and need to be explicitly granted admin access by a user with admin access.

**Note:** If you try to access ServiceNow CPQ Admin without admin access enabled, you receive the message "An unknown error occurred." If you encounter this message, ask a user who has admin access to enable your access.

\[Omitted image "cpq-error-unknown.png"\] Alt text: Error message

## Managing user access

Configure user access by visiting Utilities &gt; User Access.

\[Omitted image "cpq-user-access-pane.png"\] Alt text: User access screen

1.  Username: Email address of the user. Click to edit \(see below\)
2.  Access: The level of access a user has \(END\_USER or ADMIN\)
    -   END\_USER: Can create configurations using ServiceNow CPQ. Typical for sales users, partners, and so on
    -   ADMIN: Can access the administrative side of ServiceNow CPQ to create and modify blueprints, fields, rules, and other objects
3.  Toggle Admin Access: Select one or more users using the checkbox. Toggle Admin Access adds or removes admin access for the selected users, depending on their current access level
4.  Import: At the bottom of the user access page is a sample user access file that can be exported. After making the necessary modifications to the exported file, you can import it using the "Import” button

To edit a user, click a username in the table.

\[Omitted image "cpq-user-access-edit-user.png"\] Alt text: Edit user screen

1.  Username: email address of the user being edited
2.  Enable Admin Access: Toggle for controlling access to the Admin features of ServiceNow CPQ. The toggle to the right indicates that the user has Admin privileges
3.  Save / Cancel – Confirm changes or cancel

**Note:**

-   Users are created and show up on the User screen in ServiceNow CPQ the first time they access a ServiceNow CPQ instance and go through the authorization provider.
-   All existing users of a ServiceNow CPQ instance have END\_USER and ADMIN access. Admin access can be removed from users that do not require it.
-   Newly created users have END\_USER permissions only. The access level can be changed by an administrator following the above steps.
-   If you need additional assistance, please contact support or log a case.

## Troubleshooting

If you have Area Based Access Controls enabled. see [ServiceNow CPQ: User Access Control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/logik_admin_user_access_control.md).

Before being able to access ServiceNow CPQ Admin, new users may need to restart their browser, clear their browser cache, or remove any ServiceNow CPQ session cookies.

If users experience login issues after a CSV import, verify that the user names in the CSV match the case used in the user records. If ServiceNow CPQ is integrated with Salesforce, user names should be all lowercase to align with system requirements. Salesforce does not allow uppercase in user names.

For example, suppose a user's name is lower case in Salesforce but was imported with an uppercase letter in ServiceNow CPQ, as in the following image.

\[Omitted image "cpq-user-access-troubleshooting-1.png"\] Alt text: User access

The user would face this issue on login with ServiceNow CPQ:

\[Omitted image "cpq-user-access-troubleshooting-2.png"\] Alt text: URL

After the user is reimported with the user name in the correct case, the issue is rectified.

\[Omitted image "cpq-user-access-troubleshooting-3.png"\] Alt text: List of Blueprints

