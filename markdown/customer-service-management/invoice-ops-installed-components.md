---
title: Components installed with Case Management for Invoice Operations
description: Several types of components are installed with the Case Management for Invoice Operations application, including tables, roles, and service definitions.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Case Management for Invoice Operations, Case management, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Components installed with Case Management for Invoice Operations

Several types of components are installed with the Case Management for Invoice Operations application, including tables, roles, and service definitions.

## Tables

The Case Management for Invoice Operations application adds the following tables.

<table id="table_v3g_jhj_jcc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Invoice Case\[sn\_csm\_invoice\_case\]

</td><td>

Stores invoice case records. This table extends the Case \[sn\_customerservice\_case\] table.Records in the Invoice Case table use the prefix **INVCS**.

</td></tr><tr><td>

Invoice Case Line\[sn\_csm\_invoice\_case\_line\]

</td><td>

Stores the case line items created for invoice cases. This table extends the Case Line \[sn\_case\_line\] table.Requesters and fulfillers can use this table to capture the invoices and invoice lines as line items on an invoice case for which they want to resolve disputes, or make inquiries.

Records in the Order Case Line table use the prefix **INVCSL**.

</td></tr></tbody>
</table>The Case Management for Invoice Operations application also uses the following tables from the [Case lines and workflows](csm-case-mgmt-case-lines.md) application.

<table id="table_jcd_55l_fdc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Case Line\[sn\_case\_line\]

</td><td>

The Case Line table stores case line item records. This table extends the Task table.The prefix for case line records is **CSL**.

</td></tr><tr><td>

Case Line Characteristic\[sn\_case\_line\_characteristic\]

</td><td>

The Case Line Characteristic form displays details about a case line item on a case record.The prefix for case line characteristic records is **CSLC**.

</td></tr><tr><td>

Case Line Task\[sn\_case\_line\_task\]

</td><td>

The Case Line Task table stores the tasks related to case line items. This table extends the Case Task table.The prefix for case line task records is **CSLTASK**.

</td></tr></tbody>
</table>## Roles

The Case Management for Invoice Operations application includes roles that provide access to invoice cases and invoice case line items. It also updates some existing roles to provide this same access.

<table id="table_nyz_4s5_pdc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Includes roles

</th></tr></thead><tbody><tr><td>

Invoice case agent\[sn\_csm\_invoice.agent\]

</td><td>

The invoice case agent should have CRUD access to the invoice case header, invoice case line items, read-only access to invoices and invoice lines, products and product characteristics, accounts and contacts and assignment of invoice cases

</td><td>

-   sn\_customerservice\_agent
-   sn\_case\_line.characteristic\_delete
-   sn\_csm\_invoice.creator
-   sn\_csm\_invoice.writer
-   sn\_otc.ar\_invoice\_viewer
-   sn\_csm\_invoice.navigation\_menu

</td></tr><tr><td>

Invoice case manager\[sn\_csm\_invoice.manager\]

</td><td>

The invoice case manager should have all the access that invoice case agent has + manages agents + manager reports

</td><td>

-   sn\_csm\_invoice.agent
-   sn\_csm\_invoice.report\_viewer
-   sn\_customerservice\_manager
-   sn\_case\_line.characteristic\_report\_viewer

</td></tr><tr><td>

Invoice case task agent\[sn\_csm\_invoice.invoice\_case\_task\_agent\]

</td><td>

The invoice case task should have all the access to the case tasks assigned to the agent as well as read-only access to view the invoice case/invoice case lines, invoices/invoice lines that case task is associated with and also be able to update worknotes and comments

</td><td>

-   sn\_otc.ar\_invoice\_viewer
-   sn\_customerservice.case\_task\_agent

</td></tr></tbody>
</table>In addition to the persona roles, granular roles on invoice case header and invoice case lines are also needed.

<table id="table_z2w_3nt_pdc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Includes roles

</th></tr></thead><tbody><tr><td>

Invoice case viewer\[sn\_csm\_invoice.viewer\]

</td><td>

Read only access to invoice case, invoice case lines if access to invoice case, invoice case line characteristics if access to case line.Read access to invoice cases.

</td><td>

sn\_case\_line.characteristic\_viewer

</td></tr><tr><td>

Invoice case creator\[sn\_csm\_invoice.creator\]

</td><td>

Creating an invoice case with invoice case lines and invoice case line characteristics.Create access to invoice cases.

</td><td>

-   sn\_case\_line.characteristic\_creator
-   sn\_csm\_invoice.viewer

</td></tr><tr><td>

Invoice case writer\[sn\_csm\_invoice.writer\]

</td><td>

Editing an invoice case with invoice case lines if access to invoice case and invoice case line characteristics if access to case line.Write access to invoice cases.

</td><td>

-   sn\_case\_line.characteristic\_writer
-   sn\_csm\_invoice.viewer

</td></tr><tr><td>

Invoice case navigation menu\[sn\_csm\_invoice.navigation\_menu\]

</td><td>

Access the invoice case navigation menu item.Role to access the invoice case navigation menus.

</td><td>

 

</td></tr><tr><td>

Invoice case report viewer\[sn\_csm\_invoice.report\_viewer\]

</td><td>

Access to invoice case reports.Report viewer access to invoice cases.

</td><td>

 

</td></tr></tbody>
</table>## Service definitions and service definition categories

The Case Management for Invoice Operations application provides the following invoice case service definition: **Invoice Disputes**.

