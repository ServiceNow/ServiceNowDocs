---
title: Add statement expense line
description: At the statement item breakdown level, add the number of units consumed, unit rate of the item, and the total cost of all items. Just as an invoice has printed line items, detailing the expense list, the statement item also has the expense details reported as statement expense lines in the showback statement.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/it-business-management/financial-management/add-statement-expense-line.html
release: xanadu
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2026-06-20"
reading_time_minutes: 1
breadcrumb: [View all showback statements, Showback statements, Financial Charging, Financial Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Add statement expense line

At the statement item breakdown level, add the number of units consumed, unit rate of the item, and the total cost of all items. Just as an invoice has printed line items, detailing the expense list, the statement item also has the expense details reported as statement expense lines in the showback statement.

## Before you begin

Role required: service\_charging\_analyst

## Procedure

1.  Click **New** in the Statement Expense Lines related list.

2.  On the form, fill in the form fields.

<table id="table_zp3_tv5_tz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Showback statement

</td><td>

Defaults to the showback statement reporting entity.

</td></tr><tr><td>

Statement item

</td><td>

Select the statement item that is to be listed as the statement expense line from the choice list.

</td></tr><tr><td>

Volume

</td><td>

Number of items consumed \(in units\).

</td></tr><tr><td>

Cost

</td><td>

Calculated as Unit rate \* Volume.

</td></tr><tr><td>

State

</td><td>

Status of the statement expense line.-   **Pending**: Showback statement is not published, the statement expense line is in the Pending state. \(The showback statement is in the Draft state.\)
-   **Processed**: The showback statement is published, statement expense lines are in the Processed state. \(Showback statement is in Published state.\)
-   **Disputed**: If the statement recipient perceives the volume or unit rate of a statement expense line to be incorrect, then the recipient can raise a dispute. \(If the statement expense line is disputed, the showback statement is also in a Disputed state.\)
-   **Accepted**: The showback user accepts the statement expense lines. \(The showback statement is Closed.\)


</td></tr><tr><td>

Statement item breakdown

</td><td>

Select the statement item breakdown that you want to be listed for the statement item.

</td></tr><tr><td>

Unit rate

</td><td>

Rate at which the reporting entity is charged for one unit of the item.

</td></tr></tbody>
</table>3.  Click **Submit**.


## What to do next

[Add expense line details for the statement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-business-management/financial-management/add-statement-expense-line-details.md) expense line of the statement item.

**Parent Topic:**[View all showback statements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-business-management/financial-management/view-all-showback-statements.md)

