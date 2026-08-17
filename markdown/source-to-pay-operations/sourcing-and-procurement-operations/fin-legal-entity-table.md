---
title: Legal Entity \[sn\_fin\_legal\_entity\] table
description: The Legal Entity \[sn\_fin\_legal\_entity\] table stores information about legal entities used in financial and organizational structures.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/fin-legal-entity-table.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-07-13"
reading_time_minutes: 4
breadcrumb: [Primary data tables, Reference, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Legal Entity \[sn\_fin\_legal\_entity\] table

The Legal Entity \[sn\_fin\_legal\_entity\] table stores information about legal entities used in financial and organizational structures.

This table extends the Organization \[sn\_fin\_organization\] table and contains the following fields.

|Field|Data type|Description|
|-----|---------|-----------|
|Clearing account|String|Clearing account associated with the legal entity.|
|Trading partner|String|Trading partner associated with the legal entity.|
|Legal name|String|Legal name of the entity corresponding to the location in which it operates. Inherited from the Organization \[sn\_fin\_organization\] table.|
|Display name|String|System-generated display name of the entity. Inherited from the Organization \[sn\_fin\_organization\] table.|
|Global company|Reference|Main company to which this entity belongs at a global level. Inherited from the Organization \[sn\_fin\_organization\] table.|
|Region|Choice|Region from which the entity operates. The options are AMS, APAC, EMEA, or LATAM. Inherited from the Organization \[sn\_fin\_organization\] table.|
|Industry|Reference|Industry to which the entity belongs. Inherited from the Organization \[sn\_fin\_organization\] table.|
|Local currency|Reference|Local currency of the entity. Inherited from the Organization \[sn\_fin\_organization\] table.|
|Active|Boolean|Indicates whether the entity is active or onboarded. Inherited from the Organization \[sn\_fin\_organization\] table.|
|Parent entity|Reference|Parent entity of this legal entity. Inherited from the Organization \[sn\_fin\_organization\] table.|
|Street address|String|Street address of the entity's location. Inherited from the Organization \[sn\_fin\_organization\] table.|
|City|String|City of the entity's location. Inherited from the Organization \[sn\_fin\_organization\] table.|
|State / Province|String|State or province of the entity's location. Inherited from the Organization \[sn\_fin\_organization\] table.|
|Zip / Postal code|String|Zip or postal code of the entity's location. Inherited from the Organization \[sn\_fin\_organization\] table.|
|PO box number|String|PO box number to which supplier correspondence and payments are sent. Inherited from the Organization \[sn\_fin\_organization\] table.|
|County / District|String|Specific area within a state or a province. Inherited from the Organization \[sn\_fin\_organization\] table.|
|Country|String|Country of the entity's location. Inherited from the Organization \[sn\_fin\_organization\] table.|
|Website|URL|Official website of the entity. Inherited from the Organization \[sn\_fin\_organization\] table.|
|Owner|Reference|User who owns this entity record. Inherited from the Organization \[sn\_fin\_organization\] table.|
|ERP company code|String|Company code of the entity in the ERP system. Inherited from the Organization \[sn\_fin\_organization\] table.|
|Status|Choice|Business relationship designated to the entity. Inherited from the Organization \[sn\_fin\_organization\] table.|
|Reporting currency|Reference|Reporting currency of the entity. Inherited from the Organization \[sn\_fin\_organization\] table.|
|Alternate currency|Reference|Alternate currency of the entity. Inherited from the Organization \[sn\_fin\_organization\] table.|
|ERP source|Reference|ERP source system associated with the entity. Inherited from the Organization \[sn\_fin\_organization\] table.|
|Image|Image|Image of the entity's logo. Inherited from the Organization \[sn\_fin\_organization\] table.|

**Parent Topic:**[Primary data tables for Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/spo-primary-data-tables.md)

**Related topics**  


[Fixed Asset \[sn\_fin\_fixed\_asset\] table]()

[Finance Exchange Rates \[sn\_fin\_fx\_rate\] table]()

[Ledger Account table]()

[GL rule \[sn\_fin\_gl\_rule\] table]()

[Threshold rule \[sn\_fin\_gl\_threshold\_rule\] table]()

[Industry \[sn\_fin\_industry\] table]()

[Ledger \[sn\_fin\_ledger\] table]()

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

