---
title: User self-registration
description: The User Registration Request \[com.snc.user\_registration\] plugin provides the ability for unregistered users to request access to a ServiceNow instance. An administrator can activate the plugin.When a user submits a self-registration form, an admin can review and approve it.Admins can enable users to self-register. Enable automatic approval of such accounts to streamline user registration.
locale: en-US
release: australia
product: User Administration
classification: user-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Creating users, Creating users, companies, departments, User administration, Configure core features, Administer the ServiceNow AI Platform]
---

# User self-registration

The User Registration Request \[com.snc.user\_registration\] plugin provides the ability for unregistered users to request access to a ServiceNow instance. An administrator can activate the plugin.

A user can request an account by navigating to the instance. If the plugin is installed, the following section is added to the welcome screen.

![Welcome screen](../image/WelcomeScreen.png)

The user can complete and submit the self-registration form, and see a confirmation that it was submitted. The user receives an email when the account is registered.

**Note:** If the email address entered in the self-registration form is already in the system, the request is not submitted.

**Parent Topic:**[Creating users](../../roles/concept/ua-creating-users.md)

## Approve a self-registered user account

When a user submits a self-registration form, an admin can review and approve it.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Pending User Registrations** and open the request.

2.  Use the **Create User** and **Reject** related links on the registration request form to approve or deny the request.

    -   If **Create User** is selected, a new user is created using the email address as the **User ID**.
    -   If **Reject** is selected, the request is marked **Rejected**.
    If the request was accepted, the user is sent an email notification with the login information. If it was denied, the user is sent an email with the rejection information.


## Enable automatic self-registered user account approval

Admins can enable users to self-register. Enable automatic approval of such accounts to streamline user registration.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **System Properties** &gt; **System**.

2.  Select **Enable auto processing of user registration request**

3.  Select **save**

    If enabled, registration requests do not require approval. Instead, the business rule **Auto-Process User Registration** creates the user record from the information provided.


### What to do next

Request activation of the [Explicit Roles](https://www.servicenow.com/docs/access?context=explicit-roles&version=australia&pubname=australia-platform-security&ft:locale=en-US) \(`com.glide.explicit_roles`\) plugin. The Explicit Roles plugin creates two roles to differentiate between internal and external users.

