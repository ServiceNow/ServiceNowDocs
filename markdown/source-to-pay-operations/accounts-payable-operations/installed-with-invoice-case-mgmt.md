---
title: Components installed with Invoice Case Management
description: Reference information for the roles, scheduled jobs, and tables installed with the Invoice Case Management plugin during activation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/installed-with-invoice-case-mgmt.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, invoice management, invoice case management, invoice automation]
breadcrumb: [Install Invoice Case Management, Configure, Accounts Payable Operations, Finance and Supply Chain]
---

# Components installed with Invoice Case Management

Reference information for the roles, scheduled jobs, and tables installed with the Invoice Case Management plugin during activation.

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

Creates an invoice inquiry case from the information in an inbound email.You must activate the flow to use it. For information on how to activate the flow, see [Activate the Create Inquiry Case on Invoice email flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/activate-inquiry-email-flow.md).

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
</table>-   **[Activate the Create Inquiry Case on Invoice email flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/activate-inquiry-email-flow.md)**  
Activate the **Create Inquiry Case on Invoice email** flow to automatically create invoice inquiry cases from inbound emails.

**Parent Topic:**[Install Invoice Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/install-invoice-case-mgmt.md)

