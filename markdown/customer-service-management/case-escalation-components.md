---
title: Case and account escalation components
description: The roles, modules, and tables installed with the case and account escalation feature.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Case and account escalation, Administer, Customer Service Management]
---

# Case and account escalation components

The roles, modules, and tables installed with the case and account escalation feature.

## Roles

Roles included with the case and account escalation feature.

<table id="table_c5m_z5h_lbb"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Escalation requester \(sn\_customerservice.escalation\_requester\)

</td><td>

Can request an escalation for a case or account.

</td></tr><tr><td>

De-escalation requester \(sn\_customerservice.deescalation\_requester\)

</td><td>

Can de-escalate a case or account. This role contains the sn\_customerservice.escalation\_requester role.

</td></tr><tr><td>

Account Data Manager \(sn\_crm\_account\_data\_manager\)

</td><td>

Can request, view, update and delete an escalation for an account.

</td></tr><tr><td>

Escalation Configuration Viewer \(sn\_crm\_escalation\_config\_viewer\)

</td><td>

Can view all the escalation records, and Escalation Templates, and Escalation Severity modules.

</td></tr><tr><td>

Escalation Administrator \(sn\_crm\_escalation\_admin\)

</td><td>

-   Can create, update, view, and delete an escalation for an account escalation, escalation template, escalation severity.
-   Can request an escalation for a case or account.
-   Can de-escalate an account.

 This role contains Escalation requester \(sn\_customerservice.escalation\_requester\), De-escalation requester \(sn\_customerservice.deescalation\_requester\), and Escalation Configuration Viewer \(sn\_crm\_escalation\_config\_viewer\) roles.

</td></tr></tbody>
</table>## Escalation modules

The case and account escalation feature adds the Escalations module to the Customer Service menu:

-   **All**: lists all escalation records for cases and accounts.
-   **Escalation Templates**: lists the case and account escalation templates.
-   **Escalation Severity**: lists the types of escalation severity.

This feature also adds a list of escalated cases to the Customer Service menu: **Customer Service** &gt; **Cases** &gt; **Escalated**

## Tables

Tables included with the case and account escalation feature:

<table id="table_yhw_kvh_lbb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Escalation Templates\[sn\_customerservice\_escalation\_template\]

</td><td>

Stores escalation template records.

</td></tr><tr><td>

Escalations \[sn\_customerservice\_escalation\]

</td><td>

Stores records created for escalated cases and accounts.

</td></tr><tr><td>

Escalation Severities\[sn\_customerservice\_escalation\_severity\]

</td><td>

Stores escalation severity definition records.

</td></tr></tbody>
</table>