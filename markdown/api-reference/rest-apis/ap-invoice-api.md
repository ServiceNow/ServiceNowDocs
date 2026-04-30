---
title: AP Invoice API
description: Allows external systems, such as those used by vendors, to securely submit invoices directly into an accounts payable system in a structured and automated manner.Processes an automated invoice in commerce XML \(cXML\) format.Processes an automated invoice in JSON format.
locale: en-US
release: xanadu
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2024-10-08"
reading_time_minutes: 24
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# AP Invoice API

Allows external systems, such as those used by vendors, to securely submit invoices directly into an accounts payable system in a structured and automated manner.

This API requires the Accounts Payable Invoice Processing \(com.sn\_ap\_apm\) store application, which is provided within the `sn_spend_intg` namespace. For information, see [Accounts Payable Invoice Processing](https://www.servicenow.com/docs/access?context=acc-pay-invoice-processing&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US).

Refer to [AP Invoice API Developer Guide](../../guides/APInvoiceAPI/concept/apInvoice-dev-guide.md#) for help with the following tasks:

-   Define a custom field for invoices, invoice lines, and invoice tax lines.
-   Map the custom field between source and target tables.
-   Map the custom field to a payload entry in a specific format, such as JSON or cXML.
-   Setting credentials for authentication when using cXML as the payload.

**Note:** The maximum default payload size is 100 records. This value is configurable in the **sn\_spend\_intg.ap.invoice.create.api.record\_limit** system property.

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

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

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

-   [ERP source](https://www.servicenow.com/docs/access?context=erp-source&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)
-   [Ledger account](https://www.servicenow.com/docs/access?context=ledger-account&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)

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

Contains error details when the request fails.Possible errors:

-   400 status code. Invalid payload - Invalid content type.
-   400 status code. Invalid payload - Error: Invalid payload structure.
-   400 status code when the number of records in the batch is more than the batch size set. Invalid payload - Error: Payload exceeds allowed invoices limit in a batch.
-   400 status code if the number of records in the batch is zero. Invalid payload - Error: Empty invoices. No data to process.
-   429 status code. Rate limit of 500 requests per hour for APO Invoice Ingestion exceeded.

Data type: String

</td></tr><tr><td>

message

</td><td>

A message providing additional context about the request's processing status.Possible details:

-   202 status code. Your request has been successfully received and is being processed.
-   429 status code. Rate limit exceeded.

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

The following results display if the request is successful and the invoice data is processing. You can view the status of the request in the Invoice integration log \[sn\_spend\_intg\_invoice\_integration\_log\] table. Use the batch ID to find the invoice.

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

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

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
    "business_owner": "String",
    "currency": "String",
    "discounts": "String",
    "erp_number": "String",
    "external_invoice_number": "String",
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
    "supplier_tax_id": "String"
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

Unique number generated within the ERP \(Enterprise Resource Planning\) system for the purchase order. For information, see [Purchase order integration](https://www.servicenow.com/docs/access?context=purchase-order-integration-2&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US).Target field: u\_erp\_number

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

List of objects that define the lines that are being invoiced for purchases within this order. Invoice lines are staged in the Invoice line import inbound \[sn\_spend\_intg\_imp\_invoice\_line\] table.Data type: Array

```
"invoice_lines": [
  {
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

-   [ERP source](https://www.servicenow.com/docs/access?context=erp-source&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)
-   [Ledger account](https://www.servicenow.com/docs/access?context=ledger-account&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)

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

ERP record in which the invoice is posted. Located in the ERP Source \[sn\_fin\_erp\_source\] table. See [ERP source](https://www.servicenow.com/docs/access?context=erp-source&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US).Data type: String

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

Contains error details when the request fails.Possible errors:

-   400 status code. Invalid payload - Invalid content type.
-   400 status code. Invalid payload - Error: Invalid payload structure.
-   400 status code when the number of records in the batch is more than the batch size set. Invalid payload - Error: Payload exceeds allowed invoices limit in a batch.
-   400 status code if the number of records in the batch is zero. Invalid payload - Error: Empty invoices. No data to process.
-   429 status code. Rate limit of 500 requests per hour for APO Invoice Ingestion exceeded.

Data type: String

</td></tr><tr><td>

message

</td><td>

A message providing additional context about the request's processing status.Possible details:

-   202 status code. Your request has been successfully received and is being processed.
-   429 status code. Rate limit exceeded.

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

The following example shows how to process an invoice provided as a request in JSON format.

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
            "invoice_type": "non_po_invoice",
            "supplier_invoice_number": "SPOTLIGHT98",
            "external_invoice_number": "SPOTLIGHT98",
            "erp_number": "RTest12345",
            "purchase_order": "R0030R16537",
            "business_owner": "paula.smith@example.com",
            "supplier": "3245545",
            "original_invoice": "SIN188191",
            "invoice_date": "2023-08-15",
            "payment_terms": "Net 30",
            "legal_entity": "1000",
            "subtotal": "100.00",
            "shipping_amount": "50.00",
            "other_charges": "20.00",
            "discounts": "100.00",
            "amount_invoiced": "150.00",
            "currency": "USD",
            "invoice_line_count": "2",
            "ship_to_city": "",
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
                    "tax_type": "Central Goods and Services Tax",
                    "tax_amount": "25",
                    "tax_rate": ""
                },
                {
                    "tax_type": "Sales tax",
                    "tax_amount": "10",
                    "tax_rate": "10"
                },
                {
                    "tax_type": "IGST",
                    "tax_amount": "",
                    "tax_rate": "15"
                },
                {
                    "tax_type": "State Goods and Service Tax",
                    "tax_amount": "20",
                    "tax_rate": "10"
                }
            ],
            "invoice_lines": [
                {
                    "external_invoice_number": "SPOTLIGHT98",
                    "line_description": "Laptop",
                    "line_quantity": "5",
                    "line_unit_price": "20.00",
                    "subtotal": "100.00",
                    "line_amount_invoiced": "100.00",
                    "purchase_order_line": "232432",
                    "po_line_description": "Mac laptop",
                    "currency": "USD",
                    "cost_center": "41605600",
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
                            "tax_type": "Central Goods and Services Tax",
                            "tax_amount": "25",
                            "tax_rate": ""
                        },
                        {
                            "tax_type": "Sales tax",
                            "tax_amount": "",
                            "tax_rate": "10"
                        }
                    ]
                },
                {
                    "external_invoice_number": "SPOTLIGHT98",
                    "line_description": "Charger",
                    "line_quantity": "5",
                    "line_unit_price": "40.00",
                    "subtotal": "200.00",
                    "line_amount_invoiced": "200.00",
                    "purchase_order_line": "232432",
                    "po_line_description": "Mac laptop",
                    "currency": "USD",
                    "cost_center": "41605600",
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
                            "tax_type": "Central Goods and Services Tax",
                            "tax_amount": "25",
                            "tax_rate": ""
                        },
                        {
                            "tax_type": "Sales tax",
                            "tax_amount": "",
                            "tax_rate": "10"
                        }
                    ]
                }
            ]
        }
    ],
    "target_erp": ""
}'
```

The following results display if the request is successful and the invoice data is processing. You can view the status of the request in the Invoice integration log \[sn\_spend\_intg\_invoice\_integration\_log\] table. Use the batch ID to find the invoice.

```
{
    "batchId": "APIINV1729711710733280",
    "status": "Success",
    "message": "Your request has been successfully received and is being processed."
}
```

