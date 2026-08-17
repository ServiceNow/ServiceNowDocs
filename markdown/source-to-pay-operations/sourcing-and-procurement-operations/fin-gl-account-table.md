---
title: Ledger Account table
description: The Ledger Account \[sn\_fin\_gl\_account\] table stores information related to: General ledger accounts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/fin-gl-account-table.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-07-13"
reading_time_minutes: 3
breadcrumb: [Primary data tables, Reference, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Ledger Account table

The Ledger Account \[sn\_fin\_gl\_account\] table stores information related to: General ledger accounts.

## Ledger Account \[sn\_fin\_gl\_account\] table

The Ledger Account \[sn\_fin\_gl\_account\] table contains the following fields.

|Field|Data type|Description|
|-----|---------|-----------|
|Account name|String|Display name of the ledger account fetched from the ERP system.|
|Number|String|System-generated number that uniquely identifies this ledger account.|
|Entity|Reference|Legal entity associated with the ledger account.|
|Ledger account|String|Ledger account code.|
|Short description|String|Short description of the ledger account.|
|Type|String|Type of the ledger account.|
|ERP source|Reference|ERP source system associated with the ledger account.|
|Ledger type|String|Type of ledger to which the account belongs.|
|Category|Choice|Category of the ledger account. The options are Cash, Revenue, Investment, or Cash and Cash Equivalent.|
|Inactive|Boolean|Inactive status of the ledger account.|
|Account currency|Reference|Currency of the ledger account.|
|Local currency|Reference|Local currency of the ledger account.|
|Reporting currency|Reference|Reporting currency of the ledger account.|
|Alternate currency|Reference|Alternate currency of the ledger account.|
|Open item management|Boolean|Indicates whether open item management is enabled for the account.|
|Sub-ledger account|String|Sub-ledger account code.|
|Key account|Boolean|Indicates whether this is a key account.|
|Zero balance account|Boolean|Indicates whether this is a zero balance account.|
|Risk rating|Choice|Risk rating of the ledger account. The options are High, Medium, or Low.|
|Description|String|Detailed description of the ledger account.|

**Parent Topic:**[Primary data tables for Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/spo-primary-data-tables.md)

**Related topics**  


[Fixed Asset \[sn\_fin\_fixed\_asset\] table]()

[Finance Exchange Rates \[sn\_fin\_fx\_rate\] table]()

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

