---
title: Product Visuals \[sn\_shop\_supplier\_product\_artifact\] table
description: The Product Visuals \[sn\_shop\_supplier\_product\_artifact\] table stores product images and media.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/spo-product-visuals-table.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-07-13"
reading_time_minutes: 2
breadcrumb: [Primary data tables, Reference, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Product Visuals \[sn\_shop\_supplier\_product\_artifact\] table

The Product Visuals \[sn\_shop\_supplier\_product\_artifact\] table stores product images and media.

This table contains the following fields.

|Field|Data type|Description|
|-----|---------|-----------|
|Name|String|Name of the product visual artifact.|
|Product model|Reference|Product model associated with this artifact.|
|Image|Image|Image file for the product artifact.|
|Type|Choice|Type of artifact. The options are Image, Video, or PDF.|
|Thumbnail url|URL|URL of the thumbnail image for the artifact.|
|Youtube url|URL|YouTube URL of the artifact video.|
|Image url|URL|URL of the artifact image.|
|Active|Boolean|Indicates whether the artifact is active.|
|Primary|Boolean|Indicates whether the artifact is the primary artifact for the product.|
|Video|Video|Video file associated with the artifact.|
|Document|Attachment|File attachment for the artifact, such as a PDF.|
|Video source|Choice|Source of the video. The options are Upload or YouTube video.|

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

[Payment Terms \[sn\_shop\_payment\_term\] table]()

[Price Break \[sn\_shop\_price\_break\] table]()

[Pricing \[sn\_shop\_m2m\_product\_contract\] table]()

[Product group \[sn\_shop\_product\_group\] table]()

[Shipping methods \[sn\_shop\_shipping\_method\] table]()

