---
title: Create an email client configuration
description: Define a configuration that controls the display and behavior of the email client that is based on a selected ServiceNow table.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Email client configurations, Configure, Email client, Notifications, Configure core features, Administer]
---

# Create an email client configuration

Define a configuration that controls the display and behavior of the email client that is based on a selected ServiceNow table.

## Before you begin

Role required: email\_client\_admin

## About this task

The configuration determines the recipient auto-complete results that are displayed, email addresses that can be entered, and a set of allowable From addresses to be used when sending a message with the client.

You can create one email client configuration per ServiceNow table.

## Procedure

1.  Navigate to **Email Client** &gt; **Email Client Configuration** and select **New**.

2.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name for this email client configuration.|
    |Application|Type of scoped application.|
    |Active|Option that indicates that the configuration is active. The configuration is active by default.|
    |Table|ServiceNow table that this client configuration applies to. Select a table from the list.|

3.  In the Recipient Configuration section, select **Recipient Qualifiers** to be used for this client configuration.

    1.  Select the lock icon \(![Lock icon](../../localization-framework/image/lock-icon.png)\).

        By default, two types of recipients are available: Active Users with email accounts and Active Groups with email accounts.

    2.  Select the search icon \(![Search icon](../image/search-icon.png)\) and select a recipient configuration from the list of available recipient configurations.

    3.  Select the lock icon \(![Lock icon](../image/unlock-icon.png)\) to lock it.

4.  In the Display Configuration section:

    1.  Select the **Display From** option to display the From email address in the email client, or clear the check box to hide the From email address in the email client.

    2.  Select the **Display Reply-To** option to display the Reply To address in the email client, or clear the check box to hide the Reply To email address in the email client.

5.  In the Attachment Handling section, select from one of three choices for the **Attachment Send Action** field.

    |Option|Description|
    |------|-----------|
    |**Attach to Email Record**|Keep email client attachments on the Email \[sys\_email\] record when you send an email.|
    |**Attach to Target Record**|Attach email client attachments to the target record when you send an email. This option is the default value.|
    |**Conditionally Attach to Target Record**|Set conditions that define which email client attachments are moved to the target record when you send an email. Attachments that do not meet the conditions remain on the email record when you send an email.|

6.  In the Filter Configuration section, select **Email Address Filters** to be applied to the email client.

    1.  Unlock the lock icon \(![Lock icon](../image/unlock-icon.png)\).

    2.  Select the search icon \(![Search icon](../image/search-icon.png)\) and select one or more Email Address Filters.

    3.  Select the lock icon \(![Lock icon](../image/unlock-icon.png)\) to lock **Email Address Filters**.

    Each filter that you select evaluates a given email address and determines whether or not the given address is valid to apply to an outbound email.

7.  Click **Submit**.

    The configuration is added to the Email Client Configuration \[sys\_email\_client\_configuration\] table.


**Parent Topic:**[Email client configurations](../concept/email-client-configuration.md)

