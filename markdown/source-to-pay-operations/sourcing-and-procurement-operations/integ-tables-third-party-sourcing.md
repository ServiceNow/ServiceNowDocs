---
title: Integration tables for third-party sourcing
description: Integration tables are used to interact with the third-party sourcing application. Relevant information that is required to conduct a Request for anything \(RFx\) in the third-party application is staged within ServiceNow and transferred through APIs to the third-party application.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Sourcing Procurement Operations integration third-party, Integrate, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Integration tables for third-party sourcing

Integration tables are used to interact with the third-party sourcing application. Relevant information that is required to conduct a Request for anything \(RFx\) in the third-party application is staged within ServiceNow and transferred through APIs to the third-party application.

The following integration tables are used:

-   Sourcing Outbound Queue, which stores the sourcing requests. It captures the items that must be sourced along with the shopper, employee, or requester's requirements from sourcing intake.
-   Sourcing Line Outbound Queue, which stores the purchase lines associated with the sourcing requests. It captures the supplier details that the shopper, employee, or requester wanted to source from. Additionally, ServiceNow sends any other suppliers that supply the same product model as the item that must be sourced.
-   Sourcing Event Outbound Queue, which stores the negotiation type, objectives, third party sourcing event record, sourcing event number, and supplier response close associated with the sourcing requests.
-   Sourcing Bid Stage, which is an inbound table used as part of the RFx process. It’s used to get the supplier responses to the RFx in real time from the third-party tool, back into the ServiceNow instance.
-   Awarded Supplier Outbound Queue, which stores the awarded suppliers. It captures the supplier details that are awarded in ServiceNow, and shares this data with the third-party tool for them to share the award business wins or losses with the suppliers.

|Field|Field type|Description|
|-----|----------|-----------|
|City|String|Delivery city|
|Country|String|Delivery country|
|End date|Other Date|End date of the service|
|Expected delivery date|Other Date|Expected delivery date of the good|
|Grouped sourcing request number|String|ServiceNow's sourcing event record number|
|Integration status|String|Integration processing status|
|Manufacturer|String|Name of the manufacturer|
|Manufacturer part number|String|Part number of the manufacturer|
|Maximum budget|Decimal|Internal budget provided by the requester|
|Preferred currency|String|Preferred currency of transaction|
|Processing message|String|Integration processing message|
|Product category|String| |
|Product model|String|Product model name. Required for catalog items.|
|Product model short description|String|Short description of the product model|
|Product name|String|Product name. Required for off-catalog items.|
|Product type|String|Good or service|
|Purchase reason|String|Internal reason to purchase this item|
|Quantity|Integer|Quantity provided by the requester|
|Start date|Other Date|Start date of the service|
|State|String|Delivery state|
|Street|String|Delivery street|
|Sourcing request number|String|ServiceNow's sourcing request record number|
|Sourcing request short description|String|ServiceNow's sourcing request short description|
|Sourcing request status|String|Status of the requester's intake record \(sourcing request\)|
|Supplier responses close|Other Date|Formerly named Bids end date. This is the due date for all suppliers to provide a response to an RFx.|
|Third party tool name|String|Name of the third-party tool|
|Third party tool RFx ID|String|Event number of the third-party tool|
|Third party tool RFx ID status|String|Event status of the third-party tool|
|Third party tool RFx URL|String|Event URL of the third-party tool|
|Unit|String|Unit populated on the product details|
|UNSPSC|String|UNSPSC code|
|Zip code|String|Delivery zip code|

|Field|Field type|Description|
|-----|----------|-----------|
|Integration status|String|Integration processing status|
|Processing message|String|Integration processing message|
|Purchase line number|String|ServiceNow's purchase line record number|
|Sourcing out queue header|Reference|Reference to the sourcing outbound table|
|Sourcing request number|String|ServiceNow's sourcing request record number|
|Supplier company name|String|Supplier name. This can be requested by the requester or existing supplier providing a catalog item|
|Supplier email address|String|Email address of the supplier|
|Supplier ERP number|String|Identification number for the supplier in the ERP system|
|Supplier number|String|ServiceNow's supplier record|
|Supplier part number|String|Part number of the supplier|

