---
title: Configure email promotion rules for Activity Management
description: Configure email promotion rules to automatically process staged emails for manual association through the ServiceNow CRM for Outlook add-in or to trigger AI-powered auto-association with existing sales entities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/promote-crm-outlook-emails.html
release: australia
topic_type: task
last_updated: "2026-07-07"
reading_time_minutes: 2
breadcrumb: [Activity Management, Sales automation apps, Configure, Sales Customer Relationship Management]
---

# Configure email promotion rules for Activity Management

Configure email promotion rules to automatically process staged emails for manual association through the ServiceNow CRM for Outlook add-in or to trigger AI-powered auto-association with existing sales entities.

## Before you begin

**Note:** Configuring email promotion is required if you're on CRM Outlook Add-in application version 1.0.1.

Role required: admin

## About this task

Email promotion rules enable the following workflows for managing staged emails:

-   Manual email association: Agents use the ServiceNow CRM for Outlook add-in to associate emails with CRM records, triggering promotion from the Staged Email \[sys\_email\_staging\] table to the Email \[sys\_email\] table.
-   AI auto-association: When an agent receives an email with no existing CRM record association, the promotion rule triggers the AI sales activity association workflow to automatically match the email to a relevant sales entity \(Lead, Opportunity, Contact, or Account\) using semantic analysis and intent detection.

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

<table id="table-br-fields"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

&lt;business rule name&gt;For example, Trigger promotion rules on CRM emails.

</td></tr><tr><td>

Table

</td><td>

Staged Email \[sys\_email\_staging\]

</td></tr><tr><td>

Active

</td><td>

Selected

</td></tr><tr><td>

Advanced

</td><td>

Selected

</td></tr></tbody>
</table>    5.  In the **When to run** tab, enter the following values.

        |Field|Value|
        |-----|-----|
        |When|after|
        |Insert|Selected|
        |Update|Selected|
        |Filter Conditions|\[Target\] \[changes\] AND \[Target table\] \[changes\]|

    6.  In the **Advanced** tab, add the following values to trigger email promotion processing for staged CRM emails.

        |Field|Value|
        |-----|-----|
        |Condition|sn\_crm\_outlook.CRMOutlookAddinConstants.PROMOTED\_TABLE\_LIST\[current.target\_table\] == true &amp;&amp; !gs.nil\(current.instance\) &amp;&amp; gs.nil\(current.email\)|
        |Script|gs.eventQueue\("email\_staged.read", current\);|

        The script event initiates asynchronous processing to promote the staged email and trigger the appropriate association workflow.

        The following image shows the Advanced tab with Condition and Script fields populated.

        \[Omitted image "email-promotion-business-rule.png"\] Alt text: Advanced tab with Condition and Script fields populated.

    7.  Select **Submit**.


## Result

Staged emails that meet the specified conditions are processed according to the configured promotion rules. Promoted emails appear in the Emails tab on manually associated records or in the activity stream on AI-matched records.

**Related topics**  


[Classic Business rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/c_BusinessRules.md)

[Track emails linked from Microsoft Outlook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/view-associated-emails-crm.md)

