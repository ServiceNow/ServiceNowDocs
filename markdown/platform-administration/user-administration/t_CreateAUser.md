---
title: Create a user
description: You can add a user to your instance to enable them to log in and use designated application features.
locale: en-US
release: yokohama
product: User Administration
classification: user-administration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Creating users, Creating users, companies, and departments, User administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a user

You can add a user to your instance to enable them to log in and use designated application features.

## Before you begin

Role required: user\_admin

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="t_CreateUserFields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User ID

</td><td>

Create a unique identifier for this user's ServiceNow login user name. Typical examples of user IDs are `cwitherspoon` and `charlie.witherspoon`. You can’t create a user whose User ID duplicates an existing user. If you do import duplicates from an update set, the more recently created name takes the duplicate User ID.

</td></tr><tr><td>

Given name

</td><td>

Enter the user's given \(often their first\) name.

</td></tr><tr><td>

Family name

</td><td>

Enter the user's family name \(often their last name\). **Note:** You can clear the **First Name** field, or the **Last Name** field in an existing user record, but you can’t clear both at the same time.

</td></tr><tr><td>

Title

</td><td>

Enter a title or job description, or select one from the list.

</td></tr><tr><td>

Department

</td><td>

Select the user's department from the list.

</td></tr><tr><td>

Password

</td><td>

Assign a password to the user. To set up the user's password, fill in the fields on the form and **save** the record. Then, select **Set Password**. This password can be permanent or temporary.

</td></tr><tr><td>

Password needs reset

</td><td>

Select this check box to require the user to change the password during the first login.

</td></tr><tr><td>

Locked out

</td><td>

Select this check box to lock the user out of the instance and terminate all their active sessions. The system helps prevent users with the admin role from locking themselves out.

</td></tr><tr><td>

Active

</td><td>

Select this check box to make this user active. Only the administrator sees an inactive user in: -   Lists of users
-   The selection list on reference fields \(magnifying glass icon\)
-   The auto-complete list that appears when you type into a reference field


</td></tr><tr><td>

Web service access only

</td><td>

It designates a user as a non-interactive user. This field is available with [Non-Interactive Sessions](../concept/c_NonInteractiveSessions.md#).**Note:** The Web service access only check box is automatically enabled when you select **Machine** in the Identity type field. The Web service access only check box is automatically disabled when you select **Human** or **AI**.

</td></tr><tr><td>

Internal Integration User

</td><td>

Select this check box to [Mark service accounts as internal integration users](https://www.servicenow.com/docs/access?context=t_MarkSvcAcctsAsInternalIntegUsers&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

</td></tr><tr><td>

Email

</td><td>

Enter the user's email address. To enter a non-standard email address that doesn’t pass field validation, you must deactivate the validation script first:

1.  Navigate to **System Definition** &gt; **Validation Scripts**.
2.  Select the **email** record.
3.  Clear the **Active** check box and save the change.
4.  Complete the user profile, including the email address, and update or submit the record.
5.  Reactivate the email validation script.


</td></tr><tr><td>

Identity type

</td><td>

Select the user identity type based on the user:-   Human - Select this for a real person, such as an employee, customer, or admin.
-   Machine - Select this for a non-human system or device, such as a server, application, or service account that makes automated requests.
-   AI - Select this for an autonomous AI-driven system. AI users should be used when an AI agent or agentic workflow needs permissions greater than that of the invoking user.

See [Security for AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information on using AI Agent type users.

**Note:** The Web service access only check box is automatically enabled when you select **Machine** in the Identity type field. The Web service access only check box is automatically disabled when you select **Human** or **AI**.

</td></tr><tr><td>

Language

</td><td>

Select your preferred language from the list.

</td></tr><tr><td>

Calendar integration

</td><td>

Select **Outlook** to have this user receive meeting notifications via email directly to the calendar. Otherwise, select **None**.

</td></tr><tr><td>

Time zone

</td><td>

Select the user's time zone.

</td></tr><tr><td>

Date format

</td><td>

Select the user's preferred format for dates.

</td></tr><tr><td>

Business phone

</td><td>

Enter the user's business phone number.

</td></tr><tr><td>

Mobile phone

</td><td>

Enter the user's mobile phone number.

</td></tr><tr><td>

Photo

</td><td>

Attach a photo of the user, if appropriate.

</td></tr></tbody>
</table>    The minimum fields required to create a user record are: **User ID** and either **First name** or **Last name**.

    You can select the **Personalize Form** icon to remove fields.

4.  Add **Roles**, **Groups**, **Delegates**, **Skills**, and **Subscriptions** to the user.

    For more information, see [Managing roles](../../roles/concept/ua-creating-roles.md), [Creating groups](../../roles/concept/ua-creating-groups.md), and [Delegating roles](../../roles/concept/c_DelegateRoles.md).

5.  Select **Submit**.

    The new user record appears in the list.


**Parent Topic:**[Creating users](../../roles/concept/ua-creating-users.md)