|Field|Field type|Description|
|-----|----------|-----------|
|Integration status|String|Integration processing status|
|Negotiation objectives|String|Objectives or outcome of the negotiation|
|Negotiation type|String|Type of negotiation, such as quote for example.|
|Number|String|ServiceNow's sourcing event record number|
|Processing message|String|Integration processing message|
|Supplier response close|Other Date|Formerly named Bids end date. This is the due date for all suppliers to provide a response to an RFx.|
|Third party sourcing event record|String|Third party's sourcing event record number|

|Field|Field type|Description|
|-----|----------|-----------|
|Grouped sourcing request number|String|ServiceNow's sourcing event record number|
|Integration status|String|Integration processing status|
|Manufacturer|String|Name of the manufacturer|
|Manufacturer part number|String|Part number of the manufacturer|
|Preferred currency|String|Preferred currency of transaction|
|Processing message|String|Integration processing message|
|Product category|String| |
|Product model|String|Product model name. Required for catalog items.|
|Product model short description|String|Short description of the product model|
|Product name|String|Product name. Required for off-catalog items. This is a required field.|
|Product type|String|Good or service|
|Purchase line number|String|ServiceNow's purchase line record number|
|Quote number|String|Quote number back from Request for Quote \(RFQ\)|
|Quote price|String|Quote unit price back from RFQ|
|Shipping amount|String|Quote shipping amount from RFQ|
|Sourcing out queue ID|String|Reference to the sourcing outbound table|
|Sourcing request number|String|ServiceNow's sourcing request record number. This is a required field.|
|Sourcing request short description|String|ServiceNow's sourcing request short description|
|Supplier address|String|Supplier location: Address|
|Supplier city|String|Supplier city found on the quote|
|Supplier company name|String|Supplier name. This is a required field.|
|Supplier country|String|Supplier country found on the quote|
|Supplier County/District|String|Supplier location: County or district|
|Supplier delivery date|Date/Time|Supplier delivery date of the good|
|Supplier email address|String|Email address of the supplier found on the quote|
|Supplier end date|Date/Time|Supplier end date of the service|
|Supplier ERP number|String|Identification number for the supplier in the ERP system|
|Supplier fax number|String|Supplier fax number found on the quote|
|Supplier lead time \(days\)|String|Supplier lead time|
|Supplier notes|String|Notes from the supplier, if any|
|Supplier number|String|ServiceNow's supplier record|
|Supplier part number|String|Part number of the supplier|
|Supplier PO box number|String|Supplier PO box number found on the quote|
|Supplier primary phone number|String|Supplier primary phone number found on the quote|
|Supplier quantity|String|Supplier quantity found on the quote. This is a required field.|
|Supplier region|String|Supplier location: Region|
|Supplier start date|Date/Time|Supplier start date of the service|
|Supplier State/Province|String|Supplier state found on the quote|
|Supplier street address|String|Supplier location: Street address|
|Supplier website|String|Supplier website, if provided on the quote|
|Supplier Zip / Postal code|String|Supplier zip code found on the quote|
|Third party tool name|String| |
|Third party tool RFx ID|String|Event number of the third-party tool|
|Third party tool RFx ID status|String|Event status of the third-party tool|
|Third party tool RFx URL|String|Event URL of the third-party tool|
|Unit|String|Unit populated on the product details. This is a required field.|
|UNSPSC|String|UNSPSC code|

|Field|Field type|Description|
|-----|----------|-----------|
|Integration status|String|Status of the integration process.|
|Processing message|String|Describes the current processing status.|
|Purchase line number|String|ServiceNow's purchase line record number.|
|Purchase requisition number|String|ServiceNow's purchase requisition record number created after awarding|
|Quantity|Integer|Quantity of the goods or service awarded to the supplier.|
|Sourcing request number|String|Unique identifier of the sourcing request created inServiceNow's.|
|Supplier company name|String|Name of the supplier company that is awarded the quote.|
|Supplier ERP number|String|Identification number for the supplier in the ERP system.|
|Supplier number|String|ServiceNow's supplier record.|
|Third party tool name|String|Name of the third-party tool.|
|Third party tool RFx URL|String|Event URL of the third-party tool.|

**Parent Topic:**[Sourcing and Procurement Operations integration with third-party sourcing solutions](psm-integration-third-party-sourcing.md)

