---
title: Define email client recipient qualifiers
description: Create a configuration that controls the auto-complete list of recipients displayed in the email client.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Email client configurations, Configure, Email client, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Define email client recipient qualifiers

Create a configuration that controls the auto-complete list of recipients displayed in the email client.

## Before you begin

Role required: email\_client\_admin

## About this task

You can specify recipient qualifiers that display additional fields \(from a selected ServiceNow table\) in the auto-complete list. These fields differentiate email recipients who have the same first and last names.

Use the following tabs in the Email Client Recipient Qualifier form to define a recipient configuration.

-   **Display Configuration** – Set up the email recipient auto-complete behavior and optionally select additional fields to differentiate recipients who have the same name. The additional fields ensure that users select the proper recipient for an email.
-   **Query Configuration** – Specify a condition or script that queries the selected table and filters the recipient results returned.

You can define different recipient configurations, which can be used in an email client configuration.

## Procedure

1.  Navigate to **Email Client** &gt; **Email Client Recipient Qualifier** and select **New**.

2.  Fill in the fields at the top of the Recipient Qualifier form.

    |Field|Description|
    |-----|-----------|
    |Name|A unique name for this email client recipient configuration.|
    |Application|The type of scoped application.|
    |Table|The ServiceNow table to be queried for recipients.|
    |Description|A brief description of this recipient configuration.|
    | | |

3.  Fill in the fields in the **Display Configuration** tab to control the auto-complete display in the email client.

    |Field|Description|
    |-----|-----------|
    |Email Address|The field on the table that contains the recipient email address.|
    |Display Name|The field on the table used for the recipient name displayed.|
    |Order|The order of results returned relative to other recipient qualifiers defined.|
    |Additional Display Fields|A content list for choosing additional fields from the table to be displayed in the auto-complete list. Differentiates recipients who share the same name.|
    |Search Additional Fields|A check box for enabling additional fields to be searched. Expands the recipients returned in the auto-complete list by querying \(searching\) the **Additional Display Fields**.|

4.  Fill in the fields in the Query Configuration tab.

<table id="table_l5z_lck_zfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Prefix Search

</td><td>

Option to find the desired recipient using prefix.**Note:** Selecting the **Prefix Search** option displays the **Last Name Field** drop-down menu with options to filter the recipient's name.

</td></tr><tr><td>

Type

</td><td>

Select the method for filtering the recipients returned in the auto-complete list:-   Condition
-   Script


</td></tr><tr><td>

Conditions

</td><td>

If you selected Condition for the **Type**, use the condition builder to specify the conditions that must be met to return the appropriate recipients.

</td></tr><tr><td>

Script

</td><td>

If you selected Script for the **Type**, enter a script that uses these variables to return the appropriate recipients:-   *recipientQuery*: GlideRecord for the table being queried.
-   *targetRecord*: GlideRecord for the target record from which the email client was opened.
 For example, this recipientQuery is a GlideRecord that represents the Customer Contact table. The targetRecord variable is a Customer Service case from which the email client was opened. This query limits the email client auto-complete results to contacts who belong to the same account as the Customer Service case.

```
(function (recipientQuery, targetRecord) {
	
	 // Limit results to contacts belonging to the account for the case.
	 var account = targetRecord.getValue('account');
	 recipientQuery.addQuery('account', account);

})(recipientQuery, targetRecord);
```

</td></tr></tbody>
</table>5.  Select **Submit**.

    The recipient qualifier configuration is added to the Recipient Qualifier \[sys\_recipient\_qualifier\] table and is available for use in an email client configuration.


**Parent Topic:**[Email client configurations](../concept/email-client-configuration.md)

