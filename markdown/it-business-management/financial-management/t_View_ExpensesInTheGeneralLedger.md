---
title: View expenses in the general ledger
description: You can view records in any of the general ledger tables and make changes if necessary.
locale: en-US
release: xanadu
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Financial data import, Financial Modeling, Financial Management, Project Portfolio Management, Strategic Portfolio Management]
---

# View expenses in the general ledger

You can view records in any of the general ledger tables and make changes if necessary.

## Before you begin

Role required: cost\_transparency\_admin, cost\_transparency\_analyst

## Procedure

1.  Navigate to **All** &gt; **Financial Modeling** &gt; **Workbench** and navigate to the review stage of the workbench.

2.  Open the link in the number of **Groomed lines** that are generated in the **Others** section.

3.  On the form, fill in the fields.

    ![The Groomed General Ledger Data form](../image/General_ledger_form.png "Groomed General Ledger Data form")

<table id="table_fk1_1by_wq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Auto-generated identification number for the general ledger data record.

</td></tr><tr><td>

State

</td><td>

The current state of the record:-   **Unallocated**: Allocations for this expense are not allocated.
-   **Allocated**: This expense has been allocated.
-   **Locked**: The general ledger expense is locked so that its allocation lines cannot be reverted.


</td></tr><tr><td>

Account name

</td><td>

Name of the account.

</td></tr><tr><td>

Account number

</td><td>

Account number this expense applies to. This field is mandatory on the Cleansed General Ledger Data form to ensure that all cleansed expenses appear in an account in the Bucketing stage of the workbench.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the expense.

</td></tr><tr><td>

Amount

</td><td>

The amount of the expense.

</td></tr><tr><td>

Cleansed expense

</td><td>

\[General Ledger Staged Data form\]A reference to the corresponding record in the General Ledger Cleansed Data table. The expense in the General Ledger Cleansed Data table that is automatically created when you create an expense in the General Ledger Staged Data table.

</td></tr><tr><td>

Staged expense

</td><td>

\[General Ledger Cleansed Data form\]A reference to the corresponding record in the General Ledger Cleansed Data table.

</td></tr><tr><td>

Groomed expense

</td><td>

\[General Ledger Cleansed Data form\]A reference to the corresponding record in the Groomed General Ledger Data table.

</td></tr><tr><td>

Grooming rule

</td><td>

\[General Ledger Cleansed Data form\]The condition that the workbench uses to filter expenses that are put in buckets.

</td></tr><tr><td>

Currency

</td><td>

Currency that the expense is valued in. The currency is a three letter code defined in the Currency \[fx\_currency\] table. If the value in this field does not match any code in the Currency table, dollar signs are displayed by default for all expenses. Make sure that your expenses in all general ledger forms are in the same currency as your system currency.

</td></tr><tr><td>

Document amount

</td><td>

Amount of the original expense document.

</td></tr><tr><td>

Document currency

</td><td>

Currency that the original expense document uses. As with the **Currency** field, the value in the field is a three letter code defined in the Currency table.

</td></tr><tr><td>

Bucket

</td><td>

\[Groomed General Ledger Data form\]Bucket that this expense is associated with.

</td></tr><tr><td>

Sub-bucket

</td><td>

\[Groomed General Ledger Data form\]Sub-bucket that this expense is associated with.

</td></tr><tr><td>

Cost center

</td><td>

Cost center this expense applies to.

</td></tr><tr><td>

Department

</td><td>

Department associated with this expense.

</td></tr><tr><td>

Fiscal period

</td><td>

\[Groomed General Ledger Data form\]Period during which this expense occurred.

</td></tr><tr><td>

Document date

</td><td>

Date on which the original expense document was issued.

</td></tr><tr><td>

Import set

</td><td>

The import set containing the data that you imported into the instance.

</td></tr><tr><td>

Location

</td><td>

The location of where the expense was incurred.

</td></tr><tr><td>

Vendor

</td><td>

The vendor record that is referenced from the Company \[core\_company\] table.

</td></tr><tr><td>

Posting date

</td><td>

The date of when this expense was incurred.

</td></tr><tr><td>

Local amount

</td><td>

The amount represented in the local currency.

</td></tr><tr><td>

Local currency

</td><td>

The currency associated with the account.

</td></tr><tr><td>

Segments

</td><td>

Expense amounts for the segments that are defined in the hierarchy of segments.

</td></tr></tbody>
</table><table id="table_wjy_bh3_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cost Allocations

</td><td>

\[Groomed General Ledger Data form\]Allocation lines created from this expense.

</td></tr><tr><td>

General Ledger Cleansed Data

</td><td>

\[Groomed General Ledger Data form\]The records in the General Ledger Cleansed Data table that created the groomed expense records after the expenses are put into buckets.

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Financial data import](../concept/c_FinancialManagementImport.md)

