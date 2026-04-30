---
title: Enable automatic user creation
description: An administrator can set an email property to automatically create users from incoming email. The administrator provides a list of trusted domains to prevent untrusted users from being automatically created.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Inbound email, Notifications, Configure core features, Administer]
---

# Enable automatic user creation

An administrator can set an email property to automatically create users from incoming email. The administrator provides a list of trusted domains to prevent untrusted users from being automatically created.

## Before you begin

Role required: admin

## About this task

For example, you can prevent email from users outside your company domain from creating incidents. When an instance receives a message and there is no matching email address from the sender, the instance can create a user with the User ID \[sys\_user.user\_name\] set to the sender's full email address.

Users in your instance must still have write and update access to the records that they create or update through inbound email actions.

**Note:** To learn more about the **glide.user.trusted\_domain** property, which affects automatic email creation, see Restrict emails by domain for user creation \(instance security hardening\) in the Instance Security Hardening Settings.

|Value of email.from Variable|User ID Created|Email Address|Name|
|----------------------------|---------------|-------------|----|
|new.user@company.com|new.user@company.com|new.user@company.com|New User|
|"New User" &lt;new.user@company.com&gt;|new.user@company.com|new.user@company.com|New User|
|"User, New" &lt;new.user@company.com&gt;|new.user@company.com|new.user@company.com|New User|
|"User" &lt;nuser@company.com&gt;|nuser@company.com|nuser@company.com|User|

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **Email Properties**.

2.  Select the check box for **Automatically create users for incoming email from trusted domains** \(**glide.pop3readerjob.create\_caller**\).

    ![Automatically creating users](../image/AutomaticallyCreateUsersFOrIncomingEmailsFromTrustedDomains.png)

3.  Enter the list of trusted domains in **Trusted domains for creating users from incoming emails** \(**glide.user.trusted\_domain**\).

    ![Trusted domains](../image/TrustedDomainsForCreatingUsersFromIncomingEmails.png)

    **Note:**

    -   The **glide.user.trusted\_domain** property prevents user creation if the sender is not from a trusted domain. However, the system may still process inbound actions for emails that are received from the domain. To have the system ignore these emails, set up a system address filter. For more information on setting up system address filters, see [System address filters](../concept/system-address-filters.md). You can also prevent untrusted users from triggering inbound actions by locking out the guest user.
    -   The **glide.user.trusted\_domain** property does not accept wildcarded domains or values such as:
        -   \*.edu
        -   \*.net
        -   .edu
        -   .net
4.  Click **Save**.

5.  Complete the following steps to lock out the guest user.

    1.  Navigate to **User Administration** &gt; **Users** and select the user **guest**.

    2.  Select the **Locked out** field to disable the guest account.


## What to do next

When the property **glide.pop3readerjob.create\_caller** is set to **false**, the instance runs inbound actions from users who do not match an existing user by impersonating the guest user.

If the property **glide.pop3readerjob.create\_caller** is set to **true**, but a user has a valid email address associated with a non-primary device, the instance creates a new user record for that email address if there is no matching email address in the Users \[sys\_user\] table. The instance does not validate non-primary email addresses against the Notification Devices \[cmn\_notif\_device\] table.

The method the instance uses to create users can be upgraded to use the full email address by activating the Email Automatic User Creation plugin.

The plugin sets the property **glide.email.create\_userid\_from\_email** to **true** by default. After activating the plugin, enable automatic user creation from email.

**Note:** The **glide.email.create\_userid\_from\_email** is not used by the system when the record is created using record producer or created manually.

**Warning:** Review your existing user records to reconcile any that contain identical email addresses. If you activate the plugin prior to reconciling email addresses, your instance cannot distinguish between users with identical email addresses and randomly selects one of the users with the matching email address.

**Parent Topic:**[Configure inbound email actions](../concept/configure-inbound-email.md)

