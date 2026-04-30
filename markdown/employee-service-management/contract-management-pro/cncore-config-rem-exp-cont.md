---
title: Configure reminders for expiring contracts
description: Configure reminders for expiring contracts that each business unit can use without the need to create their own.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Set up Contracts Core, Configure Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Configure reminders for expiring contracts

Configure reminders for expiring contracts that each business unit can use without the need to create their own.

## Before you begin

Ensure Contract Management Pro be installed:

Role required: sn\_cm\_core.contract\_admin

## Procedure

1.  Navigate to **All** &gt; **Contracts Core** &gt; **Contracts Administration** &gt; **Contract Repository Rules**.

2.  Set the condition for the notification to be sent.

    The available conditions are:

    -   Expired – The email notification reminder is not sent and the expiration level in the contract is set as **Expired**.
    -   within 7 days – The email notification reminder is sent seven days before the expiration of the contract.
    -   within 15 days – The email notification reminder is sent 15 days before the expiration of the contract.
    -   within 30 days – The email notification reminder is sent 30 days before the expiration of the contract.
    1.  On the Condition Checks page, find the entry whose **Table** field value is Legal Contracts Repository \(sn\_lg\_cnt\_repository\) and **Condition field** value is expiration\_level, and select **Contract** in the **Category** field.

    2.  In the Conditions section, select **New** to create a condition.

    3.  On the form, fill in the fields.

        For more information on fields, see [Expiring Contracts Condition form fields](../reference/cncore-email-notif-expcont-form.md).

    4.  Select **Submit**.

3.  Customize the message content in the default email notification template.

    1.  Select **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

    2.  Search for and select **Legal Contract Expiry Reminder**.

        If a message regarding the current application scope is displayed, select **here**.

    3.  In the Legal Contract Expiry Reminder window, select the **What it will contain** tab.

    4.  Enter the content for the email notification message in the **Message HTML** field.

    5.  Select **Update**.


## Result

After the configurations are complete, email notifications can be sent. For the four existing conditions, the email notification feature is provided out of the box and is automatically enabled for the following users:

-   Contract request.Requested for
-   Contract request.Opened by
-   Contract request.Assigned to

**Parent Topic:**[Set up Contracts Core](../concept/cncore-setup-cmpro.md)

**Related topics**  


[Create a contract type](cncore-create-contract-type.md)

[Create document template categories](cncore-create-doc-tmplt-cat.md)

[Enable users to view email details in activity stream](cncore-enbl-user-email-astream.md)

[Activate a system property to generate a certificate of completion](cncore-config-system-prop-COC.md)

[Configuring external applications for Contract Management Pro](../concept/cncore-set-ext-app-config.md)

[Configure extension point for notifications](cmpro-configure-action-extension-point-email-notification-admin.md)

[Use default email notifications](cmpro-send-receive-email-notification-admin.md)

[Auto-populate the start date and end date for contract requests](cncore-conf-start-end-date-for-cntrcts.md)

