---
title: AP Invoice API
description: Allows external systems, such as those used by vendors, to securely submit invoices directly into an accounts payable system in a structured and automated manner.Processes an automated invoice in commerce XML \(cXML\) format.Processes an automated invoice in JSON format.Processes an automated invoice in XML format.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 51
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# AP Invoice API

Allows external systems, such as those used by vendors, to securely submit invoices directly into an accounts payable system in a structured and automated manner.

This API requires the Accounts Payable Invoice Processing \(com.sn\_ap\_apm\) store application, which is provided within the `sn_spend_intg` namespace. For information, see [Accounts Payable Invoice Processing](https://www.servicenow.com/docs/access?context=acc-pay-invoice-processing&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US).

Refer to [AP Invoice API Developer Guide](../../guides/APInvoiceAPI/concept/apInvoice-dev-guide.md#) for help with the following tasks:

-   Define a custom field for invoices, invoice lines, and invoice tax lines.
-   Map the custom field between source and target tables.
-   Map the custom field to a payload entry in a specific format, such as JSON, cXML, or XML.
-   Setting credentials for authentication when using cXML as the payload.

You can apply a filter condition for invoice lines containing multiple ERPs. For information, see [Integration errors](https://www.servicenow.com/docs/access?context=integration-errors-during-erp-posting&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US).

**Note:** The maximum default payload size is 100 records. This value is configurable in the **sn\_spend\_intg.ap.invoice.create.api.record\_limit** system property.

-   **Invoice attachments**

    The XML and JSON endpoints support attachments at the invoice, invoice line, and invoice case levels. The cXML endpoint does not support attachments.

    Use the following guidelines for attachments:

    -   Do not use the reserved "SD\_" prefix for attachment file names.
    -   All attachments must be encoded as Base64 format.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## AP Invoice – POST sn\_spend\_intg/ap\_invoice/cxml

Processes an automated invoice in commerce XML \(cXML\) format.

Use the Invoice integration field mappings \[sn\_spend\_intg\_invoice\_intg\_field\_mapping\] table to determine how the fields are mapped to cXML tags.

For additional cXML resources, refer to the **cXML Reference Guide** at [https://xml.cxml.org](https://xml.cxml.org/current/cXMLReferenceGuide.pdf).

Credentials for this API are included in the payload. You can set up credentials in the Source system credential \[sn\_spend\_intg\_source\_system\_credential\] table. For instructions, see [Setting credentials for authentication in the cXML payload](../../guides/APInvoiceAPI/concept/apInvoice-dev-guide.md#).

You can define custom invoice fields for the request body. Use the following flow to add custom fields, map them to target tables, and format them for availability in the payload:

1.  [Add custom fields for invoice import](../../guides/APInvoiceAPI/concept/apInvoice-dev-guide.md#)
2.  [Map custom fields between source and target tables](../../guides/APInvoiceAPI/concept/apInvoice-dev-guide.md#)
3.  [Map custom fields to a payload source format](../../guides/APInvoiceAPI/concept/apInvoice-dev-guide.md#)

### URL format

Versioned URL: `/api/sn_spend_intg/v1/ap_invoice/cxml`

Default URL: `/api/sn_spend_intg/ap_invoice/cxml`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Path

</th><th>

Description

</th></tr></thead><tbody><tr><td>

/cXML/Header/From /Credential\[@domain='VendorID'\]/Identity

</td><td>

Identifier for the reseller or supplier that the customer can place orders with.Target field: u\_supplier

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest /InvoiceDetailRequestHeader\[@invoiceDate\]

</td><td>

Date on which the customer was invoiced.Target field: u\_invoice\_date

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Format: YYYY-MM-DD

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest /InvoiceDetailRequestHeader\[@invoiceID\]

</td><td>

Invoice number generated from a third-party application.Target field: u\_external\_invoice\_number

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest /InvoiceDetailRequestHeader\[@invoiceOrigin\]

</td><td>

External source system from where the invoice is received. For example, supplier.Target field: u\_inbound\_source

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest /InvoiceDetailRequestHeader/InvoicePartner /Contact\[@role='billTo'\]/PostalAddress/City

</td><td>

The city to which the invoice is sent.Target field: u\_bill\_to\_city

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest /InvoiceDetailRequestHeader/InvoicePartner /Contact\[@role='billTo'\]/PostalAddress/Country

</td><td>

The country to which the invoice is sent in ISO 3166 format. For example, `US`.Target field: u\_bill\_to\_country

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest /InvoiceDetailRequestHeader/InvoicePartner /Contact\[@role='billTo'\]/PostalAddress/State

</td><td>

The state or province to which the invoice is sent.Target field: u\_bill\_to\_state\_or\_province

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest /InvoiceDetailRequestHeader/InvoicePartner /Contact\[@role='billTo'\]/PostalAddress/Street

</td><td>

The street address to which the invoice is sent.Target field: u\_bill\_to\_street

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest /InvoiceDetailRequestHeader/InvoicePartner /Contact\[@role='billTo'\]/PostalAddress/PostalCode

</td><td>

The zip or postal code to which the invoice is sent.Target field: u\_bill\_to\_zip\_or\_postal\_code

</td></tr><tr><td>

Contact\[@role="remitTo"\]/PostalAddress /Street

</td><td>

The street address to which the payment is made.Target field: u\_remit\_address

</td></tr><tr><td>

Contact\[@role="remitTo"\]/PostalAddress /City

</td><td>

The city to which the payment is made.Target field: u\_remit\_to\_city

</td></tr><tr><td>

Contact\[@role="remitTo"\]/PostalAddress /State

</td><td>

The state or province to which the payment is made.Target field: u\_remit\_to\_state\_or\_province

</td></tr><tr><td>

Contact\[@role="remitTo"\]/PostalAddress /PostalCode

</td><td>

The zip or postal code to which the payment is made.Target field: u\_remit\_to\_zip\_or\_postal\_code

</td></tr><tr><td>

Contact\[@role="remitTo"\]/PostalAddress /Country

</td><td>

The country to which the payment is made in ISO 3166 format. For example, `US`.Target field: u\_remit\_to\_country

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest/InvoiceDetailRequestHeader /InvoiceDetailShipping/Contact\[@role="shipFrom"\]/PostalAddress /Street

</td><td>

Street from which the items on the purchase order are shipped.Target field: u\_ship\_from\_street

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest/InvoiceDetailRequestHeader /InvoiceDetailShipping/Contact\[@role="shipFrom"\]/PostalAddress /City

</td><td>

City from which the items on the purchase order are shipped.Target field: u\_ship\_from\_city

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest/InvoiceDetailRequestHeader /InvoiceDetailShipping/Contact\[@role="shipFrom"\]/PostalAddress /State

</td><td>

State from which the items on the purchase order are shipped.Target field: u\_ship\_from\_state\_or\_province

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest/InvoiceDetailRequestHeader /InvoiceDetailShipping/Contact\[@role="shipFrom"\]/PostalAddress /PostalCode

</td><td>

Zip code from which the items on the purchase order are shipped.Target field: u\_ship\_from\_zip\_or\_postal\_code

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest/InvoiceDetailRequestHeader /InvoiceDetailShipping/Contact\[@role="shipFrom"\]/PostalAddress /Country

</td><td>

Country from which the items on the purchase order are shipped.Target field: u\_ship\_from\_country

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest/InvoiceDetailRequestHeader /InvoicePartner/Contact\[@role="billTo"\] \[@addressID\]

</td><td>

Name of the legal entity of the supplier. Located in the Legal Entity \[sn\_fin\_legal\_entity\] table.Target field: u\_legal\_entity

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

Contact\[@role="shipTo"\]/Name

</td><td>

Name of the contact to which the items on the purchase order should be shipped.Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

Contact\[@role="shipTo"\]/PostalAddress /Street

</td><td>

Street to which the items on the purchase order are shipped.Target field: u\_ship\_to\_street

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

Contact\[@role="shipTo"\]/PostalAddress /City

</td><td>

City to which the items on the purchase order are shipped.Target field: u\_ship\_to\_city

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

Contact\[@role="shipTo"\]/PostalAddress /State

</td><td>

State or province to which the items on the purchase order are shipped.Target field: u\_ship\_to\_state\_or\_province

</td></tr><tr><td>

Contact\[@role="shipTo"\]/PostalAddress /PostalCode

</td><td>

Zip code to which the items on the purchase order are shipped.Target field: u\_ship\_to\_zip\_or\_postal\_code

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

Contact\[@role="shipTo"\]/PostalAddress /Country

</td><td>

Country to which the items on the purchase order are shipped.Target field: u\_ship\_from\_country

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest /InvoiceDetailRequestHeader/PaymentTerm

</td><td>

The agreed upon time and conditions under which a payment to a supplier is made. For example, `Net 30`.Target field: u\_payment\_terms

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest/InvoiceDetailOrder /InvoiceDetailItem\[@description\]/

</td><td>

Description of the invoice line.Target field: u\_line\_description

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest/InvoiceDetailOrder /InvoiceDetailItem\[@quantity\]/

</td><td>

Quantity of goods or services that a customer is being invoiced for.Target field: u\_line\_quantity

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest/InvoiceDetailOrder /InvoiceDetailItem/Distribution/Accounting /AccountingSegment\[1\]/Name

</td><td>

Account number of the cost center for which the invoice is generated. Listed in the Cost Center \[cmn\_cost\_center\] table.Target field: u\_cost\_center

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest/InvoiceDetailOrder /InvoiceDetailItem/Distribution/Accounting /AccountingSegment\[2\]/Name

</td><td>

Account number of the general ledger \(GL\) used to generate the invoice.Target field: u\_gl\_account

See also:

-   [ERP source](https://www.servicenow.com/docs/access?context=erp-source&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)
-   [Ledger account](https://www.servicenow.com/docs/access?context=ledger-account&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest/InvoiceDetailOrder /InvoiceDetailItem/SubtotalAmount/Money

</td><td>

Total amount of money to be paid to the supplier excluding tax and shipping charges.Target field: u\_subtotal

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest/InvoiceDetailOrder /InvoiceDetailItem/NetAmount/Money

</td><td>

Total cost, excluding taxes and shipping, that a customer is being invoiced for a given purchase order line.Target field: u\_line\_amount\_invoiced

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest/InvoiceDetailOrder /InvoiceDetailOrderInfo/OrderReference

</td><td>

Purchase order number that is provided by the customer for this order. Listed in the Purchase Order \[sn\_shop\_purchase\_order\] table.Target field: u\_purchase\_order

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest/InvoiceDetailOrder /InvoiceDetailItem/UnitPrice/UnitOfMeasure

</td><td>

Base unit of measure \(UOM\) used to count the item in the invoice.Target field: u\_uom

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest/InvoiceDetailOrder /InvoiceDetailItem/UnitPrice/Money

</td><td>

Unit price of the line item in the invoice.Target field: u\_line\_unit\_price

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest/InvoiceDetailOrder /InvoiceDetailItem/UnitPrice/Money\[@currency\]

</td><td>

Currency for the line item. For example, `USD`.Target field: u\_currency

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

cXML/Request/InvoiceDetailRequest/InvoiceDetailOrder /InvoiceDetailItem /InvoiceDetailItemReference\[@lineNumber\]

</td><td>

Purchase order line ID for the referenced supplier. Listed in the Purchase Order Line \[sn\_shop\_purchase\_order\_line\] table.Target field: u\_purchase\_order\_line

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

cXML/Request/InvoiceDetailRequest/InvoiceDetailOrder /InvoiceDetailItem/InvoiceDetailItemReference /ItemID/SupplierPartID

</td><td>

Part number that is generated by a supplier for this invoice line.Target field: u\_supplier\_part\_number

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

cXML/Request/InvoiceDetailRequest/InvoiceDetailOrder /InvoiceDetailItem/InvoiceDetailItemReference /Description

</td><td>

Description of the purchase order line for the invoice.Target field: u\_po\_line\_description

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

cXML/Request/InvoiceDetailRequest/InvoiceDetailOrder /InvoiceDetailItem/Tax/Money

</td><td>

Total amount of taxes that are billed for the purchase.Target field: u\_tax\_amount

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

cXML/Request/InvoiceDetailRequest/InvoiceDetailOrder /InvoiceDetailItem/Tax/Description

</td><td>

Unique tax code generated from the ERP source.Target field: u\_tax\_code

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest/ InvoiceDetailSummary /SubtotalAmount/Money

</td><td>

Total amount of money to be paid to the supplier excluding tax and shipping charges.Target field: u\_subtotal

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest/InvoiceDetailSummary /Tax/Money

</td><td>

Total amount of taxes that are billed for the purchase.Target field: u\_tax\_amount

Related table: Invoice Tax Line Import \[sn\_spend\_intg\_imp\_invoice\_tax\_line\]

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest/InvoiceDetailSummary /Tax/TaxDetail\[@category\]

</td><td>

Type of tax applicable on the invoice. Listed in the Tax Type \[sn\_fin\_tax\_type\] table.Target field: u\_tax\_type

Related table: Invoice Tax Line Import \[sn\_spend\_intg\_imp\_invoice\_tax\_line\]

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest/InvoiceDetailSummary /Tax/TaxDetail\[@percentageRate\]

</td><td>

The tax rate charged by the supplier.Related table: Invoice Tax Line Import \[sn\_spend\_intg\_imp\_invoice\_tax\_line\]

Target field: u\_supplier\_tax\_rate

Related table: Invoice Tax Line Import \[sn\_spend\_intg\_imp\_invoice\_tax\_line\]

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest/InvoiceDetailSummary /SpecialHandlingAmount/Money

</td><td>

Other additional charges associated with the invoice. This is an editable field.Target field: u\_other\_charges

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest/InvoiceDetailSummary /ShippingAmount/Money

</td><td>

Total shipping cost for the entire purchase.Target field: u\_shipping\_amount

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest/InvoiceDetailSummary /GrossAmount/Money

</td><td>

Required. Currency for subtotal, tax, and shipping. The subtotal, tax, and shipping should be in the same currency.Target field: u\_currency

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest/InvoiceDetailSummary /InvoiceDetailDiscount/Money

</td><td>

Discounts that are applied toward the invoice.Target field: u\_discounts

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/cXML/Request/InvoiceDetailRequest/InvoiceDetailSummary /NetAmount/Money

</td><td>

Total amount of money to be paid to the supplier including tax and shipping charges.Target field: u\_amount\_invoiced

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content-Type

</td><td>

Data format of the request body. Only supports **application/xml**.

</td></tr><tr><td>

Source-System

</td><td>

Specifies the source system from which the request is coming from.Available systems are listed in the Source systems credentials \[sn\_spend\_intg\_source\_system\_credential\] table.

This setting helps to determine if the request provided follows the structure in the Invoice integration field mapping \[sn\_spend\_intg\_invoice\_intg\_field\_mapping\] table.

This setting is also used to fetch credentials from the Source system credentials \[sn\_spend\_intg\_source\_system\_credential\] table.

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|202|Request Accepted. The request is successful and invoice processing is in progress.|
|400|Bad Request. A bad request type or malformed request was detected.|
|429|Too Many Requests. The request rate has exceeded the maximum of 10 requests per hour.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

batch\_id

</td><td>

Unique identifier for the batch request. This ID can be used to track the status of the request. This record is stored in the Invoice integration log \[sn\_spend\_intg\_invoice\_integration\_log\] table.Data type: String

</td></tr><tr><td>

error

</td><td>

Contains error message and details when the request fails.```
{
  "detail": String,
  "message": String
}
```

Data type: Object

</td></tr><tr><td>

error.detail

</td><td>

Additional details about the request error.Possible results:

-   Failed API level ACL Validation - User does not have read/write access to the resource.
-   Rate limit of 13 requests per hour for AP Invoice exceeded – The number of records in the batch is more than the batch size set.
-   Required to provide Auth information - Either the password is wrong or user name is wrong.

Data type: String

</td></tr><tr><td>

error.message

</td><td>

Error message containing the reason the request failedPossible errors:

-   Invalid payload - Invalid content type.
-   Invalid payload - Error: Invalid payload structure.
-   Invalid payload - Error: Payload exceeds allowed invoices limit in a batch. The number of records in the batch is more than the batch size set. The maximum default payload size is 100 records. This value is configurable in the **sn\_spend\_intg.ap.invoice.create.api.record\_limit** system property.
-   Invalid payload - Error: Empty invoices. No data to process. The number of records in the batch is zero.
-   Rate limit of 500 requests per hour for APO Invoice Ingestion exceeded.
-   User Not Authenticated. Either the password is wrong or user name is wrong.
-   Failed API level ACL Validation - User does not have read/write access to the resource.

Data type: String

</td></tr><tr><td>

message

</td><td>

Success message, for example, `Your request has been successfully received and is being processed`.You can view the status of the request in the Invoice integration log \[sn\_spend\_intg\_invoice\_integration\_log\] table.

Data type: String

</td></tr><tr><td>

status

</td><td>

Indicates the result of the request.Possible values:

-   Success
-   Fail

Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to process an invoice provided as a request in cXML format.

```
curl -X POST https://instance.servicenow.com/api/sn_spend_intg/v1/ap_invoice/cxml \
-H "Source-System: Ariba" \
-H "Content-Type: application/json" \
-d '{
    "content": "------=_Part_1367_1859161670.1709186492411\r\nContent-Type: text/xml; charset=UTF-8\r\n
Content-ID: 1709186492411.10815535@produs-c4-an-s2-z3-1.us2.gcpint.ariba.com\r\n<?xml version=\"1.0\" 
encoding=\"UTF-8\"?>\r\n<!DOCTYPE cXML SYSTEM \"https://protect-us.mimecast.com/s/fgKrCERVqQU35PNzBuw39pz?domain=xml.cxml.org\">
\r\n<cXML timestamp=\"2024-02-28T22:01:32-08:00\" payloadID=\"1709186492411-3401013259654180284@10.209.37.74\">
\r\n    <Response>\r\n        <Status code=\"200\" text=\"OK\" />\r\n        <DataResponse>\r\n            <Attachment>
\r\n                <URL>186492411.10815535@produs-c4-an-s2-z3-1.us2.gcpint.ariba.com.110</URL>\r\n            </Attachment>
\r\n            <Attachment>\r\n                <URL>1709186492403.306612238@produs-c4-an-s2-z3-1.us2.gcpint.ariba.com.108</URL>
\r\n            </Attachment>\r\n        </DataResponse>\r\n    </Response>\r\n</cXML>\r\n------=_Part_1367_1859161670.1709186492411
\r\nContent-Type: text/xml; charset=UTF-8\r\nContent-ID: 1709186492403.306612238@produs-c4-an-s2-z3-1.us2.gcpint.ariba.com.108
\r\n<?xml version=\"1.0\" encoding=\"UTF-8\"?>\r\n
<!DOCTYPE cXML SYSTEM \"https://protect-us.mimecast.com/s/7QpfCG6VRKf15gQPwFpUTKe?domain=xml.cxml.org\">\r\n
<cXML payloadID=\"1705930173863-1790846563502652473@10.209.37.98\" timestamp=\"2024-01-22T05:29:33-08:00\" version=\"1.2.060\">\r\n
    <Header>\r\n        <From>\r\n            <Credential domain=\"NetworkID\">\r\n                <Identity>AN01532216648-T</Identity>\r\n
            </Credential>\r\n            <Credential domain=\"VendorID\">\r\n                <Identity>3245545</Identity>\r\n
            </Credential>\r\n            <Credential domain=\"PrivateID\">\r\n                <Identity>0000099123</Identity>\r\n
            </Credential>\r\n        </From>\r\n        <To>\r\n            <Credential domain=\"NetworkID\">\r\n
                <Identity>AN01404744424-T</Identity>\r\n            </Credential>\r\n            <Credential domain=\"SystemID\">\r\n
                <Identity>ERP1</Identity>\r\n            </Credential>\r\n            <Credential domain=\"EndPointID\">\r\n
                <Identity>CIG</Identity>\r\n            </Credential>\r\n        </To>\r\n        <Sender>\r\n
            <Credential domain=\"NetworkID\">\r\n                <Identity>AN01000000001</Identity>\r\n
                <SharedSecret>Ariba@123</SharedSecret>\r\n            </Credential>\r\n            <UserAgent>Supplier</UserAgent>\r\n
        </Sender>\r\n    </Header>\r\n    <Request deploymentMode=\"test\">\r\n        <InvoiceDetailRequest>\r\n
            <InvoiceDetailRequestHeader invoiceDate=\"2024-01-22\" invoiceID=\"\" invoiceOrigin=\"supplier\" operation=\"new\ purpose=\"PO Invoice\">\r\n
                <InvoiceDetailHeaderIndicator></InvoiceDetailHeaderIndicator>\r\n
                <InvoiceDetailLineIndicator></InvoiceDetailLineIndicator>\r\n                <InvoicePartner>\r\n
                    <Contact addressID=\"Test123\" role=\"remitTo\">\r\n
                        <Name xml:lang=\"en-US\">Oil and Natural Gas Corporation Limited</Name>\r\n
                        <PostalAddress>\r\n                            <Street>Xyz street</Street>\r\n                            <City>USA</City>\r\n
                            <State isoStateCode=\"US-NY\">NY</State>\r\n                            <PostalCode>10001</PostalCode>\r\n
                            <Country isoCountryCode=\"US\">United States</Country>\r\n                        </PostalAddress>\r\n
                    </Contact>\r\n                </InvoicePartner>\r\n                <InvoicePartner>\r\n
                    <Contact addressID=\"9009\" role=\"billTo\">\r\n                        <Name xml:lang=\"EN\">Bristlecone Inc</Name>\r\n
                        <PostalAddress>\r\n                            <Street>10 Boulvard-10</Street>\r\n
                            <City>San Jose</City>\r\n                            <State>CA</State>\r\n
                            <PostalCode>94077</PostalCode>\r\n                            <Country isoCountryCode=\"US\"></Country>\r\n
                        </PostalAddress>\r\n                        <Phone>\r\n                            <TelephoneNumber>\r\n
                                <CountryCode isoCountryCode=\"US\">1</CountryCode>\r\n                                <Number>7687687799</Number>\r\n
                            </TelephoneNumber>\r\n                        </Phone>\r\n                        <Fax>\r\n
                            <TelephoneNumber>\r\n                                <CountryCode isoCountryCode=\"US\">1</CountryCode>\r\n
                                <Number>768-FAX-NUMBER</Number>\r\n                            </TelephoneNumber>\r\n                        </Fax>\r\n
                    </Contact>\r\n                </InvoicePartner>\r\n                <InvoicePartner>\r\n                    <Contact role=\"from\">\r\n
                        <Name xml:lang=\"en-US\">Oil and Natural Gas Corporation Limited</Name>\r\n                        <PostalAddress>\r\n
                            <Street>123 , street no 5</Street>\r\n                            <City>Dallas</City>\r\n
                            <State isoStateCode=\"US-AL\">AL</State>\r\n                            <PostalCode>36615</PostalCode>\r\n
                            <Country isoCountryCode=\"US\">United States</Country>\r\n                        </PostalAddress>\r\n
                    </Contact>\r\n                </InvoicePartner>\r\n                <InvoiceDetailShipping>\r\n
                    <Contact role=\"shipFrom\">\r\n                        <Name xml:lang=\"en-US\">Oil and Natural Gas Corporation Limited</Name>\r\n
                        <PostalAddress>\r\n                            <Street>Deendayal Urja Bhawan</Street>\r\n
                            <City>New Delhi</City>\r\n                            <State isoStateCode=\"IN-MH\">Maharashtra</State>\r\n
                            <PostalCode>110070</PostalCode>\r\n                            <Country isoCountryCode=\"IN\">India</Country>\r\n
                        </PostalAddress>\r\n                    </Contact>\r\n                    <Contact addressID=\"9999\" role=\"shipTo\">\r\n
                        <Name xml:lang=\"EN\">Buyer Plant Bristlecone</Name>\r\n                        <PostalAddress name=\"default\">\r\n
                            <Street>18 Hanoi Road</Street>\r\n                            <City>San Jose</City>\r\n
                            <State>CA</State>\r\n                            <PostalCode>77077</PostalCode>\r\n
                            <Country isoCountryCode=\"US\"></Country>\r\n                        </PostalAddress>\r\n
                        <Email name=\"default\" preferredLang=\"en\">test@test.com</Email>\r\n                    </Contact>\r\n
                </InvoiceDetailShipping>\r\n            </InvoiceDetailRequestHeader>\r\n            <InvoiceDetailOrder>\r\n
                <InvoiceDetailOrderInfo>\r\n                    <OrderReference orderID=\"\">\r\n
                        <DocumentReference payloadID=\"0AAF8EA1FA5F1EDE9FDC97460BCB03E1\"></DocumentReference>\r\n
                    </OrderReference>\r\n                </InvoiceDetailOrderInfo>\r\n
                <InvoiceDetailItem invoiceLineNumber=\"2\" quantity=\"25\" description=\"Indian Oil\">\r\n
                    <UnitOfMeasure>EA</UnitOfMeasure>\r\n                    <UnitPrice>\r\n                        <Money currency=\"USD\">50</Money>\r\n
                    </UnitPrice>\r\n                    <SubtotalAmount>\r\n                        <Money currency=\"USD\">1250.00</Money>\r\n
                    </SubtotalAmount>\r\n                </InvoiceDetailItem>\r\n            </InvoiceDetailOrder>\r\n        </InvoiceDetailRequest>\r\n
    </Request>\r\n</cXML>\r\n------=_Part_1367_1859161670.1709186492411--"
}'

```

The following result shows that the request is successful and the invoice data is processing. You can view the status of the request in the Invoice integration log \[sn\_spend\_intg\_invoice\_integration\_log\] table. Use the batch ID listed in the Batch ID column to find the invoice.

```
{
    "batchId": "APIINV1729711710733280",
    "status": "Success",
    "message": "Your request has been successfully received and is being processed."
}
```

## AP Invoice – POST sn\_spend\_intg/ap\_invoice/json

Processes an automated invoice in JSON format.

Role required: sn\_spend\_intg.procurement\_integrator

Use the Invoice integration field mappings \[sn\_spend\_intg\_invoice\_intg\_field\_mapping\] table to determine how the fields are mapped to JSON properties.

You can define custom invoice fields for the request body. Use the following flow to add custom fields, map them to target tables, and format them for availability in the payload:

1.  [Add custom fields for invoice import](../../guides/APInvoiceAPI/concept/apInvoice-dev-guide.md#)
2.  [Map custom fields between source and target tables](../../guides/APInvoiceAPI/concept/apInvoice-dev-guide.md#)
3.  [Map custom fields to a payload source format](../../guides/APInvoiceAPI/concept/apInvoice-dev-guide.md#)

### URL format

Versioned URL: `/api/sn_spend_intg/v1/ap_invoice/json`

Default URL: `/api/sn_spend_intg/ap_invoice/json`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

invoices

</td><td>

List containing each invoice to be processed.Data type: Object of nested invoice objects.

```
"invoices": {
  {
    "amount_invoiced": "String",
    "bill_to_city": "String",
    "bill_to_country": "String",
    "bill_to_state_or_province": "String",
    "bill_to_street": "String",
    "bill_to_zip_or_postal_code": "String",
    "business_owner": "String",
    "currency": "String",
    "discounts": "String",
    "erp_number": "String",
    "external_invoice_number": "String",
    "invoice_copy_attachment": [Array],
    "invoice_date": "String",
    "invoice_line_count": "String",
    "invoice_lines": [Array],
    "invoice_type": "String",
    "legal_entity": "String",
    "original_invoice": "String",
    "other_charges": "String",
    "payment_terms": "String",
    "purchase_order": "String",
    "remit_address": "String",
    "remit_to_city": "String",
    "remit_to_country": "String",
    "remit_to_state_or_province": "String",
    "remit_to_zip_or_postal_code": "String",
    "ship_from_city": "String",
    "ship_from_country": "String",
    "ship_from_state_or_province": "String",
    "ship_from_street": "String",
    "ship_from_zip_or_postal_code": "String",
    "ship_to_city": "String",
    "ship_to_country": "String",
    "ship_to_state_or_province": "String",
    "ship_to_street": "String",
    "ship_to_zip_or_postal_code": "String",
    "shipping_amount": "String",
    "subtotal": "String",
    "supplier": "String",
    "supplier_invoice_number": "String",
    "supplier_tax_id": "String",
    "supporting_attachments": [Array]
  }
}
```

</td></tr><tr><td>

invoices.amount\_invoiced

</td><td>

Total amount of money to be paid to the supplier including tax and shipping charges.Target field: u\_amount\_invoiced

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 40

</td></tr><tr><td>

bill\_to\_city

</td><td>

The city to which the invoice is sent.Target field: u\_bill\_to\_city

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

bill\_to\_country

</td><td>

The country to which the invoice is sent in ISO 3166 format. For example, `US`.Target field: u\_bill\_to\_country

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

bill\_to\_state\_or\_province

</td><td>

The state or province to which the invoice is sent.Target field: u\_bill\_to\_state\_or\_province

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

bill\_to\_street

</td><td>

The street address to which the invoice is sent.Target field: u\_bill\_to\_street

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

bill\_to\_zip\_or\_postal\_code

</td><td>

The zip or postal code to which the invoice is sent.Target field: u\_bill\_to\_zip\_or\_postal\_code

</td></tr><tr><td>

invoices.business\_owner

</td><td>

Name of the owner who owns the application from the business side.Target field: u\_business\_owner

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 40

</td></tr><tr><td>

invoices.currency

</td><td>

Required. Currency for subtotal, tax, and shipping. The subtotal, tax, and shipping should be in the same currency.Target field: u\_currency

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 40

</td></tr><tr><td>

invoices.discounts

</td><td>

Discounts that are applied toward the invoice.Target field: u\_discounts

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices.erp\_number

</td><td>

Unique number generated within the ERP \(Enterprise Resource Planning\) system for the purchase order. For information, see [Purchase order integration](https://www.servicenow.com/docs/access?context=purchase-order-integration-2&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US).Target field: u\_erp\_number

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 40

</td></tr><tr><td>

invoices. external\_invoice\_number

</td><td>

Required. Invoice number generated from a third-party application.Target field: u\_external\_invoice\_number

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 40

</td></tr><tr><td>

invoices. invoice\_copy\_attachment

</td><td>

List of attachments defined at the invoice level. See [Accounts Payable Invoice Processing](https://www.servicenow.com/docs/access?context=acc-pay-invoice-processing&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US).Once created, the system will generate the invoice record along with the associated invoice case and invoice lines. Attachments will be linked to their respective records accordingly.

Data type: Array of Objects

```
"invoice_copy_attachment": [
  {
    "content": "String",
    "encoding": "String",
    "mime_code": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

invoices.invoice\_copy\_attachment. content

</td><td>

Base64-encoded file content of the attachment.Data type: String

</td></tr><tr><td>

invoices.invoice\_copy\_attachment. encoding

</td><td>

This value is always `base64`.Data type: String

</td></tr><tr><td>

invoices.invoice\_copy\_attachment. mime\_code

</td><td>

This value is always `base64`.Data type: String

</td></tr><tr><td>

invoices.invoice\_copy\_attachment. name

</td><td>

File name of the attachment.**Note:** Do not use the reserved "SD\_" prefix for an attachment file name.

Data type: String

</td></tr><tr><td>

invoices.invoice\_date

</td><td>

Required. Date on which the customer was invoiced.Target field: u\_invoice\_date

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 40

Format: YYYY-MM-DD

</td></tr><tr><td>

invoices.invoice\_line\_count

</td><td>

Number of lines in the invoice.Target field: u\_invoice\_line\_count

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 40

</td></tr><tr><td>

invoices.invoice\_lines

</td><td>

List of objects that define the lines that are being invoiced for purchases within this order. Invoice lines are staged in the Invoice line import inbound \[sn\_spend\_intg\_imp\_invoice\_line\] table.Data type: Array of Objects

```
"invoice_lines": [
  {
    "attachments": [Array],
    "cost_center": "String",
    "currency": "String",
    "external_invoice_number": "String",
    "gl_account": "String",
    "line_amount_invoiced": "String",
    "line_description": "String",
    "line_quantity": "String",
    "line_unit_price": "String",
    "po_line_description": "String",
    "purchase_order_line": "String",
    "ship_to_city": "String",
    "ship_to_country": "String",
    "ship_to_state_or_province": "String",
    "ship_to_street": "String",
    "ship_to_zip_or_postal_code": "String",
    "subtotal": "String",
    "supplier_part_number": "String",
    "tax_code": "String",
    "tax_details": [Array],
    "uom": "String"
  }
]
```

</td></tr><tr><td>

invoices.invoice\_lines. attachments

</td><td>

List of attachments defined at the invoice line level. See [Create New Invoice Line form](https://www.servicenow.com/docs/access?context=create-invoice-line-form&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US).Once created, the system will generate the invoice record along with the associated invoice case and invoice lines. Attachments will be linked to their respective records accordingly.

Data type: Array of Objects

```
"attachments": [
  {
    "content": "String",
    "encoding": "String",
    "mime_code": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

invoices.invoice\_lines. attachments.content

</td><td>

Base64-encoded file content of the attachment.Data type: String

</td></tr><tr><td>

invoices.invoice\_lines. attachments.encoding

</td><td>

This value is always `base64`.Data type: String

</td></tr><tr><td>

invoices.invoice\_lines. attachments.mime\_code

</td><td>

This value is always `base64`.Data type: String

</td></tr><tr><td>

invoices.invoice\_lines. attachments.name

</td><td>

File name of the attachment.**Note:** Do not use the reserved "SD\_" prefix for an attachment file name.

Data type: String

</td></tr><tr><td>

invoices.invoice\_lines. cost\_center

</td><td>

Account number of the cost center for which the invoice is generated. Listed in the Cost Center \[cmn\_cost\_center\] table.Target field: u\_cost\_center

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

Data type: String

Maximum length: 40

</td></tr><tr><td>

invoices.invoice\_lines. currency

</td><td>

Currency for the line item. For example, `USD`.Target field: u\_currency

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

Data type: String

Maximum length: 40

</td></tr><tr><td>

invoices.invoice\_lines. external\_invoice\_number

</td><td>

Required. Invoice number generated from a third-party application.Target field: u\_external\_invoice\_number

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 40

</td></tr><tr><td>

invoices.invoice\_lines. gl\_account

</td><td>

Account number of the general ledger \(GL\) used to generate the invoice.Target field: u\_gl\_account

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

Data type: String

Maximum length: 40

See also:

-   [ERP source](https://www.servicenow.com/docs/access?context=erp-source&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)
-   [Ledger account](https://www.servicenow.com/docs/access?context=ledger-account&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)

</td></tr><tr><td>

invoices.invoice\_lines. line\_amount\_invoiced

</td><td>

Required. Total cost, excluding taxes and shipping, that a customer is being invoiced for a given purchase order line.Target field: u\_line\_amount\_invoiced

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

Data type: String

Maximum length: 40

</td></tr><tr><td>

invoices.invoice\_lines. line\_description

</td><td>

Required. Description of the invoice line.Target field: u\_line\_description

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

Data type: String

Maximum length: 40

</td></tr><tr><td>

invoices.invoice\_lines. line\_quantity

</td><td>

Required. Quantity of goods or services that a customer is being invoiced for.Target field: u\_line\_quantity

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

Data type: String

Maximum length: 40

</td></tr><tr><td>

invoices.invoice\_lines. line\_unit\_price

</td><td>

Unit price of the line item in the invoice.Target field: u\_line\_unit\_price

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

Data type: String

Maximum length: 40

</td></tr><tr><td>

invoices.invoice\_lines. po\_line\_description

</td><td>

Description of the purchase order line for the invoice.Target field: u\_po\_line\_description

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices.invoice\_lines. purchase\_order\_line

</td><td>

Required. Purchase order line ID for the referenced supplier. Listed in the Purchase Order Line \[sn\_shop\_purchase\_order\_line\] table.Target field: u\_purchase\_order\_line

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

Data type: String

Maximum length: 40

</td></tr><tr><td>

invoices.invoice\_lines. ship\_to\_city

</td><td>

City to which the items on the purchase order are shipped.Target field: u\_ship\_to\_city

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices.invoice\_lines. ship\_to\_country

</td><td>

Country to which the items on the purchase order are shipped.Target field: u\_ship\_to\_country

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices.invoice\_lines. ship\_to\_state\_or\_province

</td><td>

State or province to which the items on the purchase order are shipped.Target field: u\_ship\_to\_state\_or\_province

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices.invoice\_lines. ship\_to\_street

</td><td>

Street to which the items on the purchase order are shipped.Target field: u\_ship\_to\_street

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices.invoice\_lines. ship\_to\_zip\_or\_postal\_code

</td><td>

Zip code to which the items on the purchase order are shipped.Target field: u\_ship\_to\_zip\_or\_postal\_code

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices.invoice\_lines. subtotal

</td><td>

Required. Total amount of money to be paid to the supplier excluding tax and shipping charges.Target field: u\_subtotal

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices.invoice\_lines. supplier\_part\_number

</td><td>

Required. Part number that is generated by a supplier for this invoice line.Target field: u\_supplier\_part\_number

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices.invoice\_lines. tax\_code

</td><td>

Unique tax code generated from the ERP source.Target field: u\_tax\_code

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices.invoice\_lines. tax\_details

</td><td>

List of tax lines for purchases associated with the invoice line.Data type: Array of Objects

```
"tax_details": [
  {
    "tax_amount": "String",
    "tax_rate": "String",
    "tax_type": "String"
  }
]
```

</td></tr><tr><td>

invoices.invoice\_lines. tax\_details.tax\_amount

</td><td>

Required. Total amount of taxes that are billed for the purchase.Target field: u\_tax\_amount

Related table: Invoice Tax Line Import \[sn\_spend\_intg\_imp\_invoice\_tax\_line\]

Data type: String

Maximum length: 40

</td></tr><tr><td>

invoices.invoice\_lines. tax\_details.tax\_rate

</td><td>

The tax rate charged by the supplier.Target field: u\_supplier\_tax\_rate

Related table: Invoice Tax Line Import \[sn\_spend\_intg\_imp\_invoice\_tax\_line\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices.invoice\_lines. tax\_details.tax\_type

</td><td>

Type of tax applicable on the invoice. Listed in the Tax Type \[sn\_fin\_tax\_type\] table.Target field: u\_tax\_type

Related table: Invoice Tax Line Import \[sn\_spend\_intg\_imp\_invoice\_tax\_line\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices.invoice\_lines.uom

</td><td>

Base unit of measure \(UOM\) used to count the item in the invoice.Target field: u\_uom

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices.invoice\_type

</td><td>

Type of invoice for processing.Target field: u\_invoice\_type

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices.legal\_entity

</td><td>

Name of the legal entity of the supplier. Located in the Legal Entity \[sn\_fin\_legal\_entity\] table.Target field: u\_legal\_entity

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices.original\_invoice

</td><td>

Unique invoice number created by the supplier.Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Target field: u\_original\_invoice

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices.other\_charges

</td><td>

Other additional charges associated with the invoice. This is an editable field.Target field: u\_other\_charges

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices.payment\_terms

</td><td>

The agreed upon time and conditions under which a payment to a supplier is made. For example, `Net 30`.Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices.purchase\_order

</td><td>

Required. Purchase order number that is provided by the customer for this order. Listed in the Purchase Order \[sn\_shop\_purchase\_order\] table.Target field: u\_purchase\_order

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 40

</td></tr><tr><td>

invoices.remit\_address

</td><td>

Required. The street address to which the payment is made.Target field: u\_remit\_address

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices.remit\_to\_city

</td><td>

Required. The city to which the payment is made.Target field: u\_remit\_to\_city

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices.remit\_to\_country

</td><td>

Required. The country to which the payment is made in ISO 3166 format. For example, `US`.Target field: u\_remit\_to\_country

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices. remit\_to\_state\_or\_province

</td><td>

Required. The state or province to which the payment is made.Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices. remit\_to\_zip\_or\_postal\_code

</td><td>

Required. The zip or postal code to which the payment is made.Target field: u\_remit\_to\_state\_or\_province

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices.ship\_from\_city

</td><td>

City from which the items on the purchase order are shipped.Target field: u\_ship\_from\_city

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices.ship\_from\_country

</td><td>

Country from which the items on the purchase order are shipped.Target field: u\_ship\_from\_country

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices. ship\_from\_state\_or\_province

</td><td>

State from which the items on the purchase order are shipped.Target field: u\_ship\_from\_state\_or\_province

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices.ship\_from\_street

</td><td>

Street from which the items on the purchase order are shipped.Target field: u\_ship\_from\_street

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices. ship\_from\_zip\_or\_postal\_code

</td><td>

Zip code from which the items on the purchase order are shipped.Target field: u\_ship\_from\_zip\_or\_postal\_code

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices.ship\_to\_city

</td><td>

City to which the items on the purchase order are shipped.Target field: u\_ship\_to\_city

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices.ship\_to\_country

</td><td>

Country to which the items on the purchase order are shipped.Target field: u\_ship\_to\_country

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices. ship\_to\_state\_or\_province

</td><td>

State to which the items on the purchase order are shipped.Target field: u\_ship\_to\_state\_or\_province

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices.ship\_to\_street

</td><td>

Street to which the items on the purchase order are shipped.Target field: u\_ship\_to\_street

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices. ship\_to\_zip\_or\_postal\_code

</td><td>

Zip code to which the items on the purchase order are shipped.Target field: u\_ship\_to\_zip\_or\_postal\_code

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices.shipping\_amount

</td><td>

Required. Total shipping cost for the entire purchase.Target field: u\_shipping\_amount

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 40

</td></tr><tr><td>

invoices.subtotal

</td><td>

Required. Total amount of money to be paid to the supplier excluding tax and shipping charges.Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 40

</td></tr><tr><td>

invoices.supplier

</td><td>

Required. Identifier for the reseller or supplier that the customer can place orders with.Target field: u\_supplier

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices. supplier\_invoice\_number

</td><td>

Required. Identification number that is generated by a supplier for this invoice.Target field: u\_supplier\_invoice\_number

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices.supplier\_tax\_id

</td><td>

Tax identifier that is associated with the third party reseller. This is an editable field.Target field: u\_supplier\_tax\_id

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Data type: String

Maximum length: 100

</td></tr><tr><td>

invoices.target\_erp

</td><td>

ERP record in which the invoice is posted. Located in the ERP Source \[sn\_fin\_erp\_source\] table. See [ERP source](https://www.servicenow.com/docs/access?context=erp-source&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US).Data type: String

</td></tr><tr><td>

invoices. supporting\_attachments

</td><td>

List of attachments defined at the invoice processing case level for cases assigned to Accounts Payable Specialists. See [Invoice processing case form](https://www.servicenow.com/docs/access?context=invoice-processing-case-form&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US).Once created, the system will generate the invoice record along with the associated invoice case and invoice lines. Attachments will be linked to their respective records accordingly.

Data type: Array of Objects

```
"supporting_attachments": [
  {
    "content": "String",
    "encoding": "String",
    "mime_code": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

invoices. supporting\_attachments.content

</td><td>

Base64-encoded file content of the attachment.Data type: String

</td></tr><tr><td>

invoices. supporting\_attachments.encoding

</td><td>

This value is always `base64`.Data type: String

</td></tr><tr><td>

invoices. supporting\_attachments.mime\_code

</td><td>

This value is always `base64`.Data type: String

</td></tr><tr><td>

invoices. supporting\_attachments.name

</td><td>

File name of the attachment.**Note:** Do not use the reserved "SD\_" prefix for an attachment file name.

Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content-Type

</td><td>

Data format of the request body. Only supports **application/json**.

</td></tr><tr><td>

Source-System

</td><td>

Specifies the source system from which the request is coming from.This setting helps to determine if the request provided follows the structure in the Invoice integration field mapping \[sn\_spend\_intg\_invoice\_intg\_field\_mapping\] table.

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|202|Request Accepted. The request is successful and invoice processing is in progress.|
|400|Bad Request. A bad request type or malformed request was detected.|
|429|Too Many Requests. The request rate has exceeded the maximum of 10 requests per hour.|

### Response body parameters

<table id="table_ig4_h1l_ddc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

batch\_id

</td><td>

Unique identifier for the batch request. This ID can be used to track the status of the request. This record is stored in the Invoice integration log \[sn\_spend\_intg\_invoice\_integration\_log\] table.Data type: String

</td></tr><tr><td>

error

</td><td>

Contains error message and details when the request fails.```
{
  "detail": String,
  "message": String
}
```

Data type: Object

</td></tr><tr><td>

error.detail

</td><td>

Additional details about the request error.Possible results:

-   Failed API level ACL Validation - User does not have read/write access to the resource.
-   Rate limit of 13 requests per hour for AP Invoice exceeded – The number of records in the batch is more than the batch size set.
-   Required to provide Auth information - Either the password is wrong or user name is wrong.

Data type: String

</td></tr><tr><td>

error.message

</td><td>

Error message containing the reason the request failedPossible errors:

-   Invalid payload - Invalid content type.
-   Invalid payload - Error: Invalid payload structure.
-   Invalid payload - Error: Payload exceeds allowed invoices limit in a batch. The number of records in the batch is more than the batch size set. The maximum default payload size is 100 records. This value is configurable in the **sn\_spend\_intg.ap.invoice.create.api.record\_limit** system property.
-   Invalid payload - Error: Empty invoices. No data to process. The number of records in the batch is zero.
-   Rate limit of 500 requests per hour for APO Invoice Ingestion exceeded.
-   User Not Authenticated. Either the password is wrong or user name is wrong.
-   Failed API level ACL Validation - User does not have read/write access to the resource.

Data type: String

</td></tr><tr><td>

message

</td><td>

Success message, for example, `Your request has been successfully received and is being processed`.You can view the status of the request in the Invoice integration log \[sn\_spend\_intg\_invoice\_integration\_log\] table.

Data type: String

</td></tr><tr><td>

status

</td><td>

Indicates the result of the request.Possible values:

-   Success
-   Fail

Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to process an invoice provided as a request in JSON format. Base64 encoding varies in size and can be very large. The content value has been truncated to conserve space. The information reflects proper payload structure.

```
curl "https://instance.servicenow.com/api/sn_spend_intg/v1/ap_invoice/json" \
--request \
 POST \
--header \
 "Source-System: Coupa" \
--header \
 "Content-Type: application/json" \
--user 'username' \
:'password' \
--data \
 '{
  "invoices": [
    {
      "invoice_type": "",
      "supplier_invoice_number": "2InvoiceAttach_A1",
      "external_invoice_number": "EXT-INV-erp-po-1_Attach1",
      "supplier": "",
      "business_owner": "lara.croft@example.com",
      "purchase_order": "",
      "date_format": "DD MMMM, YYYY",
      "invoice_date": "2nd June, 2021",
      "payment_terms": "Net 30",
      "legal_entity": "AUS",
      "subtotal": "(100.00)",
      "shipping_amount": "30.00",
      "other_charges": "20.00",
      "discounts": "00.00",
      "amount_invoiced": "200.00",
      "currency": "USD",
      "invoice_line_count": "10",
      "ship_to_city": "New York",
      "ship_to_country": "USA",
      "ship_to_state_or_province": "NY",
      "ship_to_street": "123 Main St",
      "ship_to_zip_or_postal_code": "10001",
      "ship_from_city": "Los Angeles",
      "ship_from_country": "USA",
      "ship_from_state_or_province": "CA",
      "ship_from_street": "456 Oak Ave",
      "ship_from_zip_or_postal_code": "90001",
      "remit_address": "789 Elm St, Suite 200",
      "remit_to_city": "Chicago",
      "remit_to_country": "USA",
      "remit_to_state_or_province": "IL",
      "remit_to_zip_or_postal_code": "60601",
      "supplier_tax_id": "123456789",
      "invoice_copy_attachment": [
        {
          "file_name": "InvoiceTestInv_Json_A1.pdf",
          "mime_code": "application/pdf",
          "encoding": "base64",
          "content": "JVBERi0xLjQKJaqrrK0KMSAwIG9iago8PAovVGl0bGUgKFBERiBQcmV/Base64EncodingIntentionallyTruncated"
        },
        {
          "file_name": "InvoiceTestINVIMG_Json_A1.jpg",
          "mime_code": "image/jpeg",
          "encoding": "base64",
          "content": "iVBORw0KGgoAAAANSUhEUgAAA0YAAALUCAYAAAAv/SLkAAAMTmlDQ1B/Base64EncodingIntentionallyTruncated"
        }
      ],
      "tax_details": [
        {
          "tax_type": "CGST",
          "tax_amount": "10",
          "tax_rate": ""
        },
        {
          "tax_type": "Withholding tax",
          "tax_amount": "",
          "tax_rate": "25"
        },
        {
          "tax_type": "Sales tax",
          "tax_amount": "12",
          "tax_rate": "12"
        }
      ],
      "invoice_lines": [
        {
          "external_invoice_number": "EXT-INV-erp-po-1",
          "line_description": "2INV_Line_Attach_A1",
          "po_line_description": "",
          "purchase_order_line": "",
          "line_quantity": "5",
          "line_unit_price": "20.00",
          "subtotal": "200.00",
          "line_amount_invoiced": "118.00",
          "currency": "USD",
          "cost_center": "ACN00001",
          "gl_account": "100001",
          "tax_code": "A1 - Sales tax, reduced rate",
          "ship_to_city": "New York",
          "ship_to_country": "USA",
          "ship_to_state_or_province": "NY",
          "ship_to_street": "123 Main St",
          "ship_to_zip_or_postal_code": "10001",
          "supplier_part_number": "SPN-001",
          "uom": "Hours",
          "attachments": [
            {
              "file_name": "InvoiceTestLine.pdf",
              "mime_code": "application/pdf",
              "encoding": "base64",
              "content": "JVBERi0xLjQKJaqrrK0KMSAwIG9iago8PAovVGl0bGUgKFBERiBQc/Base64EncodingIntentionallyTruncated"
            },
            {
              "file_name": "InvoiceTest1Line.jpg",
              "mime_code": "image/jpeg",
              "encoding": "base64",
              "content": "iVBORw0KGgoAAAANSUhEUgAAA0YAAALUCAYAAAAv/SLkAAAMTmlDQ1BJQ0MgUHJvZmW2GWCy8SpAszALlJ/Mv6HK54/f/3/XFv4ysU57JMAAAAASUVORK5CYII="
            }
          ]
        },
        {
          "external_invoice_number": "EXT-INV-erp-po-3",
          "line_description": "Testing",
          "po_line_description": "",
          "purchase_order_line": "",
          "line_quantity": "5",
          "line_unit_price": "20.00",
          "subtotal": "200.00",
          "line_amount_invoiced": "118.00",
          "currency": "USD",
          "cost_center": "ACN00005",
          "gl_account": "100002",
          "tax_code": "A1 - Sales tax, reduced rate",
          "ship_to_city": "New York",
          "ship_to_country": "USA",
          "ship_to_state_or_province": "NY",
          "ship_to_street": "123 Main St",
          "ship_to_zip_or_postal_code": "10001",
          "supplier_part_number": "SPN-001",
          "uom": "Hours"
        }
      ]
    },
    {
      "invoice_type": "",
      "supplier_invoice_number": "10MultiInvoiceAttach_A2",
      "external_invoice_number": "EXT-INV-noerp-PO_Attach_A2",
      "purchase_order": "0004531004",
      "supplier": "880733",
      "date_format": "DD-MM-YYYY",
      "invoice_date": "02-05-2021",
      "payment_terms": "NET 30",
      "legal_entity": "XYZ Ltd.",
      "subtotal": "100",
      "shipping_amount": "30.00",
      "other_charges": "20.00",
      "discounts": "10.00",
      "amount_invoiced": "140.00",
      "currency": "USD",
      "invoice_line_count": "1",
      "ship_to_city": "New York",
      "ship_to_country": "USA",
      "ship_to_state_or_province": "NY",
      "ship_to_street": "123 Main St",
      "ship_to_zip_or_postal_code": "10001",
      "ship_from_city": "Los Angeles",
      "ship_from_country": "USA",
      "ship_from_state_or_province": "CA",
      "ship_from_street": "456 Oak Ave",
      "ship_from_zip_or_postal_code": "90001",
      "remit_address": "789 Elm St, Suite 200",
      "remit_to_city": "Chicago",
      "remit_to_country": "USA",
      "remit_to_state_or_province": "IL",
      "remit_to_zip_or_postal_code": "60601",
      "supplier_tax_id": "12340009",
      "supporting_attachments": [
        {
          "file_name": "10InvcCaseTstInv_Json_A2.pdf",
          "mime_code": "application/pdf",
          "encoding": "base64",
          "content": "JVBERi0xLjQKJaqrrK0KMSAwIG9iago8PAovVGl0bGUgKFBERiBQcmVzZW50YXRpb24gOTY3MTUxMzkw/Base64EncodingIntentionallyTruncated"
        },
        {
          "file_name": "10InvcCaseTstPNGInv_Json_A2.png",
          "mime_code": "image/png",
          "encoding": "base64",
          "content": "iVBORw0KGgoAAAANSUhEUgAAA0YAAALUCAYAAAAv/SLkAAAMTmlDQ1BJQ0MgUHJvZmlsZQAASImVVwdY/Base64EncodingIntentionallyTruncated"
        },
        {
          "file_name": "10InvcCaseTstInv2_Json_A2.pdf",
          "mime_code": "application/pdf",
          "encoding": "base64",
          "content": "JVBERi0xLjQKJaqrrK0KMSAwIG9iago8PAovVGl0bGUgKFBERiBQcmVzZW50YXRpb24gOTY3MTQzNjgzKQovQXV0aG9yIChQYWdlcm8gQUIpCi9Td/Base64EncodingIntentionallyTruncated"
        },
        {
          "file_name": "10InvcCaseTstXMLINV_Json_A2.xml",
          "mime_code": "text/xml",
          "encoding": "base64",
          "content": "PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiIHN0YW5kYWxvbmU9I/Base64EncodingIntentionallyTruncated"
        },
        {
          "file_name": "10InvcCaseTtExcelINV_Json_A2.xlsx",
          "mime_code": "application/vnd.ms-excel",
          "encoding": "base64",
          "content": "UEsDBBQABgAIAAAAIQCpD2g4fwEAAAIFAAATAAgCW0NvbnRlbnRfVHlwZXNdLnhtbCCiBAIooAACAAAAAAAAAAAAAA/Base64EncodingIntentionallyTruncated"
        },
        {
          "file_name": "10InvcCaseTstCSVINV_Json_A2.csv",
          "mime_code": "text/csv",
          "encoding": "base64",
          "content": "Im51bWJlciIsInN1cHBsaWVyX2ludm9pY2VfbnVtYmVyIiwic3VwcGxpZXIiLCJzdGF0ZSIsInR5cGUiLCJkd/Base64EncodingIntentionallyTruncated"
        },
        {
          "file_name": "10InvcCaseTstJsonINV_Json_A2.json",
          "mime_code": "application/json",
          "encoding": "base64",
          "content": "eyJyZWNvcmRzIjpbeyJyZXF1aXJlc19hY2tub3dsZWRnZW1lbnQiOiJmYWxzZSIsInRheF9hbW91buYm91bmRfc291cmNlIjoiIn1dfQ==/Base64EncodingIntentionallyTruncated"
        },
        {
          "file_name": "10InvcCaseTstdocINV_Json_A2.docx",
          "mime_code": "application/vnd.openxmlformats-officedocument.wordprocessingml.document",
          "encoding": "base64",
          "content": "UEsDBBQABgAIAAAAIQDnIQddcAEAANcFAAATAAgCW0NvbnRlbnRfVHlwZXNdLnhtbCCiBAIooAACAAAAAAAAAAA/Base64EncodingIntentionallyTruncated"
        },
        {
          "file_name": "10InvoiceCasePPT_Json_A2.pptx",
          "mime_code": "application/vnd.ms-powerpoint",
          "encoding": "base64",
          "content": "UEsDBBQABgAIAAAAIQAPBpW0tQEAAHgMAAATAAgCW0NvbnRlbnRfVHlwZXNdLnhtbCCiB="
        },
        {
          "file_name": "10InvoiceCaseRichText_Json_A2.rtf",
          "mime_code": "application/rtf",
          "encoding": "base64",
          "content": "e1xydGYxXGFuc2lcYW5zaWNwZzEyNTJcY29jb2FydGYyODIyClxjb2NvYXRleHRzY2FsaW5nMFxjb2NvYXBsYXRmb3JtM/Base64EncodingIntentionallyTruncated"
        },
        {
          "file_name": "10InvcCaseTst_INVJPG_Json_A2.jpg",
          "mime_code": "image/jpeg",
          "encoding": "base64",
          "content": "/9j/4AAQSkZJRgABAQEA8ADwAAD/2wCEAAoHBwcIBwoICAoPCggKDxINCgoNEhQQEBIQEB/Base64EncodingIntentionallyTruncated"
        }
      ],
      "invoice_copy_attachment": [
        {
          "file_name": "10InvoiceTestInv_Json_A2.pdf",
          "mime_code": "application/pdf",
          "encoding": "base64",
          "content": "JVBERi0xLjQKJaqrrK0KMSAwIG9iago8PAovVGl0bGUgKFBERiBQcmVzZW50YXRpb24g/Base64EncodingIntentionallyTruncated"
        },
        {
          "file_name": "10InvoiceTestInv_Json_A2.jpg",
          "mime_code": "image/jpeg",
          "encoding": "base64",
          "content": "iVBORw0KGgoAAAANSUhEUgAAA0YAAALUCAYAAAAv/SLkAAAMTmlDQ1BJQ0MgUHJvZmls/Base64EncodingIntentionallyTruncated"
        },
        {
          "file_name": "10InvceTstInv2_Json_A2.pdf",
          "mime_code": "application/pdf",
          "encoding": "base64",
          "content": "JVBERi0xLjQKJaqrrK0KMSAwIG9iago8PAovVGl0bGUgKFBERiBQcmVzZW50YXRpb24g=/Base64EncodingIntentionallyTruncated"
        },
        {
          "file_name": "10InvoiceTestXMLINV_Json_A2.xml",
          "mime_code": "text/xml",
          "encoding": "base64",
          "content": "PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiIHN0YW5kYWxvbmU9Im5vI/Base64EncodingIntentionallyTruncated"
        },
        {
          "file_name": "10InvoiceTestExcelINV_Json_A2.xlsx",
          "mime_code": "application/vnd.ms-excel",
          "encoding": "base64",
          "content": "UEsDBBQABgAIAAAAIQCpD2g4fwEAAAIFAAATAAgCW0NvbnRlbnRfVHlwZXNdLnhtbCCiBAIooAACAAAAAAAAAAAAAA=/Base64EncodingIntentionallyTruncated"
        },
        {
          "file_name": "10InvoiceTestCSVINV_Json_A2.csv",
          "mime_code": "text/csv",
          "encoding": "base64",
          "content": "Im51bWJlciIsInN1cHBsaWVyX2ludm9pY2VfbnVtYmVyIiwic3VwcGxpZXIiLCJzd/Base64EncodingIntentionallyTruncated"
        },
        {
          "file_name": "10InvoiceTestJsonINV_Json_A2.json",
          "mime_code": "application/json",
          "encoding": "base64",
          "content": "eyJyZWNvcmRzIjpbeyJyZXF1aXJlc19hY2tub3dsZWRnZW1lbnQiOiJmYWxzZSI/Base64EncodingIntentionallyTruncated"
        },
        {
          "file_name": "10InvoiceTestdocINV_Json_A2.docx",
          "mime_code": "application/vnd.openxmlformats-officedocument.wordprocessingml.document",
          "encoding": "base64",
          "content": "UEsDBBQABgAIAAAAIQDnIQddcAEAANcFAAATAAgCW0NvbnRlbnRfVHlwZXNdLnht/Base64EncodingIntentionallyTruncated"
        },
        {
          "file_name": "10InvoicePPT_Json_A2.pptx",
          "mime_code": "application/vnd.ms-powerpoint",
          "encoding": "base64",
          "content": "UEsDBBQABgAIAAAAIQAPBpW0tQEAAHgMAAATAAgCW0NvbnRlbnRfVHlwZXNdLnhtb/Base64EncodingIntentionallyTruncated"
        },
        {
          "file_name": "10InvoiceRichText_Json_A2.rtf",
          "mime_code": "application/rtf",
          "encoding": "base64",
          "content": "e1xydGYxXGFuc2lcYW5zaWNwZzEyNTJcY29jb2FydGYyODIyClxjb2NvYXRleHRz/Base64EncodingIntentionallyTruncated"
        }
      ],
      "tax_details": [
        {
          "tax_type": "Value added tax",
          "tax_amount": "21",
          "tax_rate": ""
        },
        {
          "tax_type": "IGST",
          "tax_amount": "",
          "tax_rate": "22"
        },
        {
          "tax_type": "Withholding tax",
          "tax_amount": "23",
          "tax_rate": ""
        }
      ],
      "invoice_lines": [
        {
          "external_invoice_number": "EXT-INV-noerp-PO_Attach_A2",
          "purchase_order_line": "00045310041",
          "po_line_description": "Yeti microphone - black",
          "line_description": "10MultiInvoiceLineAttach_A2",
          "line_quantity": "5",
          "line_unit_price": "20.00",
          "subtotal": "200.00-",
          "line_amount_invoiced": "97.00",
          "currency": "USD",
          "cost_center": "ACN00001",
          "gl_account": "141150",
          "tax_code": "A0 - Sales tax, standard rate",
          "ship_to_city": "New York",
          "ship_to_country": "USA",
          "ship_to_state_or_province": "NY",
          "ship_to_street": "123 Main St",
          "ship_to_zip_or_postal_code": "10001",
          "supplier_part_number": "SPN-001",
          "uom": "Hours",
          "attachments": [
            {
              "file_name": "10InvoiceTest_INVLine_Json_A2.pdf",
              "mime_code": "application/pdf",
              "encoding": "base64",
              "content": "JVBERi0xLjQKJaqrrK0KMSAwIG9iago8PAovVGl0bGUgKFBERiBQcmVzZW50/Base64EncodingIntentionallyTruncated"
            },
            {
              "file_name": "10InvoiceTest_INVLine_Json_A2.jpg",
              "mime_code": "image/jpeg",
              "encoding": "base64",
              "content": "iVBORw0KGgoAAAANSUhEUgAAA0YAAALUCAYAAAAv/SLkAAAMTmlDQ1BJQ0Mg/Base64EncodingIntentionallyTruncated"
            },
            {
              "file_name": "10InvceTst2_INVLine_Json_A2.pdf",
              "mime_code": "application/pdf",
              "encoding": "base64",
              "content": "JVBERi0xLjQKJaqrrK0KMSAwIG9iago8PAovVGl0bGUgKFBERiBQcmVzZW50Y/Base64EncodingIntentionallyTruncated"
            },
            {
              "file_name": "10InvoiceTestXML_INVLine_Json_A2.xml",
              "mime_code": "text/xml",
              "encoding": "base64",
              "content": "PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiIHN0YW5kYWxv/Base64EncodingIntentionallyTruncated"
            },
            {
              "file_name": "10InvoiceTestExcel_INVLine_Json_A2.xlsx",
              "mime_code": "application/vnd.ms-excel",
              "encoding": "base64",
              "content": "UEsDBBQABgAIAAAAIQCpD2g4fwEAAAIFAAATAAgCW0NvbnRlbnRfVHlwZX/Base64EncodingIntentionallyTruncated"
            },
            {
              "file_name": "10InvoiceTestdoc_INVLine_Json_A2.docx",
              "mime_code": "application/vnd.openxmlformats-officedocument.wordprocessingml.document",
              "encoding": "base64",
              "content": "UEsDBBQABgAIAAAAIQDnIQddcAEAANcFAAATAAgCW0NvbnRlbnRfVHlwZX/Base64EncodingIntentionallyTruncated"
            },
            {
              "file_name": "10_InvoiceLinePPT_Json_A2.pptx",
              "mime_code": "application/vnd.ms-powerpoint",
              "encoding": "base64",
              "content": "UEsDBBQABgAIAAAAIQAPBpW0tQEAAHgMAAATAAgCW0NvbnRlbnRfVHlwZX/Base64EncodingIntentionallyTruncated"
            },
            {
              "file_name": "10_InvoiceLineRichText_Json_A2.rtf",
              "mime_code": "application/rtf",
              "encoding": "base64",
              "content": "e1xydGYxXGFuc2lcYW5zaWNwZzEyNTJcY29jb2FydGYyODIyClxjb2NvYX/Base64EncodingIntentionallyTruncated"
            }
          ],
          "tax_details": [
            {
              "tax_type": "IGST",
              "tax_amount": "",
              "tax_rate": "3.4"
            },
            {
              "tax_type": "GST",
              "tax_amount": "3.9",
              "tax_rate": ""
            },
            {
              "tax_type": "VAT",
              "tax_amount": "2",
              "tax_rate": "4"
            }
          ]
        },
        {
          "external_invoice_number": "EXT-INV-noerp-PO",
          "purchase_order_line": "00045310041",
          "po_line_description": "Yeti microphone - black",
          "line_description": "Testing ERP POL",
          "line_quantity": "5",
          "line_unit_price": "20.00",
          "subtotal": "200.00-",
          "line_amount_invoiced": "97.00",
          "currency": "USD",
          "cost_center": "ACN00001",
          "gl_account": "141150",
          "tax_code": "A0 - Sales tax, standard rate",
          "ship_to_city": "New York",
          "ship_to_country": "USA",
          "ship_to_state_or_province": "NY",
          "ship_to_street": "123 Main St",
          "ship_to_zip_or_postal_code": "10001",
          "supplier_part_number": "SPN-001",
          "uom": "Hours",
          "tax_details": [
            {
              "tax_type": "IGST",
              "tax_amount": "",
              "tax_rate": "3.4"
            },
            {
              "tax_type": "GST",
              "tax_amount": "3.9",
              "tax_rate": ""
            },
            {
              "tax_type": "VAT",
              "tax_amount": "2",
              "tax_rate": "4"
            }
          ]
        },
        {
          "external_invoice_number": "EXT-INV-noerp-PO_Attach3",
          "purchase_order_line": "00045310042",
          "po_line_description": "Pv-3310 photo tripod w/3-way pan",
          "line_description": "Date Formate Test",
          "line_quantity": "5",
          "line_unit_price": "20.00",
          "subtotal": "100.00",
          "line_amount_invoiced": "97.00",
          "currency": "USD",
          "cost_center": "ACN00002",
          "gl_account": "100005",
          "tax_code": "A0 - Sales tax, standard rate",
          "ship_to_city": "New York",
          "ship_to_country": "USA",
          "ship_to_state_or_province": "NY",
          "ship_to_street": "123 Main St",
          "ship_to_zip_or_postal_code": "10001",
          "supplier_part_number": "SPN-001",
          "uom": "Hours",
          "tax_details": [
            {
              "tax_type": "IGST",
              "tax_amount": "",
              "tax_rate": "3.2"
            },
            {
              "tax_type": "Withholding tax",
              "tax_amount": "",
              "tax_rate": "4"
            },
            {
              "tax_type": "VAT",
              "tax_amount": "",
              "tax_rate": "3"
            }
          ],
          "attachments": [
            {
              "file_name": "InvoiceLinePPT.pptx",
              "mime_code": "application/vnd.ms-powerpoint",
              "encoding": "base64",
              "content": "UEsDBBQABgAIAAAAIQAPBpW0tQEAAHgMAAATAAgCW0NvbnRlbnRfVHlwZXN/Base64EncodingIntentionallyTruncated"
            },
            {
              "file_name": "InvoiceLineRichText.rtf",
              "mime_code": "application/rtf",
              "encoding": "base64",
              "content": "e1xydGYxXGFuc2lcYW5zaWNwZzEyNTJcY29jb2FydGYyODIyClxjb2NvYX/Base64EncodingIntentionallyTruncated"
            }
          ]
        },
        {
          "external_invoice_number": "EXT-INV-noerp-PO-01",
          "purchase_order_line": "00045310042",
          "po_line_description": "Yeti microphone - black",
          "line_description": "",
          "line_quantity": "5",
          "line_unit_price": "20.00",
          "subtotal": "100.00",
          "line_amount_invoiced": "97.00",
          "currency": "USD",
          "cost_center": "ACN00005",
          "gl_account": "141101",
          "tax_code": "A0 - Sales tax, standard rate",
          "ship_to_city": "New York",
          "ship_to_country": "USA",
          "ship_to_state_or_province": "NY",
          "ship_to_street": "123 Main St",
          "ship_to_zip_or_postal_code": "10001",
          "supplier_part_number": "SPN-001",
          "uom": "Hours",
          "tax_details": [
            {
              "tax_type": "SGST",
              "tax_amount": "",
              "tax_rate": "3.1"
            },
            {
              "tax_type": "GST",
              "tax_amount": "3.8",
              "tax_rate": ""
            },
            {
              "tax_type": "CGST",
              "tax_amount": "",
              "tax_rate": "1.2"
            }
          ]
        }
      ]
    },
    {
      "invoice_type": "",
      "supplier_invoice_number": "LineLevelTax_Attach3",
      "external_invoice_number": "EXT-INV-noerp-PO-line_attach3",
      "purchase_order": "",
      "supplier": "880733",
      "date_format": "mm-dd-yyyy",
      "invoice_date": "09-05-2021",
      "payment_terms": "NET 30",
      "legal_entity": "1100.",
      "subtotal": "100",
      "shipping_amount": "30.00",
      "other_charges": "20.00",
      "discounts": "10.00-",
      "amount_invoiced": "140.00",
      "currency": "USD",
      "invoice_line_count": "1",
      "ship_to_city": "New York",
      "ship_to_country": "USA",
      "ship_to_state_or_province": "NY",
      "ship_to_street": "123 Main St",
      "ship_to_zip_or_postal_code": "10001",
      "ship_from_city": "Los Angeles",
      "ship_from_country": "USA",
      "ship_from_state_or_province": "CA",
      "ship_from_street": "456 Oak Ave",
      "ship_from_zip_or_postal_code": "90001",
      "remit_address": "789 Elm St, Suite 200",
      "remit_to_city": "Chicago",
      "remit_to_country": "USA",
      "remit_to_state_or_province": "IL",
      "remit_to_zip_or_postal_code": "60601",
      "supplier_tax_id": "12340009",
      "invoice_copy_attachment": [
        {
          "file_name": "InvoicePPT.pptx",
          "mime_code": "application/vnd.ms-powerpoint",
          "encoding": "base64",
          "content": "UEsDBBQABgAIAAAAIQAPBpW0tQEAAHgMAAATAAgCW0NvbnRlbnRfVHlwZXNdLnh/Base64EncodingIntentionallyTruncated"
        },
        {
          "file_name": "InvoiceRichText.rtf",
          "mime_code": "application/rtf",
          "encoding": "base64",
          "content": "e1xydGYxXGFuc2lcYW5zaWNwZzEyNTJcY29jb2FydGYyODIyClxjb2NvYXRleH/Base64EncodingIntentionallyTruncated"
        }
      ],
      "invoice_lines": [
        {
          "external_invoice_number": "EXT-INV-noerp-PO-3",
          "purchase_order_line": "00045310041",
          "po_line_description": "Yeti microphone - black",
          "line_description": "Testing ERP POL",
          "line_quantity": "5",
          "line_unit_price": "20.00",
          "subtotal": "200.00",
          "line_amount_invoiced": "97.00",
          "currency": "USD",
          "cost_center": "ACN00005",
          "gl_account": "120040",
          "tax_code": "A0 - Sales tax, standard rate",
          "ship_to_city": "New York",
          "ship_to_country": "USA",
          "ship_to_state_or_province": "NY",
          "ship_to_street": "123 Main St",
          "ship_to_zip_or_postal_code": "10001",
          "supplier_part_number": "SPN-001",
          "uom": "Hours",
          "tax_details": [
            {
              "tax_type": "IGST",
              "tax_amount": "",
              "tax_rate": "6"
            },
            {
              "tax_type": "GST",
              "tax_amount": "7",
              "tax_rate": ""
            },
            {
              "tax_type": "Sales tax",
              "tax_amount": "8",
              "tax_rate": "8"
            }
          ]
        },
        {
          "external_invoice_number": "EXT-INV-noerp-PO-3",
          "purchase_order_line": "00045310042",
          "po_line_description": "Pv-3310 photo tripod w/3-way pan",
          "line_description": "Date Formate Test",
          "line_quantity": "5",
          "line_unit_price": "20.00",
          "subtotal": "200.00",
          "line_amount_invoiced": "97.00",
          "currency": "USD",
          "cost_center": "ACN00001",
          "gl_account": "141250",
          "tax_code": "A0 - Sales tax, standard rate",
          "ship_to_city": "New York",
          "ship_to_country": "USA",
          "ship_to_state_or_province": "NY",
          "ship_to_street": "123 Main St",
          "ship_to_zip_or_postal_code": "10001",
          "supplier_part_number": "SPN-001",
          "uom": "Hours",
          "tax_details": [
            {
              "tax_type": "CGST",
              "tax_amount": "",
              "tax_rate": "4.1"
            },
            {
              "tax_type": "SGST",
              "tax_amount": "4.4",
              "tax_rate": ""
            },
            {
              "tax_type": "VAT",
              "tax_amount": "",
              "tax_rate": "4.3"
            }
          ]
        },
        {
          "external_invoice_number": "EXT-INV-noerp-PO-3",
          "purchase_order_line": "00045310042",
          "po_line_description": "Yeti microphone - black",
          "line_description": "",
          "line_quantity": "5",
          "line_unit_price": "20.00",
          "subtotal": "100.00",
          "line_amount_invoiced": "97.00",
          "currency": "USD",
          "cost_center": "ACN00007",
          "gl_account": "141300",
          "tax_code": "A0 - Sales tax, standard rate",
          "ship_to_city": "New York",
          "ship_to_country": "USA",
          "ship_to_state_or_province": "NY",
          "ship_to_street": "123 Main St",
          "ship_to_zip_or_postal_code": "10001",
          "supplier_part_number": "SPN-001",
          "uom": "Hours",
          "tax_details": [
            {
              "tax_type": "IGST",
              "tax_amount": "",
              "tax_rate": "2.4"
            },
            {
              "tax_type": "Withholding tax",
              "tax_amount": "5.5",
              "tax_rate": ""
            },
            {
              "tax_type": "VAT",
              "tax_amount": "2.6",
              "tax_rate": ""
            }
          ]
        }
      ]
    },
    {
      "invoice_type": "credit_memo",
      "supplier_invoice_number": "EXT-INV-erp-po_AttachLine",
      "external_invoice_number": "EXT-INV-erp-po_AttachLine",
      "original_invoice": "INV0001013",
      "supplier": "",
      "business_owner": "lara.croft@example.com",
      "purchase_order": "0004889699",
      "invoice_date": "09/13/2024",
      "payment_terms": "Net 30",
      "legal_entity": "AUS",
      "subtotal": "150.00",
      "shipping_amount": "30.00",
      "other_charges": "20.00",
      "discounts": "00.00",
      "amount_invoiced": "200.00",
      "currency": "USD",
      "invoice_line_count": "10",
      "ship_to_city": "New York",
      "ship_to_country": "USA",
      "ship_to_state_or_province": "NY",
      "ship_to_street": "123 Main St",
      "ship_to_zip_or_postal_code": "10001",
      "ship_from_city": "Los Angeles",
      "ship_from_country": "USA",
      "ship_from_state_or_province": "CA",
      "ship_from_street": "456 Oak Ave",
      "ship_from_zip_or_postal_code": "90001",
      "remit_address": "789 Elm St, Suite 200",
      "remit_to_city": "Chicago",
      "remit_to_country": "USA",
      "remit_to_state_or_province": "IL",
      "remit_to_zip_or_postal_code": "60601",
      "supplier_tax_id": "123456789",
      "tax_details": [
        {
          "tax_type": "CGST",
          "tax_amount": "15",
          "tax_rate": ""
        },
        {
          "tax_type": "Sales tax",
          "tax_amount": "",
          "tax_rate": "10"
        },
        {
          "tax_type": "SGST",
          "tax_amount": "10",
          "tax_rate": ""
        }
      ],
      "invoice_lines": [
        {
          "external_invoice_number": "EXT-INV-erp-po_AttachLine",
          "line_description": "POL ERP number Attachment on line only",
          "po_line_description": "",
          "purchase_order_line": "00048896991",
          "line_quantity": "5",
          "line_unit_price": "20.00",
          "subtotal": "100.00",
          "line_amount_invoiced": "118.00",
          "currency": "USD",
          "cost_center": "ACN00004",
          "gl_account": "436000",
          "tax_code": "A1 - Sales tax, reduced rate",
          "ship_to_city": "New York",
          "ship_to_country": "USA",
          "ship_to_state_or_province": "NY",
          "ship_to_street": "123 Main St",
          "ship_to_zip_or_postal_code": "10001",
          "supplier_part_number": "SPN-001",
          "attachments": [
            {
              "file_name": "InvoiceLinePPT.pptx",
              "mime_code": "application/vnd.ms-powerpoint",
              "encoding": "base64",
              "content": "UEsDBBQABgAIAAAAIQAPBpW0tQEAAHgMAAATAAgCW0NvbnRlbnRfVHlwZXN/Base64EncodingIntentionallyTruncated""
            },
            {
              "file_name": "InvoiceLineRichText.rtf",
              "mime_code": "application/rtf",
              "encoding": "base64",
              "content": "e1xydGYxXGFuc2lcYW5zaWNwZzEyNTJcY29jb2FydGYyODIyClxjb2NvYXRl/Base64EncodingIntentionallyTruncated"
          ],
          "uom": "Hours"
        }
      ]
    }
  ],
  "target_erp": ""
}'
```

The following result shows that the request is successful and the invoice data is processing. You can view the status of the request in the Invoice integration log \[sn\_spend\_intg\_invoice\_integration\_log\] table. Use the batch ID listed in the Batch ID column to find the invoice.

```
{
    "batchId": "APIINV1729711710733280",
    "status": "Success",
    "message": "Your request has been successfully received and is being processed."
}
```

## AP Invoice – POST sn\_spend\_intg/ap\_invoice/xml

Processes an automated invoice in XML format.

Use the Invoice integration field mappings \[sn\_spend\_intg\_invoice\_intg\_field\_mapping\] table to determine how the fields are mapped to XML tags.

You can define custom invoice fields for the request body. Use the following flow to add custom fields, map them to target tables, and format them for availability in the payload:

1.  [Add custom fields for invoice import](../../guides/APInvoiceAPI/concept/apInvoice-dev-guide.md#)
2.  [Map custom fields between source and target tables](../../guides/APInvoiceAPI/concept/apInvoice-dev-guide.md#)
3.  [Map custom fields to a payload source format](../../guides/APInvoiceAPI/concept/apInvoice-dev-guide.md#)

### URL format

Versioned URL: `/api/sn_spend_intg/v1/ap_invoice/xml`

Default URL: `/api/sn_spend_intg/ap_invoice/xml`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Path

</th><th>

Description

</th></tr></thead><tbody><tr><td>

/Invoice/AmountInvoiced

</td><td>

Total amount of money to be paid to the supplier including tax and shipping charges.Target field: u\_amount\_invoiced

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

Invoice/BillToCity

</td><td>

The city to which the invoice is sent.Target field: u\_bill\_to\_city

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/Invoice/BillToCountry

</td><td>

The country to which the invoice is sent in ISO 3166 format. For example, `US`.Target field: u\_bill\_to\_country

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/Invoice/BillToStateOrProvince

</td><td>

The state or province to which the invoice is sent.Target field: u\_bill\_to\_state\_or\_province

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/Invoice/BillToStreet

</td><td>

The street address to which the invoice is sent.Target field: u\_bill\_to\_street

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/Invoice/BillToZipOrPostalCode

</td><td>

The zip or postal code to which the invoice is sent.Target field: u\_bill\_to\_zip\_or\_postal\_code

</td></tr><tr><td>

/Invoice/Currency

</td><td>

Required. Currency for subtotal, tax, and shipping. The subtotal, tax, and shipping should be in the same currency.Target field: u\_currency

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/Invoice/DateFormat

</td><td>

Sets the invoice date format from the default YYYY-MM-DD to another supported date format. The date value is set in the **InvoiceDate** element.Supported date formats:

-   DD MMM YYYY
-   DD MMM, YY
-   DD MMM, YYYY
-   DD MMMM YYYY
-   DD MMMM, YY
-   DD MMMM, YYYY
-   DD-MM-YY
-   DD-MM-YYYY
-   DD-MMM-YY
-   DD-MMM-YYYY
-   DD.MM.YY
-   DD.MM.YYYY
-   DD/MM/YY
-   DD/MM/YYYY
-   dd/mmm/yyyy
-   MM-DD-YY
-   MM-DD-YYYY
-   MM.DD.YY
-   MM.DD.YYYY
-   MM/DD/YY
-   MM/DD/YYYY
-   MMM DD YYYY
-   MMM DD, YY
-   MMM DD, YYYY
-   MMMM DD YYYY
-   MMMM DD, YY
-   MMMM DD, YYYY
-   YY-MM-DD
-   YY.MM.DD
-   YY/MM/DD
-   YYYY-MM-DD \(default\)
-   YYYY.MM.DD
-   YYYY/MM/DD

**Note:** The MMM format entry represents a month in its first three letters, for example, Aug. The MMMM format entry represents the full month name, for example, August.

Target field: u\_date\_format

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Default format: YYYY-MM-DD

</td></tr><tr><td>

/Invoice/Discounts

</td><td>

Discounts that are applied toward the invoice.Target field: u\_discounts

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/Invoice/ExternalInvoiceNumber

</td><td>

Invoice number generated from a third-party application.Target field: u\_external\_invoice\_number

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/Invoice/InvoiceDate

</td><td>

Date on which the customer was invoiced. Use the **DateFormat** element to add the date in a supported non-default format.Target field: u\_invoice\_date

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

Default format: YYYY-MM-DD

</td></tr><tr><td>

/Invoice/LegalEntity

</td><td>

Name of the legal entity of the supplier. Located in the Legal Entity \[sn\_fin\_legal\_entity\] table.Target field: u\_legal\_entity

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/Invoice/OtherCharges

</td><td>

Other additional charges associated with the invoice. This is an editable field.Target field: u\_other\_charges

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/Invoice/PaymentTerms

</td><td>

The agreed upon time and conditions under which a payment to a supplier is made. For example, `Net 30`.Target field: u\_payment\_terms

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/Invoice/RemitAddress

</td><td>

The street address to which the payment is made.Target field: u\_remit\_address

</td></tr><tr><td>

Invoice/RemitToCity

</td><td>

The city to which the payment is made.Target field: u\_remit\_to\_city

</td></tr><tr><td>

/Invoice/RemitToCountry

</td><td>

The country to which the payment is made in ISO 3166 format. For example, `US`.Target field: u\_remit\_to\_country

</td></tr><tr><td>

/Invoice/RemitToStateOrProvince

</td><td>

The state or province to which the payment is made.Target field: u\_remit\_to\_state\_or\_province

</td></tr><tr><td>

/Invoice/RemitToZipOrPostalCode

</td><td>

The zip or postal code to which the payment is made.Target field: u\_remit\_to\_zip\_or\_postal\_code

</td></tr><tr><td>

/Invoice/ShipFromCity

</td><td>

City from which the items on the purchase order are shipped.Target field: u\_ship\_from\_city

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/Invoice/ShipFromCountry

</td><td>

Country from which the items on the purchase order are shipped.Target field: u\_ship\_from\_country

Related table: Invoice Line \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/Invoice/ShipFromStateOrProvince

</td><td>

State from which the items on the purchase order are shipped.Target field: u\_ship\_from\_state\_or\_province

Related table: Invoice Line \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/Invoice/ShipFromStreet

</td><td>

Street from which the items on the purchase order are shipped.Target field: u\_ship\_from\_street

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/Invoice/ShipFromZipOrPostalCode

</td><td>

Zip code from which the items on the purchase order are shipped.Target field: u\_ship\_from\_zip\_or\_postal\_code

Related table: Invoice Line \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/Invoice/ShippingAmount

</td><td>

Total shipping cost for the entire purchase.Target field: u\_shipping\_amount

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/Invoice/Subtotal

</td><td>

Total amount of money to be paid to the supplier excluding tax and shipping charges.Target field: u\_subtotal

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/Invoice/Supplier

</td><td>

Identifier for the reseller or supplier that the customer can place orders with.Target field: u\_supplier

Related table: Invoice Import \[sn\_spend\_intg\_imp\_invoice\]

</td></tr><tr><td>

/Invoice/SupportingAttachments

</td><td>

List of attachments defined at the invoice processing case level for cases assigned to Accounts Payable Specialists. See [Invoice processing case form](https://www.servicenow.com/docs/access?context=invoice-processing-case-form&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US).Once created, the system will generate the invoice record along with the associated invoice case and invoice lines. Attachments will be linked to their respective records accordingly.

</td></tr><tr><td>

/Invoice/SupportingAttachments/Attachment/

</td><td>

Contains the details for a single attachment.

</td></tr><tr><td>

/Invoice/SupportingAttachments/Attachment/Content

</td><td>

Base64-encoded file content of the attachment.

</td></tr><tr><td>

/Invoice/SupportingAttachments/Attachment/Encoding

</td><td>

This value is always `base64`.

</td></tr><tr><td>

/Invoice/SupportingAttachments/Attachment/FileName

</td><td>

File name of the attachment.**Note:** Do not use the reserved "SD\_" prefix for an attachment file name.

</td></tr><tr><td>

/Invoice/SupportingAttachments/Attachment/MimeCode

</td><td>

This value is always `base64`.

</td></tr><tr><td>

/Invoice/InvoiceCopyAttachment/

</td><td>

List of attachments defined at the invoice level. See [Accounts Payable Invoice Processing](https://www.servicenow.com/docs/access?context=acc-pay-invoice-processing&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US).Once created, the system will generate the invoice record along with the associated invoice case and invoice lines. Attachments will be linked to their respective records accordingly.

</td></tr><tr><td>

/Invoice/InvoiceCopyAttachment/Attachment/

</td><td>

Contains the details for a single attachment.

</td></tr><tr><td>

/Invoice/InvoiceCopyAttachment/Attachment/Content

</td><td>

Base64-encoded file content of the attachment.

</td></tr><tr><td>

/Invoice/InvoiceCopyAttachment/Attachment/Encoding

</td><td>

This value is always `base64`.

</td></tr><tr><td>

/Invoice/InvoiceCopyAttachment/Attachment/FileName

</td><td>

File name of the attachment.**Note:** Do not use the reserved "SD\_" prefix for an attachment file name.

</td></tr><tr><td>

/Invoice/InvoiceCopyAttachment/Attachment/MimeCode

</td><td>

This value is always `base64`.

</td></tr><tr><td>

/Invoice/InvoiceLines/

</td><td>

List of InvoiceLine elements that define the lines that are being invoiced for purchases within this order.

</td></tr><tr><td>

/InvoiceLine/

</td><td>

Invoice line definition. Invoice lines are staged in the Invoice line import inbound \[sn\_spend\_intg\_imp\_invoice\_line\] table.

</td></tr><tr><td>

/InvoiceLine/Attachment/

</td><td>

Contains the details for a single attachment.

</td></tr><tr><td>

/InvoiceLine/Attachment/Content

</td><td>

Base64-encoded file content of the attachment.

</td></tr><tr><td>

/InvoiceLine/Attachment/Encoding

</td><td>

This value is always `base64`.

</td></tr><tr><td>

/InvoiceLine/Attachment/FileName

</td><td>

File name of the attachment.**Note:** Do not use the reserved "SD\_" prefix for an attachment file name.

</td></tr><tr><td>

/InvoiceLine/Attachment/MimeCode

</td><td>

This value is always `base64`.

</td></tr><tr><td>

/InvoiceLine/CostCenter

</td><td>

Account number of the cost center for which the invoice is generated. Listed in the Cost Center \[cmn\_cost\_center\] table.Target field: u\_cost\_center

</td></tr><tr><td>

/InvoiceLine/Currency

</td><td>

Currency for the line item. For example, `USD`.Target field: u\_currency

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

/InvoiceLine/GLAccount

</td><td>

Account number of the general ledger \(GL\) used to generate the invoice.Target field: u\_gl\_account

See also:

-   [ERP source](https://www.servicenow.com/docs/access?context=erp-source&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)
-   [Ledger account](https://www.servicenow.com/docs/access?context=ledger-account&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)

</td></tr><tr><td>

/InvoiceLine/LineAmountInvoiced

</td><td>

Total cost, excluding taxes and shipping, that a customer is being invoiced for a given purchase order line.Target field: u\_line\_amount\_invoiced

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

/InvoiceLine/LineDescription

</td><td>

Description of the invoice line.Target field: u\_line\_description

</td></tr><tr><td>

/InvoiceLine/LineQuantity

</td><td>

Quantity of goods or services that a customer is being invoiced for.Target field: u\_line\_quantity

</td></tr><tr><td>

/InvoiceLine/LineUnitPrice

</td><td>

Unit price of the line item in the invoice.Target field: u\_line\_unit\_price

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

/InvoiceLine/POLineDescription

</td><td>

Description of the purchase order line for the invoice.Target field: u\_po\_line\_description

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

/InvoiceLine/PurchaseOrderLine

</td><td>

Purchase order number that is provided by the customer for this order. Listed in the Purchase Order \[sn\_shop\_purchase\_order\] table.Target field: u\_purchase\_order

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

/InvoiceLine/ShipToCity

</td><td>

City to which the items on the purchase order are shipped.Target field: u\_ship\_to\_city

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

/InvoiceLine/ShipToCountry

</td><td>

Country to which the items on the purchase order are shipped.Target field: u\_ship\_to\_country

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

/InvoiceLine/ShipToStateOrProvince

</td><td>

State or province to which the items on the purchase order are shipped.Target field: u\_ship\_to\_state\_or\_province

</td></tr><tr><td>

/InvoiceLine/ShipToStreet

</td><td>

Street to which the items on the purchase order are shipped.Target field: u\_ship\_to\_street

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

/InvoiceLine/ShipToZipOrPostalCode

</td><td>

Zip code to which the items on the purchase order are shipped.Target field: u\_ship\_to\_zip\_or\_postal\_code

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

/InvoiceLine/Subtotal

</td><td>

Total amount of money to be paid to the supplier excluding tax and shipping charges.Target field: u\_subtotal

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

/InvoiceLine/SupplierPartNumber

</td><td>

Part number that is generated by a supplier for this invoice line.Target field: u\_supplier\_part\_number

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

/InvoiceLine/TaxCode

</td><td>

Unique tax code generated from the ERP source.Target field: u\_tax\_code

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

/InvoiceLine/UOM

</td><td>

Base unit of measure \(UOM\) used to count the item in the invoice.Target field: u\_uom

Related table: Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]

</td></tr><tr><td>

/TaxDetail/TaxType

</td><td>

Type of tax applicable on the invoice. Listed in the Tax Type \[sn\_fin\_tax\_type\] table.Target field: u\_tax\_type

Related table: Invoice Tax Line Import \[sn\_spend\_intg\_imp\_invoice\_tax\_line\]

</td></tr><tr><td>

/TaxDetail/TaxRate

</td><td>

The tax rate charged by the supplier.Related table: Invoice Tax Line Import \[sn\_spend\_intg\_imp\_invoice\_tax\_line\]

Target field: u\_supplier\_tax\_rate

Related table: Invoice Tax Line Import \[sn\_spend\_intg\_imp\_invoice\_tax\_line\]

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content-Type

</td><td>

Data format of the request body. Only supports **application/xml**.

</td></tr><tr><td>

Source-System

</td><td>

Specifies the source system from which the request is coming from.Available systems are listed in the Source systems credentials \[sn\_spend\_intg\_source\_system\_credential\] table.

This setting helps to determine if the request provided follows the structure in the Invoice integration field mapping \[sn\_spend\_intg\_invoice\_intg\_field\_mapping\] table.

This setting is also used to fetch credentials from the Source system credentials \[sn\_spend\_intg\_source\_system\_credential\] table.

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|202|Request Accepted. The request is successful and invoice processing is in progress.|
|400|Bad Request. A bad request type or malformed request was detected.|
|429|Too Many Requests. The request rate has exceeded the maximum of 10 requests per hour.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

batch\_id

</td><td>

Unique identifier for the batch request. This ID can be used to track the status of the request. This record is stored in the Invoice integration log \[sn\_spend\_intg\_invoice\_integration\_log\] table.Data type: String

</td></tr><tr><td>

error

</td><td>

Contains error message and details when the request fails.```
{
  "detail": String,
  "message": String
}
```

Data type: Object

</td></tr><tr><td>

error.detail

</td><td>

Additional details about the request error.Possible results:

-   Failed API level ACL Validation - User does not have read/write access to the resource.
-   Rate limit of 13 requests per hour for AP Invoice exceeded – The number of records in the batch is more than the batch size set.
-   Required to provide Auth information - Either the password is wrong or user name is wrong.

Data type: String

</td></tr><tr><td>

error.message

</td><td>

Error message containing the reason the request failedPossible errors:

-   Invalid payload - Invalid content type.
-   Invalid payload - Error: Invalid payload structure.
-   Invalid payload - Error: Payload exceeds allowed invoices limit in a batch. The number of records in the batch is more than the batch size set. The maximum default payload size is 100 records. This value is configurable in the **sn\_spend\_intg.ap.invoice.create.api.record\_limit** system property.
-   Invalid payload - Error: Empty invoices. No data to process. The number of records in the batch is zero.
-   Rate limit of 500 requests per hour for APO Invoice Ingestion exceeded.
-   User Not Authenticated. Either the password is wrong or user name is wrong.
-   Failed API level ACL Validation - User does not have read/write access to the resource.

Data type: String

</td></tr><tr><td>

message

</td><td>

Success message, for example, `Your request has been successfully received and is being processed`.You can view the status of the request in the Invoice integration log \[sn\_spend\_intg\_invoice\_integration\_log\] table.

Data type: String

</td></tr><tr><td>

status

</td><td>

Indicates the result of the request.Possible values:

-   Success
-   Fail

Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to process an invoice provided as a request in XML format. Base64 encoding varies in size and can be very large. The content value has been truncated to conserve space. The information reflects proper payload structure.

```
curl -X POST https://instance.servicenow.com/api/sn_spend_intg/v1/ap_invoice/xml \
-H "Source-System: Ariba" \
-H "Content-Type: application/json" \
-d '<Invoices>
    <Invoice>
        <InvoiceType>po_invoice</InvoiceType>
        <SupplierInvoiceNumber>S-AttachmentInvoice-A1-SupportDoc1</SupplierInvoiceNumber>
        <ExternalInvoiceNumber>EXT-INV-#00A1</ExternalInvoiceNumber>
        <Supplier>3245545</Supplier>
        <PurchaseOrder>###0004889698</PurchaseOrder>
        <BusinessOwner>paula.smith@example.com</BusinessOwner>
        <DateFormat>DD-MMM-YY</DateFormat>
        <InvoiceDate>16-DEC-24</InvoiceDate>
        <PaymentTerms>Net 60</PaymentTerms>
        <LegalEntity>US</LegalEntity>
        <Subtotal>100.00</Subtotal>
        <ShippingAmount>20.00</ShippingAmount>
        <OtherCharges>20</OtherCharges>
        <Discounts>10</Discounts>
        <AmountInvoiced>150.00</AmountInvoiced>
        <Currency>USD</Currency>
        <InvoiceLineCount>1</InvoiceLineCount>
        <ShipToCity>Los Angeles</ShipToCity>
        <ShipToCountry>USA</ShipToCountry>
        <ShipToStateOrProvince>CA</ShipToStateOrProvince>
        <ShipToStreet>456 Oak Ave</ShipToStreet>
        <ShipToZipOrPostalCode>90001</ShipToZipOrPostalCode>
        <ShipFromCity>Addison</ShipFromCity>
        <ShipFromCountry>USA</ShipFromCountry>
        <ShipFromStateOrProvince>TX</ShipFromStateOrProvince>
        <ShipFromStreet>15725 Dallas P</ShipFromStreet>
        <ShipFromZipOrPostalCode>55555</ShipFromZipOrPostalCode>
        <RemitAddress>47 W 11th St</RemitAddress>
        <RemitToCity>New York</RemitToCity>
        <RemitToCountry>USA</RemitToCountry>
        <RemitToStateOrProvince>NY</RemitToStateOrProvince>
        <RemitToZipOrPostalCode>99999</RemitToZipOrPostalCode>
        <BillToStreet>4810 Eastgate Mall</BillToStreet>
        <BillToCity>San Diego</BillToCity>
        <BillToCountry>USA</BillToCountry>
        <BillToStateOrProvince>CA</BillToStateOrProvince>
        <BillToZipOrPostalCode>92121</BillToZipOrPostalCode>
        <SupplierTaxID>7894328742</SupplierTaxID>
        <TaxDetails>
            <TaxDetail>
                <TaxType>Sales tax</TaxType>
                <TaxAmount>10</TaxAmount>
                <TaxRate></TaxRate>
            </TaxDetail>
            <TaxDetail>
                <TaxType>CGST</TaxType>
                <TaxAmount></TaxAmount>
                <TaxRate>11</TaxRate>
            </TaxDetail>
            <TaxDetail>
                <TaxType>IGST</TaxType>
                <TaxAmount>12</TaxAmount>
                <TaxRate>12</TaxRate>
            </TaxDetail>
            <TaxDetail>
                <TaxType>Withholding tax</TaxType>
                <TaxAmount>13</TaxAmount>
                <TaxRate></TaxRate>
            </TaxDetail>
        </TaxDetails>
        <SupportingAttachments>
            <Attachment>
                <FileName>InvoiceCaseSupportingDoc.png</FileName>
                <MimeCode>image/png</MimeCode>
                <Encoding>base64</Encoding>
                <Content>iVBORw0KGgoAAAANSUhEUgAAA0YAAALUCAYAAAAv/SLkAAAMTmlDQ1BJQ/Base64EncodingIntentionallyTruncated=</Content>
            </Attachment>
            <Attachment>
                <FileName>InvoiceImageA1.jpg</FileName>
                <MimeCode>image/jpeg</MimeCode>
                <Encoding>base64</Encoding>
                <Content>/9j/4AAQSkZJRgABAQEA8ADwAAD/2wCEAAoHBwcIBwoICAoPCggKDxINC/Base64EncodingIntentionallyTruncated=</Content>
            </Attachment>
        </SupportingAttachments>
        <InvoiceCopyAttachment>
            <Attachment>
                <FileName>InvoiceA1.pdf</FileName>
                <MimeCode>application/pdf</MimeCode>
                <Encoding>base64</Encoding>
                <Content>JVBERi0xLjQKJaqrrK0KMSAwIG9iago8PAovVGl0bGUgKFBERiBQcmVzZ/Base64EncodingIntentionallyTruncated=</Content>
            </Attachment>
            <Attachment>
                <FileName>InvoiceImageA1.jpg</FileName>
                <MimeCode>image/jpeg</MimeCode>
                <Encoding>base64</Encoding>
                <Content>/9j/4AAQSkZJRgABAQEA8ADwAAD/2wCEAAoHBwcIBwoICAoPCggKDxINC/Base64EncodingIntentionallyTruncated=</Content>
            </Attachment>
        </InvoiceCopyAttachment>
        <InvoiceLines>
            <InvoiceLine>
                <ExternalInvoiceNumber>EXT-INV-#00A1</ExternalInvoiceNumber>
                <LineDescription>Invoice_Line_Attach_A1</LineDescription>
                <PurchaseOrderLine>POL11232</PurchaseOrderLine>
                <POLineDescription>NowX Charger</POLineDescription>
                <LineQuantity>10</LineQuantity>
                <LineUnitPrice>10.00</LineUnitPrice>
                <Subtotal>200.00</Subtotal>
                <LineAmountInvoiced>100</LineAmountInvoiced>
                <Currency>USD</Currency>
                <CostCenter>ACN00001</CostCenter>
                <GLAccount>100005</GLAccount>
                <TaxCode>A1 - Sales tax, reduced rate</TaxCode>
                <ShipToCity>New York</ShipToCity>
                <ShipToCountry>USA</ShipToCountry>
                <ShipToStateOrProvince>New York</ShipToStateOrProvince>
                <ShipToStreet>PA112</ShipToStreet>
                <ShipToZipOrPostalCode>1001</ShipToZipOrPostalCode>
                <SupplierPartNumber>SPN1211</SupplierPartNumber>
                <UOM>Individual Unit</UOM>
                <Attachments>
                    <Attachment>
                        <FileName>InvoiceLineA1.png</FileName>
                        <MimeCode>image/png</MimeCode>
                        <Encoding>base64</Encoding>
                        <Content>iVBORw0KGgoAAAANSUhEUgAAA0YAAALUCAYAAAAv/SLkAAAMT/Base64EncodingIntentionallyTruncated=</Content>
                    </Attachment>
                </Attachments>
            </InvoiceLine>
            <InvoiceLine>
                <ExternalInvoiceNumber>EXT-INV-#00A</ExternalInvoiceNumber>
                <LineDescription>InvoiceLine_PDF_Attach_A1</LineDescription>
                <PurchaseOrderLine>00048896981</PurchaseOrderLine>
                <POLineDescription></POLineDescription>
                <LineQuantity>10</LineQuantity>
                <LineUnitPrice>10.00</LineUnitPrice>
                <Subtotal>200.00</Subtotal>
                <LineAmountInvoiced>100</LineAmountInvoiced>
                <Currency>USD</Currency>
                <CostCenter>ACN00005</CostCenter>
                <GLAccount>120050</GLAccount>
                <TaxCode>A1 - Sales tax, reduced rate</TaxCode>
                <ShipToCity>New York</ShipToCity>
                <ShipToCountry>USA</ShipToCountry>
                <ShipToStateOrProvince>New York</ShipToStateOrProvince>
                <ShipToStreet>PA112</ShipToStreet>
                <ShipToZipOrPostalCode>1001</ShipToZipOrPostalCode>
                <SupplierPartNumber>SPN1211</SupplierPartNumber>
                <UOM>Individual Unit</UOM>
                <Attachments>
                    <Attachment>
                        <FileName>Invoice_line_A1.pdf</FileName>
                        <MimeCode>application/pdf</MimeCode>
                        <Encoding>base64</Encoding>
                        <Content>JVBERi0xLjQKJaqrrK0KMSAwIG9iago8PAovVGl0bGUgKFBER/Base64EncodingIntentionallyTruncated=</Content>
                    </Attachment>
                    <Attachment>
                        <FileName>InvoiceImageA1.jpg</FileName>
                        <MimeCode>image/jpeg</MimeCode>
                        <Encoding>base64</Encoding>
                        <Content>/9j/4AAQSkZJRgABAQEA8ADwAAD/2wCEAAoHBwcIBwoICAoPC/Base64EncodingIntentionallyTruncated=</Content>
                    </Attachment>
                </Attachments>
            </InvoiceLine>
        </InvoiceLines>
    </Invoice>
    <Invoice>
        <InvoiceType>non_po_invoice</InvoiceType>
        <SupplierInvoiceNumber>10MultiAttach_Inv_invline_A2-MultiSupp</SupplierInvoiceNumber>
        <ExternalInvoiceNumber>EXT-INV-#00A2</ExternalInvoiceNumber>
        <Supplier>3245545</Supplier>
        <BusinessOwner>paula.smith@example.com</BusinessOwner>
        <DateFormat>DD-MMM-YYYY</DateFormat>
        <InvoiceDate>10-Nov-2024</InvoiceDate>
        <PaymentTerms>Net 60</PaymentTerms>
        <LegalEntity>1100</LegalEntity>
        <Subtotal>120.00</Subtotal>
        <ShippingAmount>10.00</ShippingAmount>
        <OtherCharges>10</OtherCharges>
        <Discounts>10</Discounts>
        <AmountInvoiced>150.00</AmountInvoiced>
        <Currency>USD</Currency>
        <InvoiceLineCount>1</InvoiceLineCount>
        <ShipToCity>Los Angeles</ShipToCity>
        <ShipToCountry>USA</ShipToCountry>
        <ShipToStateOrProvince>CA</ShipToStateOrProvince>
        <ShipToStreet>456 Oak Ave</ShipToStreet>
        <ShipToZipOrPostalCode>90001</ShipToZipOrPostalCode>
        <ShipFromCity>Addison</ShipFromCity>
        <ShipFromCountry>USA</ShipFromCountry>
        <ShipFromStateOrProvince>TX</ShipFromStateOrProvince>
        <ShipFromStreet>15725 Dallas P</ShipFromStreet>
        <ShipFromZipOrPostalCode>55555</ShipFromZipOrPostalCode>
        <RemitAddress>47 W 11th St</RemitAddress>
        <RemitToCity>New York</RemitToCity>
        <RemitToCountry>USA</RemitToCountry>
        <RemitToStateOrProvince>NY</RemitToStateOrProvince>
        <RemitToZipOrPostalCode>99999</RemitToZipOrPostalCode>
        <BillToStreet>4810 Eastgate Mall</BillToStreet>
        <BillToCity>San Diego</BillToCity>
        <BillToCountry>USA</BillToCountry>
        <BillToStateOrProvince>CA</BillToStateOrProvince>
        <BillToZipOrPostalCode>92121</BillToZipOrPostalCode>
        <SupplierTaxID>7894328742</SupplierTaxID>
        <TaxDetails>
            <TaxDetail>
                <TaxType>Value added tax</TaxType>
                <TaxAmount>8</TaxAmount>
                <TaxRate></TaxRate>
            </TaxDetail>
            <TaxDetail>
                <TaxType>Withholding tax</TaxType>
                <TaxAmount></TaxAmount>
                <TaxRate>7</TaxRate>
            </TaxDetail>
        </TaxDetails>
        <SupportingAttachments>
            <Attachment>
                <FileName>10InvoiceCaseTestInv_Xml_A2.pdf</FileName>
                <MimeCode>application/pdf</MimeCode>
                <Encoding>base64</Encoding>
                <Content>JVBERi0xLjQKJaqrrK0KMSAwIG9iago8PAovVGl0bGUgKFBERiBQcmVzZ/Base64EncodingIntentionallyTruncated=</Content>
            </Attachment>
            <Attachment>
                <FileName>10InvoiceCasePNGInv_Xml_A2.png</FileName>
                <MimeCode>image/png</MimeCode>
                <Encoding>base64</Encoding>
                <Content>iVBORw0KGgoAAAANSUhEUgAAA0YAAALUCAYAAAAv/SLkAAAMTmlDQ1BJQ/Base64EncodingIntentionallyTruncated=</Content>
            </Attachment>
            <Attachment>
                <FileName>10InvceCaseTst2Inv_Xml_A2.pdf</FileName>
                <MimeCode>application/pdf</MimeCode>
                <Encoding>base64</Encoding>
                <Content>JVBERi0xLjQKJaqrrK0KMSAwIG9iago8PAovVGl0bGUgKFBERiBQcmVzZ/Base64EncodingIntentionallyTruncated=</Content>
            </Attachment>
            <Attachment>
                <FileName>10InvoiceCaseTestXMLINV_Xml_A2.xml</FileName>
                <MimeCode>text/xml</MimeCode>
                <Encoding>base64</Encoding>
                <Content>PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiIHN0YW5kY/Base64EncodingIntentionallyTruncated=</Content>
            </Attachment>
            <Attachment>
                <FileName>10InvoiceCaseTestExcelINV_Xml_A2.xlsx</FileName>
                <MimeCode>application/vnd.ms-excel</MimeCode>
                <Encoding>base64</Encoding>
                <Content>UEsDBBQABgAIAAAAIQCpD2g4fwEAAAIFAAATAAgCW0NvbnRlbnRfVHlwZ/Base64EncodingIntentionallyTruncated=</Content>
            </Attachment>
            <Attachment>
                <FileName>10InvoiceCaseTestdocINV_Xml_A2.docx</FileName>
                <MimeCode>application/vnd.openxmlformats-officedocument.wordprocessingml.document</MimeCode>
                <Encoding>base64</Encoding>
                <Content>UEsDBBQABgAIAAAAIQDnIQddcAEAANcFAAATAAgCW0NvbnRlbnRfVHlwZ/Base64EncodingIntentionallyTruncated=</Content>
            </Attachment>
            <Attachment>
                <FileName>10InvoiceCasePPT_Xml_A2.pptx</FileName>
                <MimeCode>application/vnd.ms-powerpoint</MimeCode>
                <Encoding>base64</Encoding>
                <Content>UEsDBBQABgAIAAAAIQAPBpW0tQEAAHgMAAATAAgCW0NvbnRlbnRfVHlwZ/Base64EncodingIntentionallyTruncated=</Content>
            </Attachment>
            <Attachment>
                <FileName>10InvoiceCaseRichText_Xml_A2.rtf</FileName>
                <MimeCode>application/rtf</MimeCode>
                <Encoding>base64</Encoding>
                <Content>e1xydGYxXGFuc2lcYW5zaWNwZzEyNTJcY29jb2FydGYyODIyClxjb2Nv/Base64EncodingIntentionallyTruncated=</Content>
            </Attachment>
            <Attachment>
                <FileName>10InvoiceCaseImageJpeg_XML_A2.jpg</FileName>
                <MimeCode>image/jpeg</MimeCode>
                <Encoding>base64</Encoding>
                <Content>/9j/4AAQSkZJRgABAQEA8ADwAAD/2wCEAAoHBwcIBwoICAoPCggKDxINC/Base64EncodingIntentionallyTruncated=</Content>
            </Attachment>
        </SupportingAttachments>
        <InvoiceCopyAttachment>
            <Attachment>
                <FileName>10InvoiceTestInv_Xml_A2.pdf</FileName>
                <MimeCode>application/pdf</MimeCode>
                <Encoding>base64</Encoding>
                <Content>JVBERi0xLjQKJaqrrK0KMSAwIG9iago8PAovVGl0bGUgKFBERiBQcmVzZ/Base64EncodingIntentionallyTruncated=</Content>
            </Attachment>
            <Attachment>
                <FileName>10InvoicePNGInv_Xml_A2.png</FileName>
                <MimeCode>image/png</MimeCode>
                <Encoding>base64</Encoding>
                <Content>iVBORw0KGgoAAAANSUhEUgAAA0YAAALUCAYAAAAv/SLkAAAMTmlDQ1BJQ/Base64EncodingIntentionallyTruncated=</Content>
            </Attachment>
            <Attachment>
                <FileName>10InvceTst2Inv_Xml_A2.pdf</FileName>
                <MimeCode>application/pdf</MimeCode>
                <Encoding>base64</Encoding>
                <Content>JVBERi0xLjQKJaqrrK0KMSAwIG9iago8PAovVGl0bGUgKFBERiBQcmVzZ/Base64EncodingIntentionallyTruncated=</Content>
            </Attachment>
            <Attachment>
                <FileName>10InvoiceTestXMLINV_Xml_A2.xml</FileName>
                <MimeCode>text/xml</MimeCode>
                <Encoding>base64</Encoding>
                <Content>PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiIHN0YW5kY/Base64EncodingIntentionallyTruncated=</Content>
            </Attachment>
            <Attachment>
                <FileName>10InvoiceTestExcelINV_Xml_A2.xlsx</FileName>
                <MimeCode>application/vnd.ms-excel</MimeCode>
                <Encoding>base64</Encoding>
                <Content>UEsDBBQABgAIAAAAIQCpD2g4fwEAAAIFAAATAAgCW0NvbnRlbnRfVHlwZ/Base64EncodingIntentionallyTruncated=</Content>
            </Attachment>
            <Attachment>
                <FileName>10InvoiceTestCSVINV_Xml_A2.csv</FileName>
                <MimeCode>text/csv</MimeCode>
                <Encoding>base64</Encoding>
                <Content>Im51bWJlciIsInN1cHBsaWVyX2ludm9pY2VfbnVtYmVyIiwic3VwcGxp/Base64EncodingIntentionallyTruncated=</Content>
            </Attachment>
            <Attachment>
                <FileName>10InvoiceTestJsonINV_Xml_A2.json</FileName>
                <MimeCode>application/json</MimeCode>
                <Encoding>base64</Encoding>
                <Content>eyJyZWNvcmRzIjpbeyJyZXF1aXJlc19hY2tub3dsZWRnZW1lbnQiOiJmY/Base64EncodingIntentionallyTruncated=</Content>
            </Attachment>
            <Attachment>
                <FileName>10InvoiceTestdocINV_Xml_A2.docx</FileName>
                <MimeCode>application/vnd.openxmlformats-officedocument.wordprocessingml.document</MimeCode>
                <Encoding>base64</Encoding>
                <Content>UEsDBBQABgAIAAAAIQDnIQddcAEAANcFAAATAAgCW0NvbnRlbnRfVHlwZ/Base64EncodingIntentionallyTruncated=</Content>
            </Attachment>
            <Attachment>
                <FileName>10InvoicePPT_Xml_A2.pptx</FileName>
                <MimeCode>application/vnd.ms-powerpoint</MimeCode>
                <Encoding>base64</Encoding>
                <Content>UEsDBBQABgAIAAAAIQAPBpW0tQEAAHgMAAATAAgCW0NvbnRlbnRfVHlwZ/Base64EncodingIntentionallyTruncated=</Content>
            </Attachment>
            <Attachment>
                <FileName>10InvoiceRichText_Xml_A2.rtf</FileName>
                <MimeCode>application/rtf</MimeCode>
                <Encoding>base64</Encoding>
                <Content>e1xydGYxXGFuc2lcYW5zaWNwZzEyNTJcY29jb2FydGYyODIyClxjb2Nv/Base64EncodingIntentionallyTruncated=</Content>
            </Attachment>
            <Attachment>
                <FileName>10InvoiceImageJpeg_XML_A2.jpg</FileName>
                <MimeCode>image/jpeg</MimeCode>
                <Encoding>base64</Encoding>
                <Content>/9j/4AAQSkZJRgABAQEA8ADwAAD/2wCEAAoHBwcIBwoICAoPCggKDxINC/Base64EncodingIntentionallyTruncated=</Content>
            </Attachment>
        </InvoiceCopyAttachment>
        <InvoiceLines>
            <InvoiceLine>
                <ExternalInvoiceNumber>EXT-INV-#00A2</ExternalInvoiceNumber>
                <LineDescription>Apple_MultiAttach_A2</LineDescription>
                <PurchaseOrderLine>48896981</PurchaseOrderLine>
                <POLineDescription>Keyboards</POLineDescription>
                <LineQuantity>12</LineQuantity>
                <LineUnitPrice>10.00</LineUnitPrice>
                <Subtotal>(200.00)</Subtotal>
                <LineAmountInvoiced>100</LineAmountInvoiced>
                <Currency>USD</Currency>
                <CostCenter>ACN00005</CostCenter>
                <GLAccount>141100</GLAccount>
                <TaxCode>A0 Sales Tax</TaxCode>
                <ShipToCity>New York</ShipToCity>
                <ShipToCountry>USA</ShipToCountry>
                <ShipToStateOrProvince>New York</ShipToStateOrProvince>
                <ShipToStreet>PA112</ShipToStreet>
                <ShipToZipOrPostalCode>1001</ShipToZipOrPostalCode>
                <SupplierPartNumber>SPN1211</SupplierPartNumber>
                <UOM>Individual Unit</UOM>
                <TaxDetails>
                    <TaxDetail>
                        <TaxType>SGST</TaxType>
                        <TaxAmount>2</TaxAmount>
                        <TaxRate></TaxRate>
                    </TaxDetail>
                    <TaxDetail>
                        <TaxType>IGST</TaxType>
                        <TaxAmount></TaxAmount>
                        <TaxRate>3</TaxRate>
                    </TaxDetail>
                    <TaxDetail>
                        <TaxType>IGST</TaxType>
                        <TaxAmount>5</TaxAmount>
                        <TaxRate>4</TaxRate>
                    </TaxDetail>
                </TaxDetails>
                <Attachments>
                    <Attachment>
                        <FileName>10InvoiceTestInvLine_Xml_A2.pdf</FileName>
                        <MimeCode>application/pdf</MimeCode>
                        <Encoding>base64</Encoding>
                        <Content>JVBERi0xLjQKJaqrrK0KMSAwIG9iago8PAovVGl0bGUgKFBER/Base64EncodingIntentionallyTruncated=</Content>
                    </Attachment>
                    <Attachment>
                        <FileName>10InvcPNGInvLine_Xml_A2.png</FileName>
                        <MimeCode>image/png</MimeCode>
                        <Encoding>base64</Encoding>
                        <Content>iVBORw0KGgoAAAANSUhEUgAAA0YAAALUCAYAAAAv/SLkAAAMT/Base64EncodingIntentionallyTruncated=</Content>
                    </Attachment>
                    <Attachment>
                        <FileName>10InvTst2InvLine_Xml_A2.pdf</FileName>
                        <MimeCode>application/pdf</MimeCode>
                        <Encoding>base64</Encoding>
                        <Content>JVBERi0xLjQKJaqrrK0KMSAwIG9iago8PAovVGl0bGUgKFBER/Base64EncodingIntentionallyTruncated=</Content>
                    </Attachment>
                    <Attachment>
                        <FileName>10InvoiceTestXMLINVLine_Xml_A2.xml</FileName>
                        <MimeCode>text/xml</MimeCode>
                        <Encoding>base64</Encoding>
                        <Content>PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiIH/Base64EncodingIntentionallyTruncated=</Content>
                    </Attachment>
                    <Attachment>
                        <FileName>10InvoiceTestExcelINVLine_Xml_A2.xlsx</FileName>
                        <MimeCode>application/vnd.ms-excel</MimeCode>
                        <Encoding>base64</Encoding>
                        <Content>UEsDBBQABgAIAAAAIQCpD2g4fwEAAAIFAAATAAgCW0NvbnRlbn/Base64EncodingIntentionallyTruncated=</Content>
                    </Attachment>
                    <Attachment>
                        <FileName>10InvoiceTestCSVINVLine_Xml_A2.csv</FileName>
                        <MimeCode>text/csv</MimeCode>
                        <Encoding>base64</Encoding>
                        <Content>Im51bWJlciIsInN1cHBsaWVyX2ludm9pY2VfbnVtYmVyIiwic/Base64EncodingIntentionallyTruncated=</Content>
                    </Attachment>
                    <Attachment>
                        <FileName>10InvoiceTestJsonINVLine_Xml_A2.json</FileName>
                        <MimeCode>application/json</MimeCode>
                        <Encoding>base64</Encoding>
                        <Content>eyJyZWNvcmRzIjpbeyJyZXF1aXJlc19hY2tub3dsZWRnZW1lb/Base64EncodingIntentionallyTruncated=</Content>
                    </Attachment>
                    <Attachment>
                        <FileName>10InvoiceTestdocINVLine_Xml_A2.docx</FileName>
                        <MimeCode>application/vnd.openxmlformats-officedocument.wordprocessingml.document</MimeCode>
                        <Encoding>base64</Encoding>
                        <Content>UEsDBBQABgAIAAAAIQDnIQddcAEAANcFAAATAAgCW0NvbnRlb/Base64EncodingIntentionallyTruncated=</Content>
                    </Attachment>
                    <Attachment>
                        <FileName>10InvoiceLinePPT_Xml_A2.pptx</FileName>
                        <MimeCode>application/vnd.ms-powerpoint</MimeCode>
                        <Encoding>base64</Encoding>
                        <Content>UEsDBBQABgAIAAAAIQAPBpW0tQEAAHgMAAATAAgCW0NvbnRlb/Base64EncodingIntentionallyTruncated=</Content>
                    </Attachment>
                    <Attachment>
                        <FileName>10InvoiceLineRichText_Xml_A2.rtf</FileName>
                        <MimeCode>application/rtf</MimeCode>
                        <Encoding>base64</Encoding>
                        <Content>e1xydGYxXGFuc2lcYW5zaWNwZzEyNTJcY29jb2FydGYyODIyC/Base64EncodingIntentionallyTruncated=</Content>
                    </Attachment>
                    <Attachment>
                        <FileName>10InvcImageJPG_InvcLine_Xml_A2.jpg</FileName>
                        <MimeCode>image/jpeg</MimeCode>
                        <Encoding>base64</Encoding>
                        <Content>/9j/4AAQSkZJRgABAQEA8ADwAAD/2wCEAAoHBwcIBwoICAoPC/Base64EncodingIntentionallyTruncated=</Content>
                    </Attachment>
                </Attachments>
            </InvoiceLine>
            <InvoiceLine>
                <ExternalInvoiceNumber>EXT-INV-#002</ExternalInvoiceNumber>
                <LineDescription>Negative Tax</LineDescription>
                <PurchaseOrderLine>48896981</PurchaseOrderLine>
                <POLineDescription>Keyboards</POLineDescription>
                <LineQuantity>12</LineQuantity>
                <LineUnitPrice>10.00</LineUnitPrice>
                <Subtotal>200.00</Subtotal>
                <LineAmountInvoiced>100</LineAmountInvoiced>
                <Currency>USD</Currency>
                <CostCenter>ACN00001</CostCenter>
                <GLAccount>100001</GLAccount>
                <TaxCode>A0 Sales Tax</TaxCode>
                <ShipToCity>New York</ShipToCity>
                <ShipToCountry>USA</ShipToCountry>
                <ShipToStateOrProvince>New York</ShipToStateOrProvince>
                <ShipToStreet>PA112</ShipToStreet>
                <ShipToZipOrPostalCode>1001</ShipToZipOrPostalCode>
                <SupplierPartNumber>SPN1211</SupplierPartNumber>
                <UOM>Individual Unit</UOM>
                <TaxDetails>
                    <TaxDetail>
                        <TaxType>Value added tax</TaxType>
                        <TaxAmount></TaxAmount>
                        <TaxRate>6</TaxRate>
                    </TaxDetail>
                    <TaxDetail>
                        <TaxType>Withholding tax</TaxType>
                        <TaxAmount>16</TaxAmount>
                        <TaxRate></TaxRate>
                    </TaxDetail>
                </TaxDetails>
            </InvoiceLine>
        </InvoiceLines>
    </Invoice>
    <Invoice>
        <InvoiceType></InvoiceType>
        <SupplierInvoiceNumber>Both taxes</SupplierInvoiceNumber>
        <ExternalInvoiceNumber>EXT-INV-#008</ExternalInvoiceNumber>
        <Supplier>3245545</Supplier>
        <OriginalInvoice></OriginalInvoice>
        <PurchaseOrder>###0004889698</PurchaseOrder>
        <BusinessOwner>paula.smith@example.com</BusinessOwner>
        <DateFormat>DD MMMM, YY</DateFormat>
        <InvoiceDate>5 June, 24</InvoiceDate>
        <PaymentTerms>Net 60</PaymentTerms>
        <LegalEntity>1100</LegalEntity>
        <Subtotal>100.00</Subtotal>
        <ShippingAmount>10.00</ShippingAmount>
        <OtherCharges>10-</OtherCharges>
        <Discounts>10</Discounts>
        <AmountInvoiced>130.00</AmountInvoiced>
        <Currency>USD</Currency>
        <InvoiceLineCount>1</InvoiceLineCount>
        <ShipToCity>Los Angeles</ShipToCity>
        <ShipToCountry>USA</ShipToCountry>
        <ShipToStateOrProvince>CA</ShipToStateOrProvince>
        <ShipToStreet>456 Oak Ave</ShipToStreet>
        <ShipToZipOrPostalCode>90001</ShipToZipOrPostalCode>
        <ShipFromCity>Addison</ShipFromCity>
        <ShipFromCountry>USA</ShipFromCountry>
        <ShipFromStateOrProvince>TX</ShipFromStateOrProvince>
        <ShipFromStreet>15725 Dallas P</ShipFromStreet>
        <ShipFromZipOrPostalCode>55555</ShipFromZipOrPostalCode>
        <RemitAddress>47 W 11th St</RemitAddress>
        <RemitToCity>New York</RemitToCity>
        <RemitToCountry>USA</RemitToCountry>
        <RemitToStateOrProvince>NY</RemitToStateOrProvince>
        <RemitToZipOrPostalCode>99999</RemitToZipOrPostalCode>
        <BillToStreet>4810 Eastgate Mall</BillToStreet>
        <BillToCity>San Diego</BillToCity>
        <BillToCountry>USA</BillToCountry>
        <BillToStateOrProvince>CA</BillToStateOrProvince>
        <BillToZipOrPostalCode>92121</BillToZipOrPostalCode>
        <SupplierTaxID>7894328742</SupplierTaxID>
        <TaxDetails>
            <TaxDetail>
                <TaxType>SGST</TaxType>
                <TaxAmount>21</TaxAmount>
                <TaxRate></TaxRate>
            </TaxDetail>
            <TaxDetail>
                <TaxType>IGST</TaxType>
                <TaxAmount></TaxAmount>
                <TaxRate>23</TaxRate>
            </TaxDetail>
        </TaxDetails>
        <InvoiceLines>
            <InvoiceLine>
                <ExternalInvoiceNumber>EXT-INV-008</ExternalInvoiceNumber>
                <LineDescription>Apple macbook 15 Pro</LineDescription>
                <PurchaseOrderLine>#ABC00048896981</PurchaseOrderLine>
                <POLineDescription>NowX Laptop</POLineDescription>
                <LineQuantity>10</LineQuantity>
                <LineUnitPrice>10.00</LineUnitPrice>
                <Subtotal>-200.00</Subtotal>
                <LineAmountInvoiced>100</LineAmountInvoiced>
                <Currency>USD</Currency>
                <CostCenter>ACN00005</CostCenter>
                <GLAccount>100001</GLAccount>
                <TaxCode>A0 Sales Tax</TaxCode>
                <ShipToCity>New York</ShipToCity>
                <ShipToCountry>USA</ShipToCountry>
                <ShipToStateOrProvince>New York</ShipToStateOrProvince>
                <ShipToStreet>PA112</ShipToStreet>
                <ShipToZipOrPostalCode>1001</ShipToZipOrPostalCode>
                <SupplierPartNumber>SPN1211</SupplierPartNumber>
                <UOM>Individual Unit</UOM>
                <TaxDetails>
                    <TaxDetail>
                        <TaxType>SGST</TaxType>
                        <TaxAmount>12</TaxAmount>
                        <TaxRate></TaxRate>
                    </TaxDetail>
                </TaxDetails>
            </InvoiceLine>
        </InvoiceLines>
    </Invoice>
    <Invoice>
        <InvoiceType>credit_memo</InvoiceType>
        <SupplierInvoiceNumber>no taxes</SupplierInvoiceNumber>
        <ExternalInvoiceNumber>EXT-INV-#009</ExternalInvoiceNumber>
        <Supplier>3245545</Supplier>
        <OriginalInvoice>Both taxes</OriginalInvoice>
        <PurchaseOrder></PurchaseOrder>
        <BusinessOwner>Paula Smith</BusinessOwner>
        <DateFormat></DateFormat>
        <InvoiceDate>2024-06-03</InvoiceDate>
        <PaymentTerms>Net 60</PaymentTerms>
        <LegalEntity>US</LegalEntity>
        <Subtotal>100.00</Subtotal>
        <ShippingAmount>10.00</ShippingAmount>
        <OtherCharges>10</OtherCharges>
        <Discounts>10</Discounts>
        <AmountInvoiced>130.00</AmountInvoiced>
        <Currency>USD</Currency>
        <InvoiceLineCount>1</InvoiceLineCount>
        <ShipToCity>Los Angeles</ShipToCity>
        <ShipToCountry>USA</ShipToCountry>
        <ShipToStateOrProvince>CA</ShipToStateOrProvince>
        <ShipToStreet>456 Oak Ave</ShipToStreet>
        <ShipToZipOrPostalCode>90001</ShipToZipOrPostalCode>
        <ShipFromCity>Addison</ShipFromCity>
        <ShipFromCountry>USA</ShipFromCountry>
        <ShipFromStateOrProvince>TX</ShipFromStateOrProvince>
        <ShipFromStreet>15725 Dallas P</ShipFromStreet>
        <ShipFromZipOrPostalCode>55555</ShipFromZipOrPostalCode>
        <RemitAddress>47 W 11th St</RemitAddress>
        <RemitToCity>New York</RemitToCity>
        <RemitToCountry>USA</RemitToCountry>
        <RemitToStateOrProvince>NY</RemitToStateOrProvince>
        <RemitToZipOrPostalCode>99999</RemitToZipOrPostalCode>
        <BillToStreet>4810 Eastgate Mall</BillToStreet>
        <BillToCity>San Diego</BillToCity>
        <BillToCountry>USA</BillToCountry>
        <BillToStateOrProvince>CA</BillToStateOrProvince>
        <BillToZipOrPostalCode>92121</BillToZipOrPostalCode>
        <SupplierTaxID>7894328742</SupplierTaxID>
        <InvoiceLines>
            <InvoiceLine>
                <ExternalInvoiceNumber>EXT-INV-008</ExternalInvoiceNumber>
                <LineDescription>Apple macbook 15 Pro</LineDescription>
                <PurchaseOrderLine>#ABC00048896981</PurchaseOrderLine>
                <POLineDescription>NowX Laptop</POLineDescription>
                <LineQuantity>10</LineQuantity>
                <LineUnitPrice>10.00-</LineUnitPrice>
                <Subtotal>100.00</Subtotal>
                <LineAmountInvoiced>100</LineAmountInvoiced>
                <Currency>USD</Currency>
                <CostCenter>ACN00005</CostCenter>
                <GLAccount>141200</GLAccount>
                <TaxCode>A0 Sales Tax</TaxCode>
                <ShipToCity>New York</ShipToCity>
                <ShipToCountry>USA</ShipToCountry>
                <ShipToStateOrProvince>New York</ShipToStateOrProvince>
                <ShipToStreet>PA112</ShipToStreet>
                <ShipToZipOrPostalCode>1001</ShipToZipOrPostalCode>
                <SupplierPartNumber>SPN1211</SupplierPartNumber>
                <UOM>Individual Unit</UOM>
            </InvoiceLine>
            <InvoiceLine>
                <ExternalInvoiceNumber>EXT-INV-008</ExternalInvoiceNumber>
                <LineDescription>Apple macbook 15 Pro</LineDescription>
                <PurchaseOrderLine>#ABC00048896981</PurchaseOrderLine>
                <POLineDescription>NowX Laptop</POLineDescription>
                <LineQuantity>10</LineQuantity>
                <LineUnitPrice>10.00</LineUnitPrice>
                <Subtotal>100.00</Subtotal>
                <LineAmountInvoiced>100</LineAmountInvoiced>
                <Currency>USD</Currency>
                <CostCenter>ACN00001</CostCenter>
                <GLAccount>100002</GLAccount>
                <TaxCode>A0 Sales Tax</TaxCode>
                <ShipToCity>New York</ShipToCity>
                <ShipToCountry>USA</ShipToCountry>
                <ShipToStateOrProvince>New York</ShipToStateOrProvince>
                <ShipToStreet>PA112</ShipToStreet>
                <ShipToZipOrPostalCode>1001</ShipToZipOrPostalCode>
                <SupplierPartNumber>SPN1211</SupplierPartNumber>
                <UOM>Individual Unit</UOM>
            </InvoiceLine>
        </InvoiceLines>
    </Invoice>
    <Invoice>
        <InvoiceType></InvoiceType>
        <SupplierInvoiceNumber>LineLevelTaxes</SupplierInvoiceNumber>
        <ExternalInvoiceNumber>EXT-INV-#0010</ExternalInvoiceNumber>
        <Supplier>3245545</Supplier>
        <PurchaseOrder></PurchaseOrder>
        <BusinessOwner>Paula Smith</BusinessOwner>
        <DateFormat>MMM DD, YYYY</DateFormat>
        <InvoiceDate>Aug 3, 2024</InvoiceDate>
        <PaymentTerms>Net 60</PaymentTerms>
        <LegalEntity>US</LegalEntity>
        <Subtotal>100</Subtotal>
        <ShippingAmount>10</ShippingAmount>
        <OtherCharges>10</OtherCharges>
        <Discounts>10</Discounts>
        <AmountInvoiced>10</AmountInvoiced>
        <Currency>USD</Currency>
        <InvoiceLineCount>1</InvoiceLineCount>
        <ShipToCity>Los Angeles</ShipToCity>
        <ShipToCountry>USA</ShipToCountry>
        <ShipToStateOrProvince>CA</ShipToStateOrProvince>
        <ShipToStreet>456 Oak Ave</ShipToStreet>
        <ShipToZipOrPostalCode>90001</ShipToZipOrPostalCode>
        <ShipFromCity>Addison</ShipFromCity>
        <ShipFromCountry>USA</ShipFromCountry>
        <ShipFromStateOrProvince>TX</ShipFromStateOrProvince>
        <ShipFromStreet>15725 Dallas P</ShipFromStreet>
        <ShipFromZipOrPostalCode>55555</ShipFromZipOrPostalCode>
        <RemitAddress>47 W 11th St</RemitAddress>
        <RemitToCity>New York</RemitToCity>
        <RemitToCountry>USA</RemitToCountry>
        <RemitToStateOrProvince>NY</RemitToStateOrProvince>
        <RemitToZipOrPostalCode>99999</RemitToZipOrPostalCode>
        <BillToStreet>4810 Eastgate Mall</BillToStreet>
        <BillToCity>San Diego</BillToCity>
        <BillToCountry>USA</BillToCountry>
        <BillToStateOrProvince>CA</BillToStateOrProvince>
        <BillToZipOrPostalCode>92121$%ad</BillToZipOrPostalCode>
        <SupplierTaxID>7894328742</SupplierTaxID>
        <InvoiceLines>
            <InvoiceLine>
                <ExternalInvoiceNumber>EXT-INV-008</ExternalInvoiceNumber>
                <LineDescription>Apple macbook 15 Pro</LineDescription>
                <PurchaseOrderLine></PurchaseOrderLine>
                <POLineDescription>NowX Laptop</POLineDescription>
                <LineQuantity>10</LineQuantity>
                <LineUnitPrice>20</LineUnitPrice>
                <Subtotal>-200¥</Subtotal>
                <LineAmountInvoiced>200$</LineAmountInvoiced>
                <Currency>USD</Currency>
                <CostCenter>ACN00005</CostCenter>
                <GLAccount>141300</GLAccount>
                <TaxCode>A0 Sales Tax</TaxCode>
                <ShipToCity>New York</ShipToCity>
                <ShipToCountry>USA</ShipToCountry>
                <ShipToStateOrProvince>New York</ShipToStateOrProvince>
                <ShipToStreet>PA112</ShipToStreet>
                <ShipToZipOrPostalCode>1001ACD@</ShipToZipOrPostalCode>
                <SupplierPartNumber>SPN1211</SupplierPartNumber>
                <UOM>Individual Unit</UOM>
                <TaxDetails>
                    <TaxDetail>
                        <TaxType>SGST</TaxType>
                        <TaxAmount>12</TaxAmount>
                        <TaxRate></TaxRate>
                    </TaxDetail>
                    <TaxDetail>
                        <TaxType>CGST</TaxType>
                        <TaxAmount></TaxAmount>
                        <TaxRate>15</TaxRate>
                    </TaxDetail>
                    <TaxDetail>
                        <TaxType>Withholding tax</TaxType>
                        <TaxAmount>13</TaxAmount>
                        <TaxRate>13</TaxRate>
                    </TaxDetail>
                </TaxDetails>
            </InvoiceLine>
        </InvoiceLines>
    </Invoice>
    <Invoice>
        <InvoiceType></InvoiceType>
        <SupplierInvoiceNumber>LineLevelTaxes</SupplierInvoiceNumber>
        <ExternalInvoiceNumber>EXT-INV-#0010</ExternalInvoiceNumber>
        <Supplier>3245545</Supplier>
        <PurchaseOrder></PurchaseOrder>
        <BusinessOwner>Paula Smith</BusinessOwner>
        <DateFormat>MMMM DD, YYYY</DateFormat>
        <InvoiceDate>september 1st, 2024</InvoiceDate>
        <PaymentTerms>Net 60</PaymentTerms>
        <LegalEntity>US</LegalEntity>
        <Subtotal>100</Subtotal>
        <ShippingAmount>10</ShippingAmount>
        <OtherCharges>10</OtherCharges>
        <Discounts>10</Discounts>
        <AmountInvoiced>10</AmountInvoiced>
        <Currency>USD</Currency>
        <InvoiceLineCount>1</InvoiceLineCount>
        <ShipToCity>Los Angeles</ShipToCity>
        <ShipToCountry>USA</ShipToCountry>
        <ShipToStateOrProvince>CA</ShipToStateOrProvince>
        <ShipToStreet>456 Oak Ave</ShipToStreet>
        <ShipToZipOrPostalCode>90001</ShipToZipOrPostalCode>
        <ShipFromCity>Addison</ShipFromCity>
        <ShipFromCountry>USA</ShipFromCountry>
        <ShipFromStateOrProvince>TX</ShipFromStateOrProvince>
        <ShipFromStreet>15725 Dallas P</ShipFromStreet>
        <ShipFromZipOrPostalCode>55555</ShipFromZipOrPostalCode>
        <RemitAddress>47 W 11th St</RemitAddress>
        <RemitToCity>New York</RemitToCity>
        <RemitToCountry>USA</RemitToCountry>
        <RemitToStateOrProvince>NY</RemitToStateOrProvince>
        <RemitToZipOrPostalCode>99999</RemitToZipOrPostalCode>
        <BillToStreet>4810 Eastgate Mall</BillToStreet>
        <BillToCity>San Diego</BillToCity>
        <BillToCountry>USA</BillToCountry>
        <BillToStateOrProvince>CA</BillToStateOrProvince>
        <BillToZipOrPostalCode>92121$%ad</BillToZipOrPostalCode>
        <SupplierTaxID>7894328742</SupplierTaxID>
        <InvoiceLines>
            <InvoiceLine>
                <ExternalInvoiceNumber>EXT-INV-008</ExternalInvoiceNumber>
                <LineDescription>Apple macbook 15 Pro</LineDescription>
                <PurchaseOrderLine></PurchaseOrderLine>
                <POLineDescription>NowX Laptop</POLineDescription>
                <LineQuantity>10</LineQuantity>
                <LineUnitPrice>20</LineUnitPrice>
                <Subtotal>-200¥</Subtotal>
                <LineAmountInvoiced>200$</LineAmountInvoiced>
                <Currency>USD</Currency>
                <CostCenter>ACN00005</CostCenter>
                <GLAccount>141300</GLAccount>
                <TaxCode>A0 Sales Tax</TaxCode>
                <ShipToCity>New York</ShipToCity>
                <ShipToCountry>USA</ShipToCountry>
                <ShipToStateOrProvince>New York</ShipToStateOrProvince>
                <ShipToStreet>PA112</ShipToStreet>
                <ShipToZipOrPostalCode>1001ACD@</ShipToZipOrPostalCode>
                <SupplierPartNumber>SPN1211</SupplierPartNumber>
                <UOM>Individual Unit</UOM>
                <TaxDetails>
                    <TaxDetail>
                        <TaxType>SGST</TaxType>
                        <TaxAmount>12</TaxAmount>
                        <TaxRate></TaxRate>
                    </TaxDetail>
                    <TaxDetail>
                        <TaxType>CGST</TaxType>
                        <TaxAmount></TaxAmount>
                        <TaxRate>15</TaxRate>
                    </TaxDetail>
                    <TaxDetail>
                        <TaxType>Withholding tax</TaxType>
                        <TaxAmount>13</TaxAmount>
                        <TaxRate>13</TaxRate>
                    </TaxDetail>
                </TaxDetails>
            </InvoiceLine>
        </InvoiceLines>
    </Invoice>
    <TargetERP>ERP1</TargetERP>
</Invoices>'

```

The following result shows that the request is successful and the invoice data is processing. You can view the status of the request in the Invoice integration log \[sn\_spend\_intg\_invoice\_integration\_log\] table. Use the batch ID listed in the Batch ID column to find the invoice.

```
{
    "batchId": "APIINV1736249646168148",
    "status": "Success",
    "message": "Your request has been successfully received and is being processed."
}
```

