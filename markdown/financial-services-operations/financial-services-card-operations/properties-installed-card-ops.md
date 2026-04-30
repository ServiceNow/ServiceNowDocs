---
title: Properties installed with Financial Services Card Operations
description: Customize the properties that are available with the Financial Services Card Operations application.
locale: en-US
release: zurich
product: Financial Services Card Operations
classification: financial-services-card-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Card Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Properties installed with Financial Services Card Operations

Customize the properties that are available with the Financial Services Card Operations application.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

You can submit your changes by selecting **Save**.

<table id="table_dcc_wt1_gmb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable Mastercard integration

</td><td>

Enables or disables the integration of Mastercard's Mastercom APIs into the Dispute Management workflow.-   **Type**: true \| false
-   **Default value**: True
-   **Location**: **All** &gt; **Card Operations** &gt; **Administration** &gt; **Properties**
-   Learn more: [Managing disputes integrated with Mastercard](../concept/work-on-disputes-integrated-with-mc.md)

</td></tr><tr><td>

Number of hours \(before end date\) to unblock credit card for a temporary block credit card requestsn\_bom\_credit\_card.reserverd\_hours\_to\_unblock\_credit\_card

</td><td>

For an unblock credit card \(for limited time\) request, the system automatically creates a new case to unblock the blocked credit card at the specified number of hours before the end date in the request.-   **Type**: integer
-   **Default value**: 8
-   **Location**: **All** &gt; **Card Operations** &gt; **Administration** &gt; **Properties**
-   Learn more: [Blocking a credit card](../concept/work-block-credit-card-case.md)

</td></tr><tr><td>

Number of hours \(before the end date\) to revert the credit limit for a temporary increase credit limit requestsn\_bom\_credit\_card.reserverd\_hours\_to\_update\_credit\_limit

</td><td>

For a temporary increase credit limit request, the system automatically creates a new case to revert the credit limit of the card at the specified number of hours before the end date in the request.-   **Type**: integer
-   **Default value**: 8
-   **Location**: **All** &gt; **Card Operations** &gt; **Administration** &gt; **Properties**
-   Learn more: [Reset the credit limit for a customer](../task/reset-credit-limit.md)

</td></tr></tbody>
</table>**Parent Topic:**[Financial Services Card Operations reference](../concept/card-operations-reference.md)

