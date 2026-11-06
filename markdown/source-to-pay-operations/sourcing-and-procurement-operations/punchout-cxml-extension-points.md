---
title: Punchout cXML extension points
description: Use the PunchoutRequestBuilder and PunchoutResponseParser scripted extension points to customize the cXML requests that are sent to a punchout supplier and how the cXML responses from that supplier are parsed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/source-to-pay-operations/sourcing-and-procurement-operations/punchout-cxml-extension-points.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-10-15"
reading_time_minutes: 1
breadcrumb: [Configure punchout third-party site purchases, Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Punchout cXML extension points

Use the PunchoutRequestBuilder and PunchoutResponseParser scripted extension points to customize the cXML requests that are sent to a punchout supplier and how the cXML responses from that supplier are parsed.

Each punchout supplier can have its own implementation of an extension point. For a punchout transaction, the system looks for an implementation whose `getSupplierId` method returns the ID of that punchout supplier. If it finds one, it uses the first matching implementation. If it does not find one, it uses the default implementation.

<table id="table_punchout_cxml_ext_points"><thead><tr><th>

Extension point

</th><th>

What it controls

</th><th>

Methods to implement

</th><th>

Default implementation

</th></tr></thead><tbody><tr><td>

`sn_spend_intg.PunchoutRequestBuilder`

</td><td>

How the punchout setup request and the punchout order request are built and sent to the supplier.

</td><td>

-   `getSupplierId`
-   `sendPunchoutSetupRequest(payload, sku)`
-   `sendPunchoutOrderRequest(orderId)`

</td><td>

`DefaultPunchoutRequestBuilder`

</td></tr><tr><td>

`sn_spend_intg.PunchoutResponseParser`

</td><td>

How the cXML responses and messages from the supplier are parsed.

</td><td>

-   `getSupplierId`
-   `parsePunchoutSetupResponse(xmlResponse)`
-   `parsePunchoutOrderMessageResponse(params)`
-   `parsePunchoutOrderConfirmationResponse(xmlResponse)`
-   `parsePunchoutShippingConfirmationResponse(xmlResponse)`

</td><td>

`DefaultPunchoutResponseParser`

</td></tr></tbody>
</table>**Note:** The `initialize` method of your implementation must return the object that implements the methods. The system calls the methods on the object that `initialize` returns.

To create an implementation, create a script include and an extension instance for the extension point, as described in [Create script include for punchout supplier products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/sourcing-and-procurement-operations/configure-ext-point-punchout.md) and [Create extension instance for the scripted extension point](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/sourcing-and-procurement-operations/configure-ext-point-punchout.md). Use the default implementation as a starting point.

For the extension point that controls how product details from a punchout supplier are displayed in Shopping Hub, see [Configure extension point for Product search API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/sourcing-and-procurement-operations/configure-ext-point-punchout.md).

**Parent Topic:**[Configure punchout for third-party site purchases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/sourcing-and-procurement-operations/configure-supplier-punchout.md)

