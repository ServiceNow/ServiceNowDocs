---
title: View tolerance form
description: Invoice processing cases with exceptions displays the associated Tolerance details at header level and Variance details at line level.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/accounts-payable-operations/view-tolerance-form.html
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Tolerance Rules and Variances for invoices, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# View tolerance form

Invoice processing cases with exceptions displays the associated **Tolerance details** at header level and **Variance details** at line level.

## Before you begin

Role required: sn\_ap\_apm.accounts\_payable\_specialist

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **All Work** &gt; **All open invoice processing cases**.

    List of **All open invoice processing cases** is displayed.

2.  Open an invoice case.

3.  Click **Exceptions**.

4.  Open any invoice exception record with **Status** as **Open** and contains **Tolerance type**.

5.  In the **Details** tab.

    1.  For header level exception- View **Tolerance** and **Variance details**.

    2.  For line level exception- View **Tolerance** details.

        You can view the variance details of each invoice line under **Invoice line affected** tab in list view and form view.

        **Note:** If the variance value and variance percentage is exceeding the limit, the values are highlighted in yellow color with warning \[Omitted image "warning-icon.png"\] Alt text: Warning icon icon suffixed with **Exceeds** and **Within** labels. Grey color indicates that the variance value and variance percentage is within the limits or closed with check\[Omitted image "check-icon.png"\] Alt text: Check icon icon.


## Result

The Tolerance details at the header level and Variance details at the line level are displayed in the invoice processing case with exceptions.

**Parent Topic:**[Tolerance Rules and Variances for invoices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/tolerance-rules-and-variance.md)

