---
title: Organization \[sn\_fin\_organization\] table
description: The Organization \[sn\_fin\_organization\] table stores information about organizational entities such as companies and legal entities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/fin-organization-table.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-07-13"
reading_time_minutes: 3
breadcrumb: [Primary data tables, Reference, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Organization \[sn\_fin\_organization\] table

The Organization \[sn\_fin\_organization\] table stores information about organizational entities such as companies and legal entities.

This table contains the following fields.

|Field|Data type|Description|
|-----|---------|-----------|
|Type|Choice|Table class name that indicates the specific type of organization record.|
|Display name|String|System-generated display name of the organization.|
|Legal name|String|Legal name of the entity corresponding to the location in which it operates.|
|Short description|String|Short description of the organization.|
|Global company|Reference|Main company to which this entity belongs at a global level.|
|Region|Choice|Region from which the entity operates. The options are AMS, APAC, EMEA, or LATAM.|
|Industry|Reference|Industry to which the entity belongs.|
|Local currency|Reference|Local currency of the entity.|
|Active|Boolean|Indicates whether the entity is active.|
|Parent entity|Reference|Parent entity of this organization.|
|Street address|String|Street address of the entity's location.|
|City|String|City of the entity's location.|
|State / Province|String|State or province of the entity's location.|
|Zip / Postal code|String|Zip or postal code of the entity's location.|
|PO box number|String|PO box number to which supplier correspondence and payments are sent.|
|County / District|String|Specific area within a state or a province.|
|Country|String|Country of the entity's location.|
|Website|URL|Official website of the entity.|
|Owner|Reference|User who owns this organization record.|
|ERP company code|String|Company code of the entity in the ERP system.|
|Status|Choice|Business relationship designated to the entity.|
|Reporting currency|Reference|Reporting currency of the entity.|
|Alternate currency|Reference|Alternate currency of the entity.|
|ERP source|Reference|ERP source system associated with the entity.|
|Image|Image|Image of the entity's logo.|
|Is transform map running?|Boolean|Internal flag that indicates whether a transformation is in progress.|

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

