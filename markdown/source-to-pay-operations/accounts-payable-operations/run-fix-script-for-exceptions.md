---
title: Run fix script for exceptions
description: When you upgrade the instance from previous release to Zurich release, you must manually execute the fix script to re-calculate the amount and quantity of invoices \(which are in-process state\) with Insufficient goods receipt, Insufficient amount line and header variance logic.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/accounts-payable-operations/run-fix-script-for-exceptions.html
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-12-08"
reading_time_minutes: 1
breadcrumb: [Post upgrade tasks for APO, Upgrade Accounts Payable Operations, Components installed with Accounts Payable Invoice Processing, Install Accounts Payable Invoice Processing, Configure, Accounts Payable Operations, Finance and Supply Chain]
---

# Run fix script for exceptions

When you upgrade the instance from previous release to Zurich release, you must manually execute the fix script to re-calculate the amount and quantity of invoices \(which are in-process state\) with Insufficient goods receipt, Insufficient amount line and header variance logic.

## Before you begin

Role required: AP admin

## Procedure

1.  Navigate to **Source-to-Pay Workspace** &gt; **All** &gt; **sysauto\_script.LIST** table.

    The **Scheduled Script Executions** page appears.

2.  Search for script "APM - Recalculate In-Process Invoice Amounts and Quantity".

    The image shows the Fix script.\[Omitted image "fix-script-exception.png"\] Alt text: Fix script for exceptions

3.  Select **Execute Now** to run the fix script.


## Result

The script ensures invoices that are in-process state are re-calculated against amount and quantity as per the logic of Insufficient goods receipt, Insufficient line and header amount variance.

**Related topics**  


[Invoice exceptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/work-with-invoice-exceptions.md)