-   Type: Post-Sale
-   Table: Invoice Case \[sn\_csm\_invoice\_case\]
-   Products: All
-   Service definition category: Invoice

Agents can use this service definition to raise a dispute for one or more invoices or for specific lines on a single invoice.

This service definition belongs to the Invoice service definition category, which stores services for invoice-related issues. When creating an invoice case, agents can select this service definition in the [case type selector](csm-case-type-select-modals.md).

**Note:** The **Invoice Disputes** service definition is not active by default. To activate this service definition, the system administrator can:

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Service Definitions**.
2.  Filter the list to show service definitions from the Invoice Case \[sn\_invoice\_case\] table.
3.  Select **Invoice Disputes**.
4.  Enable the **Active** check box.

For more information about service definitions and categories, see the following topics:

-   [Service definitions](csm-service-definitions.md)
-   [Service definition categories](csm-service-definitions.md#section_e5p_mzw_jzb)

## Service level agreements \(SLAs\)

The Case Management for Invoice Operations application includes the following SLAs for the Invoice Case table \(sn\_csm\_invoice\_case\).

<table id="table_whd_wsq_qdc"><thead><tr><th>

SLA

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Initial Response Time for P1 and P2 cases

</td><td>

-   Start condition: State of the case is New and Priority is P1 or P2.
-   Stop condition: State is not New or Draft.
-   Schedule: None \(24x7\).
-   Duration: 4 hours.

</td></tr><tr><td>

Initial Response Time for P3 and P4 cases

</td><td>

-   Start condition: State of the case is New and Priority is P3 or P4.
-   Stop condition: State is not New or Draft.
-   Schedule: 8am-5pm weekdays excluding holidays.
-   Duration: 8 hours.

Duration: 8 hours.

</td></tr><tr><td>

Resolution SLA for P1 and P2 cases

</td><td>

-   Start condition: State of the case is New and Priority is P1 or P2.
-   Pause condition: State of the case is Awaiting information.
-   Resume condition: State of the case is not Awaiting information.
-   Stop condition: State of the case is Resolved.
-   Schedule: None \(24x7\)
-   Duration: 2 days.

</td></tr><tr><td>

Resolution SLA for P3 and P4 cases

</td><td>

-   Start condition: State of the case is New and Priority is P3 or P4.
-   Pause condition: State of the case is Awaiting information.
-   Resume condition: State of the case is not Awaiting information.
-   Stop condition: State of the case is Resolved.
-   Schedule: 8am-5pm weekdays excluding holidays.
-   Duration: ???.

</td></tr></tbody>
</table>## Invoice case type

The Case Management for Invoice Operations application includes the **Invoice** case type. This case type captures the case information for invoice-related issues.

In addition to the fields on the customer service case record, the Invoice Case table \[sn\_csm\_invoice\_case\] includes the following fields:

-   **Invoice number**: The invoice number that the invoice case has been opened for.
-   **Request source**: The source of the invoice case. Invoice cases can be created from the following sources:
    -   Specific invoice lines, single invoice
    -   Invoice header details, multiple invoices

For more information about case types, see [Customer service case types](customer-service-case-types.md).

To view the Invoice case type, navigate to **All** &gt; **Customer Service** &gt; **Case Types** &gt; **Manage Case Types** and select **Invoice**.

## Invoice case form views

The Case Management for Invoice Operations application includes form views to display invoice cases in CSM Configurable Workspace and in the Core UI.

This application uses the [CSM default record page](csm-default-record-page.md) to display Invoice case records in CSM Configurable Workspace.

Invoice cases include the following related lists:

-   Invoice Case Lines: Includes the individual case line records for this invoice case.
-   Tasks: Includes tasks that have been created for this invoice case.
-   Case Line Tasks: Includes tasks that have been created for individual case lines.

For more information, see the following topics:

-   [Invoice case form](../reference/invoice-case-form.md)
-   [Invoice case line form](../reference/invoice-case-lines-form.md)

## Invoice case archive rules

The Case Management for Invoice Operations application includes archive rules that archive older invoice cases.

<table id="table_bmp_vgp_2dc"><thead><tr><th>

Archive rule

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Archive Invoice Case

</td><td>

This rule archives invoice case records that have been closed for more than 2 years. Archiving these invoice case records also archives the following records:-   Invoice case tasks
-   Invoice case lines
-   Case line characteristics
-   Invoice case line tasks

</td></tr><tr><td>

Archive Invoice Case Line

</td><td>

This rule archives invoice case line records that have been closed for more than 2 years. Archiving these invoice case line records also archives the following records:-   Case line characteristics
-   Invoice case line tasks

</td></tr></tbody>
</table>Invoice case records that have been archived for more than five years are deleted. Deleting these records also deletes the following records:

-   Invoice case tasks
-   Invoice case line items
-   Case line characteristics
-   Invoice case line tasks

## Invoice case workflows

The Case Management for Invoice Operations application includes a subflow that provides the mapping between a customer invoice and an invoice case. The subflow **Primitives - AR Invoice to CSM Invoice case request** creates the data mapping between two different entities: 1\) the customer invoice and 2\) the invoice case.

For example, when mapping a customer invoice to an invoice case, the entities share some fields such as **Account** and **Contact**. The data mapping copies these field values from the customer invoice to the invoice case record.

To view this subflow, navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio** and select **Subflows** on the Workflow Studio homepage.

