---
title: Threshold rule \[sn\_fin\_gl\_threshold\_rule\] table
description: The Threshold Rule \[sn\_fin\_gl\_threshold\_rule\] table stores variance threshold information for general ledger rules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/fin-gl-threshold-rule-table.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-07-13"
reading_time_minutes: 2
breadcrumb: [Primary data tables, Reference, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Threshold rule \[sn\_fin\_gl\_threshold\_rule\] table

The Threshold Rule \[sn\_fin\_gl\_threshold\_rule\] table stores variance threshold information for general ledger rules.

This table extends the GL Rule \[sn\_fin\_gl\_rule\] table and contains the following fields.

|Field|Data type|Description|
|-----|---------|-----------|
|Threshold amount|Decimal|Threshold amount used to calculate variance.|
|Threshold percent|Decimal|Threshold percentage used to calculate variance.|
|Threshold type|Choice|Determines whether the threshold is calculated using amount, percent, or both. The options are Amount, Percent, Amount or Percent, or Amount and percent.|
|Name|String|Name of the GL rule. Inherited from the GL Rule \[sn\_fin\_gl\_rule\] table.|
|Class name|String|Table class name of the rule record. Inherited from the GL Rule \[sn\_fin\_gl\_rule\] table.|
|Table|Table name|Table to which the rule applies. Inherited from the GL Rule \[sn\_fin\_gl\_rule\] table.|
|Execution order|Integer|Order in which the rule is executed relative to other rules. Inherited from the GL Rule \[sn\_fin\_gl\_rule\] table.|
|Inactive|Boolean|Inactive status of the rule. Inherited from the GL Rule \[sn\_fin\_gl\_rule\] table.|
|Conditions|Conditions|Conditions on the selected table that determine when the rule applies. Inherited from the GL Rule \[sn\_fin\_gl\_rule\] table.|
|Default|Boolean|Indicates whether this is the default rule. Inherited from the GL Rule \[sn\_fin\_gl\_rule\] table.|

**Parent Topic:**[Primary data tables for Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/spo-primary-data-tables.md)

**Related topics**  


[Fixed Asset \[sn\_fin\_fixed\_asset\] table]()

[Finance Exchange Rates \[sn\_fin\_fx\_rate\] table]()

[Ledger Account table]()

[GL rule \[sn\_fin\_gl\_rule\] table]()

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

