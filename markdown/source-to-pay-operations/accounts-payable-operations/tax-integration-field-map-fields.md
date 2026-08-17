---
title: Tax integration field map fields
description: Field descriptions for the Tax integration field mappings \[sn\_spend\_intg\_tax\_field\_map\] table, which defines the outbound and inbound mappings that transform invoice data between APO and a tax engine.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/tax-integration-field-map-fields.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2026-07-29"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, tax field mapping, sn\_spend\_intg\_tax\_field\_map, Vertex, tax integration]
breadcrumb: [Tax lines, Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Tax integration field map fields

Field descriptions for the Tax integration field mappings \[sn\_spend\_intg\_tax\_field\_map\] table, which defines the outbound and inbound mappings that transform invoice data between APO and a tax engine.

## Tax integration field map fields

The Tax integration field mappings \[sn\_spend\_intg\_tax\_field\_map\] table drives the transformation of invoice data between APO and the tax engine. Mappings are maintained as configuration rather than script. The following table describes the fields.

|Field|Description|
|-----|-----------|
|Type|Direction of the mapping. Set to **outbound** for the request that is sent from APO to the tax engine, or **inbound** for the response that is returned from the tax engine.|
|Transaction type|Transaction type that the mapping applies to, such as invoice tax verification.|
|Source table|Table that the source data is read from.|
|Source field|Field that the value is read from on the source table.|
|Target field|Field that the value is written to in the target payload.|
|Target entity|Entity in the target payload that the target field belongs to.|
|Target tax engine|Tax engine that the mapping applies to, such as Vertex.|
|Mapping type|Vertex's tax response is converted back as JSON format into internal staging record.|
|Version|Version of the mapping set.|
|Order|Order in which the mapping is applied.|
|Active|Status of the mapping. The transformation uses active mappings only and excludes inactive mappings and mappings for a different tax engine.|

**Parent Topic:**[Tax lines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-tax-lines-apo.md)

