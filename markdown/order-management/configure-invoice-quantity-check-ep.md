---
title: Configure the invoice quantity validation extension point
description: Implement the invoice quantity check extension point to enable the invoice dispute intake assistant AI agent to validate a customer's quantity dispute claim by reconciling it with delivered quantity data from your Enterprise Resource Planning \(ERP\) or inventory system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/order-management/configure-invoice-quantity-check-ep.html
release: zurich
topic_type: task
last_updated: "2026-02-27"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Now Assist for Order Management]
---

# Configure the invoice quantity validation extension point

Implement the invoice quantity check extension point to enable the invoice dispute intake assistant AI agent to validate a customer's quantity dispute claim by reconciling it with delivered quantity data from your Enterprise Resource Planning \(ERP\) or inventory system.

## Before you begin

The application scope must be set to Manage Invoice Operations. You can change the application scope using the application picker \[Omitted image "globe-outline-24.svg"\] Alt text: in the Unified Navigation bar.

Role required: admin

## About this task

The demo data for the Manage Invoice Operations application includes a sample implementation called invoiceQuantityCheckDemo as part of the sn\_inv\_ops\_aias.invoiceQuantityCheckEP extension point. To enable real-world validation of quantity disputes against your external ERP system or inventory delivery records, replace the demo implementation with your own custom logic.

The demo implementation also illustrates a fallback pattern. When sold product information is unavailable on an invoice line, the function validates the disputed quantity against the corresponding sales order line quantity instead. You can mirror this pattern in your custom implementation when applicable.

## Procedure

1.  Log in to the ServiceNow instance.

2.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

3.  Search for the sn\_inv\_ops\_aias.invoiceQuantityCheckEP scripted extension point in the **API Name** field.

4.  View the sample script included in the demo data by selecting **sn\_inv\_ops\_aias.invoiceQuantityCheckEP**.

5.  Create your own implementation of the extension point by selecting the **Create implementation** related link.

6.  On the Script Include form, fill in the fields.

    For a description of the Script Include form fields, see [Script includes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/scripts/c_ScriptIncludes.md).

7.  Override the functions in the script to implement your logic for validating the customer's quantity dispute claim.

    -   **checkInvoiceQuantityWithInvoiceCase**

        Placeholder function meant to be overridden. Use this placeholder to implement the logic to validate quantity disputes across multiple invoice lines associated with an invoice case.

        Input:

        ```
        {
            "invoiceNumber": <Invoice number of the customer invoice record>,
            "verifiedInvoiceLineDetails": <Array of invoice line details>
        ```

        Output:

        ```
        {
        “invoiceLineNumber”: <Invoice line number against which the dispute was raised>,
        “disputedQuantity”: <Disputed quantity claimed by the customer, as available in the invoice case line>
        }
        ```

    -   **checkInvoiceQuantity**

        Placeholder function meant to be overridden. Use this placeholder to implement the logic to validate a quantity dispute by reconciling the customer's claimed quantity against your ERP or inventory delivery records.

        Input:

        ```
        {
            "invoiceNumber": <Invoice number of the customer invoice record>,
            "invoiceLineNumber": <Invoice line number of the customer invoice line record against which the dispute was raised>,
            "userEnteredQty": <Disputed quantity claimed by the customer>
        }
        ```

        Output:

        ```
        {
            "invoiceLineNumber": <Invoice line number against which the dispute was raised>,
            "invoiceQty": <Actual quantity on the invoice line record>,
            "deliveredQty": <Integer representing the disputed quantity claimed
                              by the customer>,
            "qtyMatch": <Boolean; true if the customer's dispute claim is valid, false if the invoiced and claimed quantities match>,
            "isError": <Boolean; true if the API call failed, false if the API call was successful>,
            "errorMessage": <Error message string to handle failure scenarios>
        }
        ```

8.  Select **Update**.

9.  Validate your implementation by submitting an invoice dispute from the Business Portal using the Now Assist Virtual Assistant.

    For more information, see [Dispute invoice issues using Now Assist Virtual Assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/dispute-invoice-issues-now-assist.md).


**Parent Topic:**[Configuring Now Assist for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/now-assist-for-order-management-configuring.md)

**Related topics**  


[Using extension points to extend application functionality](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/web-services/extension-points.md)

[Creating and adding a scripted extension point](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/web-services/impl-scripted-ext-pts-base-code.md)

