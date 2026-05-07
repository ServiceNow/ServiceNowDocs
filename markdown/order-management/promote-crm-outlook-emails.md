---
title: Make emails associated through the CRM Outlook Add-in visible to agents
description: Configure email promotion so that emails associated with CRM records through the ServiceNow CRM for Outlook add‑in are promoted from the Staged Email \[sys\_email\_staging\] table to the Email \[sys\_email\] table, making them visible to agents in the workspace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Activity Management, Lead and opportunity management apps, Configure, Sales Customer Relationship Management]
---

# Make emails associated through the CRM Outlook Add-in visible to agents

Configure email promotion so that emails associated with CRM records through the ServiceNow CRM for Outlook add‑in are promoted from the Staged Email \[sys\_email\_staging\] table to the Email \[sys\_email\] table, making them visible to agents in the workspace.

## Before you begin

**Note:** Configuring email promotion is required if you're on CRM Outlook Add-in application version 1.0.1.

Role required: admin

## Procedure

1.  Log in to your ServiceNow instance.

2.  Add a promotion rule.

    1.  Set the application scope to **Global**.

    2.  Navigate to **All** &gt; **User Mailboxes** &gt; **Promotion Rules**.

    3.  Select **New**.

    4.  On the form, fill in the fields.

<table id="table-promotion-rule"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

&lt;promotion rule name&gt;

</td></tr><tr><td>

Condition

</td><td>

\(current.target\_table == "&lt;table\_name&gt;"\) &amp;&amp; !gs.nil\(current.instance\)

 For example, \(current.target\_table == "sn\_lead\_mgmt\_core\_lead"\) &amp;&amp; !gs.nil\(current.instance\)

</td></tr><tr><td>

Promotion strategy

</td><td>

Promote and run Triggers

</td></tr></tbody>
</table>    5.  Select **Submit**.

3.  Create a business rule on the Staged Email \[sys\_email\_staging\] table.

    1.  Set the application scope to **Global**.

    2.  Navigate to **All** &gt; **System Definition** &gt; **Business Rules**.

    3.  Select **New**.

    4.  On the form, fill in the fields.

        |Field|Value|
        |-----|-----|
        |Name|&lt;business rule name&gt;|
        |Table|Staged Email \[sys\_email\_staging\]|
        |Active|Selected|
        |Advanced|Selected|

    5.  In the **When to run** tab, enter the following values.

        |Field|Value|
        |-----|-----|
        |When|after|
        |Insert|Selected|
        |Filter Conditions|\[Target\] \[is anything\] AND \[Target table\] \[is anything\]|

    6.  In the **Advanced** tab, add the following line in the **Script** field to trigger email promotion processing for staged emails.

        ```
        gs.eventQueue("email_staged.read", current);
        ```

        This event initiates asynchronous processing for the staged email record. It triggers the promotion logic that moves emails from the staging table to the Emails \[sys\_email\] table, ensuring all staged emails are processed successfully after the UID duplication issue is resolved.

        The following image shows the complete **Script** field value.

        ![Script field value after adding the eventQueue system event.](../image/email-promotion-business-rule.png)

    7.  Select **Submit**.


## Result

When an agent associates an email with a CRM record through the Microsoft Outlook add-in, the business rule fires and promotes the email from the Staged Email \[sys\_email\_staging\] table to the Email \[sys\_email\] table. The email then appears in the Emails tab on the associated Lead, Opportunity, or Account record.

**Related topics**  


[Classic Business rules](https://www.servicenow.com/docs/access?context=c_BusinessRules&version=australia&pubname=australia-build-workflows&ft:locale=en-US)

[Track emails linked from Microsoft Outlook](view-associated-emails-crm.md)

