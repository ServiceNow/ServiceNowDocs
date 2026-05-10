---
title: Configure the invoice dispute resolution extension point
description: Implement the invoice case resolution extension point to enable the invoice dispute intake assistant AI agent to resolve a validated quantity dispute by issuing a credit note or placing an order for the disputed quantity.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Now Assist for Order Management]
---

# Configure the invoice dispute resolution extension point

Implement the invoice case resolution extension point to enable the invoice dispute intake assistant AI agent to resolve a validated quantity dispute by issuing a credit note or placing an order for the disputed quantity.

## Before you begin

The application scope must be set to Manage Invoice Operations. You can change the application scope using the application picker ![](../../../reuse/icons/product-icons/globe-outline-24.svg) in the Unified Navigation bar.

Role required: admin

## About this task

The demo data for the Manage Invoice Operations application includes a sample implementation called `invoiceCaseResolutionEP` as part of the `sn_inv_ops_aias.invoiceCaseResolutionEP` extension point. To enable real-world resolution of validated invoice disputes, such as issuing credit notes or placing orders through your external systems, replace the demo implementation with your own custom logic.

## Procedure

1.  Log in to the ServiceNow instance.

2.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

3.  Search for the `sn_inv_ops_aias.invoiceCaseResolutionEP` scripted extension point in the **API Name** field.

4.  View the sample script included in the demo data by selecting **sn\_inv\_ops\_aias.invoiceCaseResolutionEP**.

5.  Create your own implementation of the extension point by selecting the **Create implementation** related link.

6.  On the Script Include form, fill in the fields.

    For a description of the Script Include form fields, see [Script includes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/c_ScriptIncludes.md).

7.  Override the `processInvoiceDisputeResolution` function to implement your resolution logic for validated invoice quantity disputes.

<table id="table_invoice_resolution_function"><thead><tr><th>

Function name

</th><th>

Description

</th><th>

Input and output

</th></tr></thead><tbody><tr><td>

`processInvoiceDisputeResolution`

</td><td>

Placeholder function meant to be overridden. Use this placeholder to implement the logic to resolve a validated invoice quantity dispute by processing the customer's preferred resolution option, such as issuing a credit note or placing an order for the disputed quantity.

</td><td>

Input:

```
{
    "invoiceCase": <Invoice case number of the invoice case record>,
    "resolutionOption": <String value representing the resolution option selected by the customer>,
    "conversationSummary": <Optional. String containing the summarized transcript of the complete conversation.>
}
```

 Output:

```
{
    "hasResolved": <Boolean; true if the resolution was processed successfully, false if the resolution failed>,
    "creditNote": <String containing the generated credit note number>,
    "orderNumber": <String containing the generated order number>
}
```

</td></tr></tbody>
</table>8.  Select **Update**.

9.  Validate your implementation by submitting an invoice dispute from the Business Portal and selecting a resolution option using the Now Assist Virtual Assistant.

    For more information, see [Dispute invoice issues using Now Assist Virtual Assistant](dispute-invoice-issues-now-assist.md).


**Parent Topic:**[Configuring Now Assist for Order Management](../concept/now-assist-for-order-management-configuring.md)

**Related topics**  


[Using extension points to extend application functionality](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/extension-points.md)

[Creating and adding a scripted extension point](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/impl-scripted-ext-pts-base-code.md)

