---
title: SupplyOn inbound confirmation field mapping
description: This reference describes how SupplyOn demand-response confirmations map to the inbound confirmation staging tables, including the ResponseResult code map and sample payloads.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/source-to-pay-operations/supplyon-inbound-confirmation-mapping.html
release: australia
topic_type: reference
last_updated: "2026-10-09"
reading_time_minutes: 2
breadcrumb: [Reference, Purchase Order Management integration with SupplyOn, Integrate with Purchase Order Management, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# SupplyOn inbound confirmation field mapping

This reference describes how SupplyOn demand-response confirmations map to the inbound confirmation staging tables, including the ResponseResult code map and sample payloads.

The SupplyOn model is line-item, with no confirmation header. The integration synthesizes one confirmation header per purchase order \(\[sn\_fcms\_intg\_imp\_po\_confirmation\]\) and writes one confirmation line per position schedule line \(\[sn\_fcms\_intg\_imp\_po\_confirmation\_line\]\). The cross-reference keys are the purchase order number \(header\) and the position ID \(line\). Both staging tables extend `sys_import_set_row`, so every column is prefixed with `u_` and stored as a string. The transform into the core tables casts them to their semantic types.

## Confirmation header staging mapping

|ServiceNow field|Staging column|SupplyOn property|Notes|
|----------------|--------------|-----------------|-----|
|Purchase order|u\_purchase\_order|DemandResponse.OrderNumber|ServiceNow PO number. Header cross-reference key.|
|Additional comments|u\_additional\_comments|Positions\[\].ResponseBy|Responder email. Optional.|
|Confirmation source|u\_confirmation\_source|Constant "Integration"|Fixed.|
|ERP source|u\_erp\_source|Constant "SupplyOn"|Fixed.|
|Status|u\_status|Constant "submitted"|Submitted when sent by SupplyOn.|
|Active|u\_active|Constant \(active\)|Fixed.|
|ERP number, ERP PO number|u\_erp\_number, u\_erp\_po\_number|Not populated|External confirmation number. Not populated for SupplyOn.|
|Number|u\_number|Auto-generated in base table|Left empty in staging.|

**Note:** GenericHeaderData.MessageDate is the intended source for an ERP-created-date header field. That column is a planned addition and is not yet present on the staging table.

## Confirmation line staging mapping

|ServiceNow field|Staging column|SupplyOn property|Notes|
|----------------|--------------|-----------------|-----|
|Purchase order line|u\_purchase\_order\_line|Positions\[\].PosId|Line cross-reference key.|
|Confirmation status|u\_confirmation\_status|Positions\[\].ResponseResult|Choice. Mapped to the ServiceNow choice \(see the code map\).|
|Confirmed unit price|u\_confirmed\_unit\_price|Positions\[\].PricePerUnit|Decimal.|
|Confirmed supplier part number|u\_confirmed\_supplier\_part\_number|Positions\[\].SupplierPartNumber|Populated only if SupplyOn config lets the supplier enter it.|
|Confirmed delivery date|u\_confirmed\_delivery\_date|Positions\[\].ScheduleLines\[\].Date|If empty \(for example, declined\), reconstructed from the PO line.|
|Quantity|u\_quantity|Positions\[\].ScheduleLines\[\].Quantity|If empty \(for example, declined\), reconstructed from the PO line.|
|Additional comments|u\_additional\_comments|Positions\[\].Comment| |
|Sequence number|u\_sequence\_number|Derived|Schedule lines ordered chronologically by confirmed date.|
|Unit|u\_unit|From the PO line|Supplier cannot change the unit of measure.|
|Currency|u\_currency|From the PO line|Supplier cannot change the currency.|
|Confirmed amount|u\_confirmed\_amount|Not sent \(price times quantity\)|Amount not returned by SupplyOn.|
|ERP number, ERP PO line number|u\_erp\_number, u\_erp\_po\_line\_number|Not populated|Cross-referenced in the base table.|
|ERP source|u\_erp\_source|Constant "SupplyOn"|Fixed.|
|Purchase order confirmation|u\_purchase\_order\_confirmation|Not applicable|Open item: whether this link field is needed in staging.|
|Number|u\_number|Auto-generated in base table|Left empty in staging.|

## ResponseResult mapping

|SupplyOn code|ServiceNow confirmation status|
|-------------|------------------------------|
|4 \(No action\)|No action|
|5 \(Confirmed as-is\)|Confirmed|
|7 \(Declined\)|Rejected|
|6, 84, 111, 112, 113 \(changed, price, date, quantity, surcharge, or rebate\)|Changes requested|

**Note:** Confirmation writes stop at staging \(\[sn\_fcms\_intg\_imp\_po\_confirmation\] and \[sn\_fcms\_intg\_imp\_po\_confirmation\_line\]\). The transform into the core `sn_poem_po_confirmation` and `_line` tables is a customer or framework concern and is not part of this application.

## Query and sample payloads

Summaries are queried by response-date window and demand type. The range must be 100 days or less.

```
GET /scc/demandresponse/v1/demandresponse-summaries
    ?lastResponseDateFrom=2026-06-01T00:00:00Z
    &lastResponseDateTo=2026-06-30T00:00:00Z
    &demandType=ORDER

# then, per returned order:
GET /scc/demandresponse/v1/demandresponse
    ?demandType=ORDER&orderNumber=pha2026062c
    &orgCode=SENOW&plantCode=SNPOC01&supplierNumber=656546
```

Sample response \(summaries\):

```
[
  {
    "lastResponseDate": "2026-06-18T12:13:17.127Z",
    "orderNumber": "pha2026062c",
    "routingTriple": { "OrgCode": "SENOW", "PlantCode": "SNPOC01", "SupplierNumber": "656546" }
  }
]
```

Sample response \(detail\):

```
{
  "OrderNumber": "pha2026062c",
  "Type": "320",
  "Positions": [
    {
      "PosId": "000020",
      "ResponseResult": "5",
      "ResponseBy": "responder@example.com",
      "ResponseDate": "2026-06-18T12:13:17.127Z",
      "SupplierPartNumber": "SB 20260218",
      "PricePerUnit": 10,
      "ScheduleLines": [{ "Date": "2026-06-30T22:00:00Z", "Quantity": 10, "Type": "1" }]
    }
  ]
}
```

