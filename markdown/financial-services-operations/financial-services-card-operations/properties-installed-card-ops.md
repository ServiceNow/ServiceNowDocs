---
title: Properties installed with Financial Services Card Operations
description: Properties that control the behavior of the Financial Services Card Operations application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/financial-services-card-operations/properties-installed-card-ops.html
release: brazil
product: Financial Services Card Operations
classification: financial-services-card-operations
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Reference, Card Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Properties installed with Financial Services Card Operations

Properties that control the behavior of the Financial Services Card Operations application.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

You can submit your changes by selecting **Save**.

<table id="table_dcc_wt1_gmb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable Mastercard integrationsn\_bom\_credit\_card.is\_mastercard\_integration\_enabled

</td><td>

Enables or disables the integration of Mastercard's Mastercom APIs into the Dispute Management workflow.-   **Type**: true \| false
-   **Default value**: False
-   **Location**: **All** &gt; **Card Operations** &gt; **Administration** &gt; **Properties**
-   Learn more: [Managing disputes integrated with Mastercard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/dispute-management/work-on-disputes-integrated-with-mc.md)

</td></tr><tr><td>

Enable Visa integrationsn\_bom\_credit\_card.is\_visa\_integration\_enabled

</td><td>

Enables or disables the integration of Visa's VROL APIs into the Dispute Management workflow.-   **Type**: true \| false
-   **Default value**: False
-   **Location**: **All** &gt; **Card Operations** &gt; **Administration** &gt; **Properties**
-   Learn more: [Managing disputes integrated with Visa](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/dispute-management/work-on-a-dispute-case-integrated-with-visa.md)

</td></tr><tr><td>

Dispute categories enabled for multiple transaction selection\[TBD: property name\]

</td><td>

Specifies the dispute categories for which multiple transactions can be selected in a single dispute case during intake. Applies to the agent workspace and the customer portal.-   **Type**: \[TBD\]
-   **Default value**: \[TBD\]
-   **Location**: **All** &gt; **Card Operations** &gt; **Administration** &gt; **Properties**
-   Learn more: [About dispute intake](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/dispute-management/dispute-intake-overview.md)

</td></tr><tr><td>

Apply common questionnaire answers to disputed transactions\[TBD: property name\]

</td><td>

Enables or disables the automatic application of common questionnaire answers to each transaction in a dispute case that has multiple transactions. When disabled, answers must be provided for each transaction separately.-   **Type**: \[TBD\]
-   **Default value**: \[TBD\]
-   **Location**: **All** &gt; **Card Operations** &gt; **Administration** &gt; **Properties**
-   Learn more: [About dispute intake](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/dispute-management/dispute-intake-overview.md)

</td></tr><tr><td>

Number of hours \(before end date\) to unblock credit card for a temporary block credit card requestsn\_bom\_credit\_card.reserverd\_hours\_to\_unblock\_credit\_card

</td><td>

For an unblock credit card \(for limited time\) request, the system automatically creates a new case to unblock the blocked credit card at the specified number of hours before the end date in the request.-   **Type**: integer
-   **Default value**: 8
-   **Location**: **All** &gt; **Card Operations** &gt; **Administration** &gt; **Properties**
-   Learn more: [Blocking a credit card](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/financial-services-card-operations/work-block-credit-card-case.md)

</td></tr><tr><td>

Number of hours \(before the end date\) to revert the credit limit for a temporary increase credit limit requestsn\_bom\_credit\_card.reserverd\_hours\_to\_update\_credit\_limit

</td><td>

For a temporary increase credit limit request, the system automatically creates a new case to revert the credit limit of the card at the specified number of hours before the end date in the request.-   **Type**: integer
-   **Default value**: 8
-   **Location**: **All** &gt; **Card Operations** &gt; **Administration** &gt; **Properties**
-   Learn more: [Reset the credit limit for a customer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/financial-services-card-operations/reset-credit-limit.md)

</td></tr></tbody>
</table>**Parent Topic:**[Financial Services Card Operations reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/financial-services-card-operations/card-operations-reference.md)

