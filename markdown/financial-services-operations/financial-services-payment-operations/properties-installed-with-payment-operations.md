---
title: Properties installed with Financial Services Payment Operations
description: Customize the properties that are available with Financial Services Payment Operations.
locale: en-US
release: yokohama
product: Financial Services Payment Operations
classification: financial-services-payment-operations
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Financial Services Payment Operations reference, Payment Operations, Using banking applications, Financial Services Operations \(FSO\)]
---

# Properties installed with Financial Services Payment Operations

Customize the properties that are available with Financial Services Payment Operations.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

You can access the payment operations properties by navigating to **All** &gt; **Payment Operations** &gt; **Administration** &gt; **Properties**.

<table id="table_dcc_wt1_gmb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number of days to wait until creation of a follow-up claim tasksn\_bom\_payment.claim\_follow \_up\_interval\_in\_days

</td><td>

The system creates a follow-up claim task for a claim if the claim case is not closed within the number of days mentioned in this property. -   **Type**: integer
-   **Default value**: 16
-   **Location**: **All** &gt; **Payment Operations** &gt; **Administration** &gt; **Properties**
-   Learn more: [Work on a claim task for an external refund](../task/work-claim-task.md)

</td></tr><tr><td>

Number of days to wait until creation of a follow up inquiry tasksn\_bom\_payment.inquiry\_task \_folow\_up\_interval\_in\_days

</td><td>

The system creates a follow-up inquiry task for the payment inquiry case if the case is not resolved or closed within the number of days mentioned in this property. -   **Type**: integer
-   **Default value**: 16
-   **Location**: **All** &gt; **Payment Operations** &gt; **Administration** &gt; **Properties**
-   Learn more: [Work on an inquiry task](../task/work-on-inquiry-task.md)

</td></tr></tbody>
</table>**Parent Topic:**[Financial Services Payment Operations reference](../concept/payment-operations-reference.md)

