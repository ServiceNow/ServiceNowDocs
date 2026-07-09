---
title: Configure conditions to send reminder notifications for expiring contracts
description: Configure contract repository rules to determine the expiration conditions under which reminder notifications for expiring contracts are sent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/employee-service-management/contract-management-pro/cncore-config-rem-exp-cont.html
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure additional features in CM Pro, Configuring Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Configure conditions to send reminder notifications for expiring contracts

Configure contract repository rules to determine the expiration conditions under which reminder notifications for expiring contracts are sent.

## About this task

Email notifications are available for the following contract expiration conditions in the base system:

-   Expired – The email notification reminder is not sent and the expiration level in the contract is set as Expired.
-   within 7 days – The email notification reminder is sent seven days before the expiration of the contract.
-   within 15 days – The email notification reminder is sent 15 days before the expiration of the contract.
-   within 30 days – The email notification reminder is sent 30 days before the expiration of the contract.

You can update the contract repository rule to modify or add expiration conditions that determine when the notification email is sent.

## Before you begin

Role required: sn\_cm\_core.contract\_admin

## Procedure

1.  Navigate to **All** &gt; **Contracts Core** &gt; **Contracts Administration** &gt; **Contract Repository Rules**.

2.  Set the condition for the notification to be sent.

    1.  On the Condition Checks page, find the entry whose **Table** field value is Legal Contracts Repository \(sn\_lg\_cnt\_repository\) and **Condition field** value is expiration\_level, and select **Contract** in the **Category** field.

    2.  In the Conditions section, select **New** to create a condition.

    3.  On the form, fill in the fields.

        For more information on these fields, see [Expiring Contracts Condition form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/contract-management-pro/cncore-email-notif-expcont-form.md).

    4.  Select **Submit**.

3.  Customize the message content in the default email notification template.

    1.  Select **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

    2.  Search for and select **Legal Contract Expiry Reminder**.

        If a message regarding the current application scope is displayed, select **here**.

    3.  In the Legal Contract Expiry Reminder window, select the **What it will contain** tab.

    4.  Enter the content for the email notification message in the **Message HTML** field.

    5.  Select **Update**.


**Parent Topic:**[Configure additional features in Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/contract-management-pro/cmpro-additional-feature.md)

**Related topics**  


[Configuring Contract Workspace with UI Builder components]()

[Configure signature pause duration when modifying signatories]()

[Auto-populate the start date and end date for contract requests]()

[Activate a system property to generate a certificate of completion]()

[Enable users to view email details in activity stream]()

[Enable keyword search for contract templates]()

[Configuring contract summarization for Contract Management Pro]()

[Copy fields from parent request to amendment request]()

[Manage notifications in Contract Management Pro]()

