---
title: SupplyOn outbound purchase order request mapping
description: ServiceNow outbound purchase order header and line fields map to the SupplyOn POST /purchaseorder payload. This topic includes a sample request and response.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/source-to-pay-operations/supplyon-outbound-request-mapping.html
release: australia
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 2
breadcrumb: [Reference, Purchase Order Management integration with SupplyOn, Integrate with Purchase Order Management, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# SupplyOn outbound purchase order request mapping

ServiceNow outbound purchase order header and line fields map to the SupplyOn POST /purchaseorder payload. This topic includes a sample request and response.

The send subflow maps `sn_spend_intg_outbound_purchase_order` and its lines \(and the source purchase order for attachments\) to the SupplyOn `POST /purchaseorder` payload.

## Header field mapping

|ServiceNow field|Type|SupplyOn property|Notes|
|----------------|----|-----------------|-----|
|order\_number|String|PurchaseOrderHeader.OrderNumber, GenericInboundData.DocumentNumber|Required.|
|order\_date|Date|PurchaseOrderHeader.OrderDate|Date only, sent as ...T00:00:00Z \(ISO 8601 UTC\).|
|currency|String|PurchaseOrderHeader.Currency, NetValueCurrency| |
|Constant "9"|String|PurchaseOrderHeader.FunctionCode|Always 9. SupplyOn decides insert versus update. No code 4 or 5.|
|Sum of line net values|Decimal|PurchaseOrderHeader.NetValue|Computed at send. Omitted when there are no lines.|
|payment\_term|String|PurchaseOrderHeader.FlexibleLongText\[Code=AAB\]|Omitted when blank.|
|header\_note \(property\)|String|PurchaseOrderHeader.FlexibleLongText\[Code=AAI\]|Customer-visible. Omitted when blank.|
|order\_type \(property, NB\)|String|PurchaseOrderHeader.OrderType|Standard orders.|
|supplier\_name|String|Address\[SU\].Name1|Supplier address.|
|supplier\_id \(sn\_fin\_supplier.number\)|String|Address\[SU\].PartnerNumber, RoutingTriple.SupplierNumber|ServiceNow supplier number \(SUP...\), not the sys\_id and not erp\_company\_code.|
|Supplier contacts|String|Address\[SU\].Contacts\[\].Email/Name/Phone|All supplier contacts.|
|Supplier address|String|Address\[SU\].Street/City/ZIP/Country|Headquarters location. Falls back to the sn\_fin\_supplier organization address when no headquarters location exists.|
|purchasing\_org|String|Address\[BY\].Contacts\[\].Department|Buyer address. Contacts omitted when blank.|
|Routing triple|String|RoutingTriple.OrgCode|org\_code\_override or plus company code.|
|Routing triple|String|RoutingTriple.PlantCode|plant\_code property or plus company code.|
|edi\_sender \(property\)|String|GenericHeaderData.EDISender|Default SERVICENOW.|
|Constant|String|GenericHeaderData.EDIReceiver = SUPPLYON, GenericInboundData.EDIMessageCode = 220|Fixed.|

## Line field mapping

The integration sends one PurchaseOrderPosition per line.

|ServiceNow field|Type|SupplyOn property|Notes|
|----------------|----|-----------------|-----|
|Index times 10|Derived|Position.PosID|10, 20, 30, and so on.|
|sku|String|Position.Material.SupplierPartNumber| |
|product\_name|String|Position.Material.CustomerPartDescription| |
|mpn|String|Position.ManufacturerArticleNumber| |
|unit|String|Position.CustomerPartUoM, Delivery.UoM, PriceUnitUoM| |
|purchased\_quantity|Decimal|Position.Quantity, Delivery.Quantity| |
|expected\_del\_date|Date|Position.Delivery\[\].DeliveryDate \(Type=1, firm\)|ISO 8601 UTC.|
|unit\_price|Decimal|Position.PricePerUnit|PriceUnit defaults to 1.|
|unit\_price\_currency|String|Position.PricePerUnitCurrency, NetValueCurrency| |
|unit\_price times quantity|Decimal|Position.NetValue|Computed.|
|Ship-to address fields|String|Position.Addresses\[CN\] \(per line\)|Country as ISO 3166-1 alpha-2.|
|Constant|Boolean|Position.ToBeConfirmed = true|Supplier must confirm.|

**Important:** Service lines \(**product\_type** 20\) and handling-fee lines \(30\) are excluded from the payload. Lines with an empty product type are kept.

## Attachments

Attachments are header-level only, because SupplyOn has no per-line attachment field. They are embedded as Base64 in the top-level Attachments list on create and update \(cancel carries none\). Before send, the integration enforces these limits: 10 files or fewer, 5 MB per file or less, 15 MB total or less, and allowed types only. A violation throws `SUPPLYON_ATTACHMENT_VIOLATION` and aborts before the REST call. Attachments live on the source purchase order and are resolved by order number. Line-level attachments aren't sent.

## Sample request payload

```
{
  "GenericHeaderData": {
    "EDISender": "SERVICENOW",
    "EDIReceiver": "SUPPLYON",
    "MessageDate": "2025-09-11T11:50:00Z",
    "RoutingTriple": { "OrgCode": "SENOW", "PlantCode": "SNPOC01", "SupplierNumber": "656546" }
  },
  "GenericInboundData": {
    "EDIMessageCode": "220",
    "DocumentNumber": "pha2026062c",
    "MessageNumber": "0000200003",
    "ERPSystemID": ""
  },
  "PurchaseOrderHeader": {
    "OrderNumber": "pha2026062c",
    "OrderDate": "2025-09-10T00:00:00Z",
    "Currency": "EUR",
    "FunctionCode": "9",
    "OrderType": "NB",
    "NetValue": 100,
    "NetValueCurrency": "EUR",
    "FlexibleLongText": [{ "Code": "AAB", "Text": "Net 30" }]
  },
  "Address": [
    { "AddressCode": "SU", "Name1": "Demo Seller GmbH", "PartnerNumber": "656546" },
    { "AddressCode": "BY", "Contacts": [{ "Department": "Purchasing Organization" }] },
    { "AddressCode": "CN", "Name1": "Plant 2", "Street": "Burgweg 341", "City": "Hamburg", "ZIP": "20095", "Country": "DE" }
  ],
  "PurchaseOrderPosition": [
    {
      "PosID": "10",
      "Material": { "SupplierPartNumber": "SB 20260218", "CustomerPartDescription": "Widget" },
      "CustomerPartUoM": "PCE",
      "Quantity": 10,
      "Delivery": [{ "Type": "1", "DeliveryDate": "2026-08-01T00:00:00Z", "Quantity": 10, "UoM": "PCE" }],
      "PricePerUnit": 10,
      "PricePerUnitCurrency": "EUR",
      "NetValue": 100,
      "ToBeConfirmed": true
    }
  ]
}
```

## Sample synchronous response \(HTTP 201\)

The synchronous response confirms transport receipt only. The business outcome arrives through the async status callback.

```
{
  "TransactionID": "2491C8AF4F962D2CCB87CC102AFCXXXX",
  "StatusCode": "OK",
  "StatusText": "Message received"
}
```

