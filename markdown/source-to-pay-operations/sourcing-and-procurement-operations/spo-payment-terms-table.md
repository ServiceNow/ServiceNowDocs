---
title: Payment Terms \[sn\_shop\_payment\_term\] table
description: The Payment Terms \[sn\_shop\_payment\_term\] table stores payment term information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/spo-payment-terms-table.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-07-13"
reading_time_minutes: 2
breadcrumb: [Primary data tables, Reference, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Payment Terms \[sn\_shop\_payment\_term\] table

The Payment Terms \[sn\_shop\_payment\_term\] table stores payment term information.

This table contains the following fields.

|Field|Data type|Description|
|-----|---------|-----------|
|Payment term|String|Name or code of the payment term.|
|Short description|String|Short explanation of the payment term.|
|Type|Choice|Type of payment term. The options are Due upon receipt, Fixed, or Net.|
|Discount percentage|Decimal|Percentage of discount applied on the total invoice amount.|
|Active|Boolean|Indicates whether the payment term is active.|
|Payment due by|Choice|When the payment is due. The options are End of the year or End of the month.|
|Discount days|Integer|Number of days from the invoice generation date until the discount applies.|
|Net days to pay|Integer|Total number of days within which the payment must be made.|

**Parent Topic:**[Primary data tables for Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/spo-primary-data-tables.md)

**Related topics**  


[Fixed Asset \[sn\_fin\_fixed\_asset\] table]()

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

[Price Break \[sn\_shop\_price\_break\] table]()

[Pricing \[sn\_shop\_m2m\_product\_contract\] table]()

[Product group \[sn\_shop\_product\_group\] table]()

[Product Visuals \[sn\_shop\_supplier\_product\_artifact\] table]()

[Shipping methods \[sn\_shop\_shipping\_method\] table]()

