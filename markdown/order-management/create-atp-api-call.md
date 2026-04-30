---
title: Configure ATP API for the manage order operations agent
description: Create an Available-to-Promise \(ATP\) API call that enables the manage order operations agent to check product availability and determine the earliest possible delivery date when customers request expedited shipping.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-11-21"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Now Assist for Order Management]
---

# Configure ATP API for the manage order operations agent

Create an Available-to-Promise \(ATP\) API call that enables the manage order operations agent to check product availability and determine the earliest possible delivery date when customers request expedited shipping.

## Before you begin

The application scope must be set to Order Exception AI Agents. You can change the application scope using the application picker ![](../../../reuse/icons/product-icons/globe-outline-24.svg) in the Unified Navigation bar.

Role required: admin

## About this task

The demo data for the manage order operations agent includes a sample implementation called orderExpeditionCheckDemo as part of the sn\_ord\_ops\_aias.orderExpeditionCheckEP extension point. To enable real-world functionality such as checking on-hand quantities and delivery dates from external Enterprise Resource Planning \(ERP\) systems like SAP or Oracle, you should replace the demo data implementation with your custom ATP API.

## Procedure

1.  Log in to the ServiceNow instance.

2.  Navigate to **All** &gt; **Scripted Extension Points** &gt; **Scripted Extension Points**.

3.  In the **API Name** field, search for the `sn_ord_ops_aias.orderExpeditionCheckEP` scripted extension point.

4.  View the sample script included in the demo data by selecting **sn\_ord\_ops\_aias.orderExpeditionCheckEP**.

5.  Create your own implementation of the sn\_ord\_ops\_aias.orderExpeditionCheckEP extension point by selecting the **Create implementation** related link.

6.  On the Script Include orderExpeditionCheckEP form, fill in the fields.

    For a description of the Script Include form fields, see [Script includes](https://www.servicenow.com/docs/access?context=c_ScriptIncludes&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

7.  Edit the getAvailability function in the script to implement your own logic for checking product availability and delivery dates.

<table id="table_nvf_4d5_2hc"><thead><tr><th>

Function name

</th><th>

Description

</th><th>

Input and output

</th></tr></thead><tbody><tr><td>

getAvailability

</td><td>

Placeholder function meant to be overridden. Use this placeholder to implement the logic to:

-   Query external inventory or ERP systems.
-   Determine if the product is available.
-   Calculate the earliest delivery date based on the requested date and stock levels.


</td><td>

Input: The getAvailability function takes the order number of the Customer order record and the revised date requested by the customer as input.

 Output:

```
{
	"isAvailaible": <true/false – denotes if stock is available>, 
	"earliestDelivery": <earliest delivery date in yyyy-MM-dd format>, 
	"isError": <true/false – denotes if there is any failure in the API call>, 
	"errorMessage": <error message string in case of failure> 
}
```

</td></tr></tbody>
</table>8.  Select **Update**.

9.  Validate your implementation by requesting order changes from the Business Portal using the Now Assist Virtual Assistant.

    For more information, see [Request order changes using Now Assist Virtual Assistant](request-order-changes-now-assist.md).


**Parent Topic:**[Configuring Now Assist for Order Management](../concept/now-assist-for-order-management-configuring.md)

**Related topics**  


[Using extension points to extend application functionality](https://www.servicenow.com/docs/access?context=extension-points&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

[Creating and adding a scripted extension point](https://www.servicenow.com/docs/access?context=impl-scripted-ext-pts-base-code&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

