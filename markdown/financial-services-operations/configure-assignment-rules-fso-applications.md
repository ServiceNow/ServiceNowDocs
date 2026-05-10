---
title: Configure assignment rules
description: Configure rules to automatically assign cases to specific agents or groups based on the rule conditions. You can either modify predefined assignment rules or create new ones.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Financial Services Operations \(FSO\)]
---

# Configure assignment rules

Configure rules to automatically assign cases to specific agents or groups based on the rule conditions. You can either modify predefined assignment rules or create new ones.

## Before you begin

Role required: Based on the application that you are configuring, you need the following roles:

-   For Financial Services Payment Operations: sn\_bom\_payment.admin and admin
-   For Financial Services Card Operations: sn\_bom\_card.admin and admin
-   For Financial Services Complaint Management: sn\_bom\_compl.admin and admin
-   For Financial Services Business Deposit Operations: sn\_bom\_deposit\_b2b.admin and admin
-   For Financial Services Personal Deposit Operations: sn\_bom\_deposit\_b2c.admin and admin
-   For Financial Services Business Loan Operations: sn\_bom\_loan\_b2b.admin and admin
-   For Financial Services Personal Loan Operations: sn\_bom\_loan.b2c\_admin and admin
-   For Financial Services Business Lifecycle: sn\_bom\_clo\_b2b.admin and admin
-   For Financial Services Client Lifecycle: sn\_bom\_clo\_b2c.admin and admin
-   For Financial Services Treasury Operations: sn\_bom\_treasury.admin and admin
-   For Commercial Lines Claims: sn\_ins\_claim\_cml.admin and admin

    **Note:** Insurance Special Investigations is installed with Commercial Lines Claims, and additionally requires the following roles: sn\_ins\_siu.admin and admin

-   For Individual Life Servicing and Individual Life Underwriting: sn\_ins\_policy\_b2c.admin and admin
-   For Group Life Servicing and Group Life Underwriting: sn\_ins\_policy\_b2b.admin and admin
-   Individual Life Claims: sn\_ins\_claim\_indl.admin and admin
-   Insurance claims: sn\_ins\_gen\_claim.admin and admin

## About this task

When you create an assignment rule, you select the following:

-   The table for the task type and the conditions that must be met before the task is assigned.
-   The user or the group that the task is assigned to.

Alternately, you can create a script to further customize the assignment rule.

Review the assignment rules that are installed with the Financial Services Operations applications.

|Application|Assignment rule|Table|
| | | |
|-----------|---------------|-----|
|---|---|---|
|Financial Services Payment Operations|Payment Inquiry Assignment Rule|sn\_bom\_payment\_inquiry|
|Inquiry Task|sn\_bom\_payment\_inquiry \_task|
|Claim|sn\_bom\_payment\_claim|
|Debit Approval|sn\_bom\_payment\_service|
|Financial Services Card Operations|Credit Card Service|sn\_bom\_credit\_card\_service|
|Credit Card Task|sn\_bom\_credit\_card\_task|
|Credit Task|sn\_bom\_credit\_asmt\_task|
|Document Service|sn\_bom\_document\_task|
|Financial Services Business Loan Operations|Loan Service – Business|sn\_bom\_loan\_b2b\_service|
|Loan Task – Business|sn\_bom\_loan\_b2b\_task|
|Credit Service – Business|sn\_bom\_credit\_asmt\_loan\_b2b\_service|
|Credit Task – Business|sn\_bom\_credit\_asmt\_b2b\_task|
|Document Service – Business|sn\_bom\_document\_b2b\_task|
|Financial Services Personal Loan Operations|Loan Service|sn\_bom\_loan\_service|
|Loan Task|sn\_bom\_loan\_task|
|Credit Service|sn\_bom\_credit\_asmt\_loan\_service|
|Credit Task|sn\_bom\_credit\_asmt\_task|
|Document Service|sn\_bom\_document\_task|
|Financial Services Business Lifecycle|Account Lifecycle Service|sn\_bom\_clo\_b2b\_account\_service|
|Contact Lifecycle Service|sn\_bom\_clo\_b2b\_contact\_service|
|Account Lifecycle Service Task|sn\_bom\_clo\_b2b\_account\_task|
|Contact Lifecycle Service Task|sn\_bom\_clo\_b2b\_contact\_task|
|Financial Services Client Lifecycle|Customer Lifecycle Service|sn\_bom\_clo\_b2c\_service|
|Customer Lifecycle Task|sn\_bom\_clo\_b2c\_task|
|Financial Services Treasury Operations|RDC Service|sn\_bom\_treasury\_rdc\_service|
|Wire Service|sn\_bom\_treasury\_wire\_service|
|Treasury Task|sn\_bom\_treasury\_task|
|Individual Life Claims|Individual life claim service|sn\_ins\_claim\_indl\_death\_case|
|Individual life claim task|sn\_ins\_claim\_indl\_death\_task|
|Related death policy claim service|sn\_ins\_claim\_indl\_rel\_death\_case|
|Insurance claims|Travel claim case|sn\_ins\_gen\_claim\_case|
|Travel claim baggage adjuster task|sn\_ins\_gen\_claim\_adj\_task|
|Travel claim trip adjuster task|sn\_ins\_gen\_claim\_adj\_task|

For advanced assignment rules, you can also use the ServiceNow Advanced Work Assignment \(AWA\) feature to automatically assign work items to agents, based on their availability, capacity, and optionally, skills. For more information, see [Advanced Work Assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-overview.md).

## Procedure

1.  Navigate to **All** &gt; **Routing and Assignment** &gt; **Assignment Rule**.

2.  Create an assignment rule or modify an existing rule.

    -   To create a rule, click **New**.
    -   To review an existing rule, filter the list to show the rules for the application tables and then open a rule.
3.  On the form, fill in the fields.

    For information about the Assignment Rule form fields, see [Create an assignment rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/t_AssignmentModuleRule.md).

4.  Click **Submit** or **Update**.


