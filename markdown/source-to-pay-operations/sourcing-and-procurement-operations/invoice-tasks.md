---
title: Invoice tasks
description: Invoice tasks, an extension of acknowledgment tasks, lists invoice tasks in the Open, Work in Progress, and Closed Rejected status.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Sourcing and Purchasing Automation, Exploring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Invoice tasks

Invoice tasks, an extension of acknowledgment tasks, lists invoice tasks in the Open, Work in Progress, and Closed Rejected status.

**Note:** If you are a new customer, or an existing customer who has upgraded and installed the Shopping Hub \(sn\_spend\_uib\) plugin, these tasks aren't applicable for you. However, if you choose to continue with the existing Source-to-Pay Common Architecture \(sn\_shop\) plugin and skip the Shopping Hub plugin, these tasks are available for you to work on.

When an invoice acknowledgment is triggered, a task is created against the invoice and displayed as an Invoice Task related list on the Invoice form view.

You can view these invoice tasks from the **Receipt Acknowledgment** sub-module under the Sourcing and Purchasing Automation module. The following are the key fields of an invoice task:

<table id="table_icy_vyy_hlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated unique identifier of the invoice task.

</td></tr><tr><td>

Assigned to

</td><td>

Person primarily responsible for this invoice task.

</td></tr><tr><td>

Primary contact

</td><td>

Person within the procurement team who can be contacted with questions about receipts, milestones, invoices, or other activities related to acknowledgment. This field is populated or updated with the same user in the **Assigned to** field of the parent task record, as follows: For an invoice or acknowledgment task, from the referenced purchase order.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the invoice task.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the invoice task.

</td></tr><tr><td>

State

</td><td>

Status of the invoice task. The options are **Open**, **Work in Progress**, **Closed Complete**, **Closed Rejected**, and **Closed Canceled**.If a line is acknowledged in Shopping Hub, the state of the invoice line will be Invoice Confirmed. If rejected, the state of the invoice line will be Rejected.

</td></tr><tr><td>

Due date

</td><td>

Expected due date from the person to whom this task is assigned.

</td></tr><tr><td class="sub-head" colspan="2">

Summary Details

</td></tr><tr><td>

Invoice

</td><td>

Invoice for which this invoice task is created.

</td></tr><tr><td>

Expected start

</td><td>

Expected start date of the invoice task.

</td></tr><tr><td>

Actual start

</td><td>

Actual start date of the invoice task.

</td></tr><tr><td>

Actual end

</td><td>

Actual end date of the invoice task.

</td></tr><tr><td>

Duration

</td><td>

Duration to complete this invoice task.

</td></tr></tbody>
</table>The following are the related lists of an invoice task:

|Related list|Description|
|------------|-----------|
|Invoice lines|List of all the related invoice lines with acknowledgment type as service acknowledgment, for this invoice task.|

**Parent Topic:**[Sourcing and Purchasing Automation](purchase-experience-workflow.md)

