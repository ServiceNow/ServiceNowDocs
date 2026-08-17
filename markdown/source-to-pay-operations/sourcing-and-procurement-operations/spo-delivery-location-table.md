---
title: Delivery Location \[sn\_shop\_delivery\_location\] table
description: The Delivery Location \[sn\_shop\_delivery\_location\] table stores delivery address information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/spo-delivery-location-table.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-07-13"
reading_time_minutes: 3
breadcrumb: [Primary data tables, Reference, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Delivery Location \[sn\_shop\_delivery\_location\] table

The Delivery Location \[sn\_shop\_delivery\_location\] table stores delivery address information.

This table contains the following fields.

|Field|Data type|Description|
|-----|---------|-----------|
|Address|String|Calculated value that combines the recipient's name and location.|
|Street|String|Street address of the delivery location.|
|City|String|City of the delivery location.|
|State / Province|String|State of the delivery location.|
|Zip / Postal Code|String|Zip code of the delivery location.|
|Country|Reference|Country of the delivery location.|
|Country Name|String|Country name of the delivery location.|
|Shopper|Reference|Logged-in user who saved this address.|
|Recipient|Reference|User who is the recipient of this address.|
|User saved location|Boolean|Indicates that the user saved the address for future purchases.|
|User default location|Boolean|Indicates whether this is the user's default location.|
|Deleted|Boolean|Indicates that the user soft-deleted this saved address. The record is retained for auditability and possible restore rather than being removed.|
|Work address|Reference|Office location associated with this address.|
|Location|Reference|Location used for integration with third-party systems.|
|Address verification|Choice|Indicates whether this delivery address is a real, shippable location. The options are Pending review, Valid address, or Invalid address.|
|Address approval|Choice|Indicates whether this delivery address can be used for user purchases. The options are Company approved, Not approved, Pending Review, or One time approval.|

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

[Job Code \[sn\_shop\_job\_code\] table]()

[Payment Terms \[sn\_shop\_payment\_term\] table]()

[Price Break \[sn\_shop\_price\_break\] table]()

[Pricing \[sn\_shop\_m2m\_product\_contract\] table]()

[Product group \[sn\_shop\_product\_group\] table]()

[Product Visuals \[sn\_shop\_supplier\_product\_artifact\] table]()

[Shipping methods \[sn\_shop\_shipping\_method\] table]()

