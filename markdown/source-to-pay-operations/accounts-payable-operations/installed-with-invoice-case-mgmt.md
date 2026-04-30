---
title: Components installed with Invoice Case Management
description: Several types of components are installed with activation of the Invoice Case Management plugin, including user roles, scheduled jobs, and tables.
locale: en-US
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Install Invoice Case Management, Configure, Accounts Payable Operations, Finance and Supply Chain]
---

# Components installed with Invoice Case Management

Several types of components are installed with activation of the Invoice Case Management plugin, including user roles, scheduled jobs, and tables.

## Roles installed

<table id="table_obx_pbp_ywb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Invoice Case Management Administrator \[sn\_ap\_cm.admin\]

</td><td>

Can configure and make changes to record producers, invoice case assignment rules, invoice case SLA definitions, and email properties.

</td><td>

-   sla\_admin
-   sn\_ap\_cm.agent

</td></tr><tr><td>

Invoice Case Management Agent \[sn\_ap\_cm.agent\]

</td><td>

Can view, create, and update invoice cases and tasks and manage the workflows for fulfilling requests.

</td><td>

-   sn\_ap\_cm.requester
-   sla\_manager
-   workspace\_user
-   vendor\_reader
-   canvas\_user
-   sn\_ap\_cm.task\_owner
-   email\_composer

</td></tr><tr><td>

Invoice Case Management Requester \[sn\_ap\_cm.requester\]

</td><td>

Can create invoice inquiry cases.

</td><td>

sn\_shop.invoice\_owner

</td></tr><tr><td>

Invoice Case Management Task Owner\[sn\_ap\_cm.task\_owner\]

</td><td>

Can view and update the tasks that are assigned to them.

</td><td>

None

</td></tr></tbody>
</table>## Scheduled jobs installed

<table id="table_qbx_pbp_ywb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create Inquiry Case on Invoice email

</td><td>

Creates an invoice inquiry case from the information in an inbound email.You must activate the flow to use it. For information on how to activate the flow, see [Activate the Create Inquiry Case on Invoice email flow](../task/activate-inquiry-email-flow.md).

</td></tr></tbody>
</table>## Tables installed

<table id="table_sbx_pbp_ywb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Invoice case \[sn\_ap\_cm\_ap\_case\]

</td><td>

Extends the Service Case table. Stores the invoice case records.

</td></tr><tr><td>

Invoice task \[sn\_ap\_cm\_ap\_task\]

</td><td>

Extends the Service Task table. Stores the invoice task records.

</td></tr></tbody>
</table>-   **[Activate the Create Inquiry Case on Invoice email flow](../task/activate-inquiry-email-flow.md)**  
Activate the **Create Inquiry Case on Invoice email** flow to automatically create an invoice inquiry case based on the information in an inbound email.

**Parent Topic:**[Install Invoice Case Management](../task/install-invoice-case-mgmt.md)

**Related topics**  


[Work with invoices](../concept/work-with-invoices.md)

[Work on an invoice inquiry case](../task/work-inquiry-case.md)

[Create an invoice inquiry case manually](../task/create-inquiry-case.md)

