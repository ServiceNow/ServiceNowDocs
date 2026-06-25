---
title: Configuring invoice owner prediction settings
description: Configure system properties for the Recommend Invoice Owner AI agent to define how business owners are identified for Non-PO invoices and credit memos.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/configuring-bo-prediction-settings.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [AI agent, Now Assist, APO, Accounts Payable Operations, invoice management, AI automation]
breadcrumb: [Recommend invoice owner AI agent, Using AI agents in Now Assist for Accounts Payable Operations, Now Assist for APO, Accounts Payable Operations, Finance and Supply Chain]
---

# Configuring invoice owner prediction settings

Configure system properties for the Recommend Invoice Owner AI agent to define how business owners are identified for Non-PO invoices and credit memos.

Navigate to **All** &gt; **Accounts Payable Operations** &gt; **Administration** &gt; **Properties** to access the invoice owner prediction settings. These settings influence the number of historical invoices analyzed, the time considered, and the confidence threshold used to make recommendations. The AP admin can modify these settings. For more information on the settings, see [Set APO properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/set-apo-properties.md).

\[Omitted image "apo-invoice-owner-prediction.png"\] Alt text: Use theInvoice owner prediction settings to check the number of historical invoices analyzed, the time considered, and the confidence threshold used to make recommendations. The screenshot shows the default values.

<table id="table_qts_43s_ghc"><thead><tr><th>

Setting

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

Number of recent invoices from the same supplier the system should review to predict the business owner

</td><td>

Defines the number of recent invoices from the same supplier that the AI agent analyzes when identifying a business owner.

</td><td>

5

</td></tr><tr><td>

The time window \(in days\) within which invoices from the supplier are considered

</td><td>

Indicates the time frame for analyzing historical invoices. By default, the AI agent evaluates invoices submitted in the past 90 days.

</td><td>

90 days

</td></tr><tr><td>

The lowest confidence score allowed when suggesting a business owner based on supplier invoices

</td><td>

Specifies the minimum semantic match score required for the AI agent to recommend a business owner. When the match score falls below the default value, the AI agent prompts the AP specialist to create an exception task to review and confirm the business owner.

</td><td>

85

</td></tr><tr><td id="automatic">

Automatically assign the predicted business owner if there’s only one match from the supplier and it meets the minimum score

</td><td>

Determines whether the AI agent automatically assigns the predicted business owner when there's a single, high-confidence match. If this property is set to true, the system updates the business owner automatically.

</td><td>

No

</td></tr></tbody>
</table>**Related topics**  


[Set APO properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/set-apo-properties.md)

