---
title: Fixed Asset \[sn\_fin\_fixed\_asset\] table
description: The Fixed Asset \[sn\_fin\_fixed\_asset\] table stores information related to: Fixed assets purchased from suppliers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/fin-fixed-asset-table.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-07-13"
reading_time_minutes: 2
breadcrumb: [Primary data tables, Reference, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Fixed Asset \[sn\_fin\_fixed\_asset\] table

The Fixed Asset \[sn\_fin\_fixed\_asset\] table stores information related to: Fixed assets purchased from suppliers.

This table contains the following fields.

|Field|Data type|Description|
|-----|---------|-----------|
|Number|String|System-generated value that uniquely identifies this fixed asset.|
|ERP asset number|String|Value generated within an ERP system to uniquely identify this fixed asset.|
|Display name|String|System-generated name that uniquely identifies this fixed asset.|
|Status|Choice|Status of the fixed asset. The options are Submitted, Success, or Pending Deletion.|
|Supplier|Reference|Supplier from whom this fixed asset was purchased.|
|Product name|String|Product that was purchased.|
|Capitalize on|Date|Date on which the fixed asset was created within the ERP system.|
|Original value|Currency|Amount originally paid for the fixed asset.|
|Depreciation lifecycle|String|Length of time in which the fixed asset is fully depreciated.|
|Depreciation term|String|Frequency of depreciation throughout the lifecycle of the fixed asset.|
|Remaining value|Currency|Amount that the fixed asset is worth today after depreciation.|
|Depreciated amount|Currency|Amount that the fixed asset has depreciated over time.|
|Salvage value|Currency|Amount that the fixed asset is worth after it reaches the end of its useful life.|
|ERP Source|Reference|ERP source system associated with the fixed asset.|

**Parent Topic:**[Primary data tables for Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/spo-primary-data-tables.md)

**Related topics**  


[Finance Exchange Rates \[sn\_fin\_fx\_rate\] table]()

[Ledger Account table]()

[GL rule \[sn\_fin\_gl\_rule\] table]()

[Threshold rule \[sn\_fin\_gl\_threshold\_rule\] table]()

[Industry \[sn\_fin\_industry\] table]()

[Ledger \[sn\_fin\_ledger\] table]()

[Legal Entity \[sn\_fin\_legal\_entity\] table]()

[Office Location table]()

[Organization \[sn\_fin\_organization\] table]()

[Approval Group \[sn\_shop\_approval\_group\] table]()

[Approval Rule \[sn\_shop\_approval\_rule\] table]()

[Approval Rule Composition table]()

[Attribute \[sn\_shop\_attribute\] table]()

[Attribute Set \[sn\_shop\_attribute\_set\] table]()

[Attribute Type \[sn\_shop\_attribute\_type\] table]()

[Delivery Location \[sn\_shop\_delivery\_location\] table]()

[Job Code \[sn\_shop\_job\_code\] table]()

[Payment Terms \[sn\_shop\_payment\_term\] table]()

[Price Break \[sn\_shop\_price\_break\] table]()

[Pricing \[sn\_shop\_m2m\_product\_contract\] table]()

[Product group \[sn\_shop\_product\_group\] table]()

[Product Visuals \[sn\_shop\_supplier\_product\_artifact\] table]()

[Shipping methods \[sn\_shop\_shipping\_method\] table]()

