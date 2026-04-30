---
title: System address filters
description: Prevent your system from communicating with untrusted domains and email addresses.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Advanced email setup, Configure email administration, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# System address filters

Prevent your system from communicating with untrusted domains and email addresses.

System address filters control who can communicate with your instance via email. You can improve email security by filtering domains and email addresses that you find suspicious.

For example, you might identify `example.com` as a suspicious domain. You can stop receiving emails from `example.com` by specifying the domain in a system address filter. You can also use another system address filter to prevent your system from sending emails to `example.com`.

There are two types of system address filters:

-   **Outbound**

    Controls which domains and email addresses can receive email from your instance.

-   **Inbound**

    Controls which domains and email addresses can send email to your instance.


When setting up system address filters, you can create one default outbound filter and one default inbound filter. A default outbound filter applies to all active SMTP email accounts automatically. A default inbound filter applies to all active IMAP or POP3 email accounts automatically.

To control senders and recipients for a specific email account, create a non-default filter and then apply it to the account.

## Before setup

Before you set up system address filters, consider doing the following:

-   Monitor your email to identify suspicious domains and email addresses.

    Using Security Center, you can monitor the blocked and allowed incoming email metrics for your instance. For more information, see [Designate untrusted and trusted email domains](https://www.servicenow.com/docs/access?context=designate-untrusted-trusted-email-domains&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

-   Designate someone to set up system address filters by assigning them the email\_account\_admin role.

## Setting up system address filters

To set up system address filters for your instance, complete the following tasks:

1.  [Set email address filters](../task/set-email-address-filters.md)

    Specify which domains and email addresses are allowed or disallowed.

2.  [Create a system address filter](../task/create-system-address-filter.md)

    Define how email address filters apply to inbound and outbound email.


## Next steps

After you set up system address filters, configure email filters for an added layer of security. Email filters enable you to ignore an inbound email or move it to a particular mailbox. For more information on configuring email filters, see [Email filters](c_EmailFilters.md).

-   **[Set email address filters](../task/set-email-address-filters.md)**  
Specify which domains and email addresses are allowed or disallowed.

**Parent Topic:**[Advanced email setup](../../reference-pages/concept/c_AlternateEmailConfigurations.md)

