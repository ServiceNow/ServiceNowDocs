---
title: Set email address filters
description: Specify which domains and email addresses are allowed or disallowed.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [System address filters, Advanced email setup, Configure email administration, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Set email address filters

Specify which domains and email addresses are allowed or disallowed.

## Before you begin

Role required: email\_account\_admin

## About this task

You can specify two types of email address filters:

-   Allow List: A list of allowed domains and email addresses
-   Deny List: A list of disallowed domains and email addresses

You can also specify exceptions to the allowed or disallowed domains and email addresses.

## Procedure

1.  Navigate to **System Mailboxes** &gt; **Administration** &gt; **Email Address Filters**, and then select **New**.

2.  Enter the **Name** of the address filter.

3.  Select the filter **Type**:

    -   Allow List: Allow all specified domains. All other domains are disallowed.
    -   Deny List: Disallow all specified domains. All domains that don’t match the denied list domains are allowed.
4.  In the **Domains** field:

    1.  Select the lock icon to unlock it and access the domains controlled by this filter.

    2.  Select an existing domain or enter a new domain:

        -   If the filter **Type** is Allow List, select the Search icon. Select the domains for which all email addresses are allowed. To add a new domain, select **New**, enter the **Domain**, and select **Submit**.
        -   If the filter **Type** is Deny List, select the Search icon. Select the domains for which all email addresses are disallowed. To add a new domain, select **New**, enter the **Domain**, and select **Submit**.
        **Note:** You can specify a wildcard \(\*\) in the domain name, for example`*.com`. If you create an email configuration that has multiple email address filters, all the filters evaluate the given email addresses. The filters determine whether the addresses are valid and the message can be sent as outbound email.

        By default, the maximum number of domains that you can associate with an email address filter is 100. You can reconfigure this limit by setting the **glide.email\_address\_filter.max\_domains** property.

    3.  Select the lock icon to lock the **Domains** field.

5.  Specify any email addresses that are **Exceptions** to the domains specified in Step 4.

    1.  Select the lock icon to open the Email Address Filter Exceptions \[sys\_email\_address\_filt\_except\] table.

    2.  Click the search icon to choose an existing email address.

    3.  To add a new email address, select **New**, enter the email address exception, and select **Submit**.

        **Note:** You can specify a wildcard \(\*\) in an email address exception.

        By default, the maximum number of exceptions that you can associate with an email address filter is 1000. You can reconfigure this limit by setting the **glide.email\_address\_filter.max\_exceptions** property.

    4.  Select the lock icon to lock the **Exceptions** field.

        The exception is added to the Email Address Filter Exceptions \[sys\_email\_address\_filt\_except\] table.

6.  Select **Submit**.

    The email address filter is added to the Email Address Filters \[sys\_email\_address\_filter\] table.


## Email address filter

**Note:** After the email address filter is added to the Email Address Filters \[sys\_email\_address\_filter\] table, [Create an email client configuration](create-email-client-config.md).

![Allowed exception in the email address filter and how it appears in the email client.](../image/whitelist-example.png "Email address filter — allowed exception example")

**Note:** Domain name should not contain @ symbol.

![Disallowed exception in the email address filter and how it appears in the email client.](../image/blacklist-example.png "Email address filter — disallowed exception example")

## Example

![Allowed exception in the email address filter and how it appears in the email client.](../image/whitelist-example.png "Email address filter — allowed exception example")

![Disallowed exception in the email address filter and how it appears in the email client.](../image/blacklist-example.png "Email address filter — disallowed exception example")

## What to do next

Apply the email address filter to a system address filter. For more information, see [Create a system address filter](create-system-address-filter.md).

**Parent Topic:**[System address filters](../concept/system-address-filters.md)

