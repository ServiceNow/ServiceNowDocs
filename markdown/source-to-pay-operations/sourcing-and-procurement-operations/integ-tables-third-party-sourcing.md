---
title: Integration tables for third-party sourcing
description: Integration tables are used to interact with the third-party sourcing application. Relevant information that is required to conduct a Request for anything \(RFx\) in the third-party application is staged within ServiceNow and transferred through APIs to the third-party application.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Sourcing and Procurement Operations integration with third-party sourcing solutions, Integrating Sourcing and Procurement Operations with other applications, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Integration tables for third-party sourcing

Integration tables are used to interact with the third-party sourcing application. Relevant information that is required to conduct a Request for anything \(RFx\) in the third-party application is staged within ServiceNow and transferred through APIs to the third-party application.

The following integration tables are used:

-   Sourcing Outbound Queue, which stores the sourcing requests. It captures the items that must be sourced along with the shopper, employee, or requester's requirements from sourcing intake.
-   Sourcing Line Outbound Queue, which stores the purchase lines associated with the sourcing requests. It captures the supplier details that the shopper, employee, or requester wanted to source from. Additionally, ServiceNow sends any other suppliers that supply the same product model as the item that must be sourced.
-   Negotiation Event Outbound Queue, which stores the negotiation type, objectives, third party negotiation event record, negotiation event number, and supplier response closely associated with the sourcing requests.
-   Sourcing Bid Stage, which is an inbound table used as part of the RFx process. It’s used to get the supplier responses to the RFx in real time from the third-party tool, back into the ServiceNow instance.
-   Awarded Supplier Outbound Queue, which stores the awarded suppliers. It captures the supplier details that are awarded in ServiceNow, and shares this data with the third-party tool for them to share the award business wins or losses with the suppliers.

|Field|Field type|Description|
|-----|----------|-----------|
|City|String|City where the sourced items are delivered.|
|Close supplier bids now|Boolean|Indicates if the bidding phase is closed.|
|Country|String|Country where the sourced items are delivered.|
|End date|Date|Expiration date for the sourced goods or services.|
|Expected delivery date|Date|Expected delivery date of the goods or services.|
|Grouped sourcing request number|String|ServiceNow's negotiation event record number.|
|Integration status|String|Status of the sourcing integration process.|
|Internal notes|String| |
|Manufacturer|String|Name of the manufacturer that processes the sourcing request.|
|Manufacturer part number|String|Unique identifier assigned by the supplier to a specific product.|
|Maximum budget|Decimal|Internal budget provided by the requester.|
|NE out queue header|Reference| |
|Preferred currency|String|Preferred currency of transaction.|
|Processing message|String|Integration processing message.|
|Product category|String|Category to which this product belongs.|
|Product model|String|Product model name. Required for catalog items.|
|Product model short description|String|Short description of the product model.|
|Product name|String|Product name. Required for off-catalog items.|
|Product type|String|Indicates if the product is classified as goods or services.|
|Purchase reason|String|Internal reason to purchase the item.|
|Quantity|Integer|Quantity of product requested.|
|Sourcing request number|String|ServiceNow's sourcing request record number|
|Sourcing request short description|String|ServiceNow's sourcing request short description|
|Sourcing request status|String|Status of the requester's intake record \(sourcing request\)|
|Start date|Other Date|Start date of the service|
|State|String|State where the sourced items are delivered.|
|Street|String|Street where the sourced items are delivered.|
|Submitted by|String|Name of the employee who created the sourcing request.|
|Supplier responses close|String|Due date for all suppliers to provide a response to an RFx. Formerly named Bids end date.|
|Third party tool name|String|Name of the third-party tool.|
|Third party tool RFx ID|String|Unique identifier assigned to a specific sourcing event or document.|
|Third party tool RFx ID status|String|Event status of the third-party tool.|
|Third party tool RFx URL|String|Event URL of the third-party tool.|
|Unit|String|Unit populated on the product details.|
|UNSPSC|String|United Nations Standard Products and Services Code \(UNSPSC\) - Use to standardize and simplify the process of identifying and categorizing goods and services.|
|Zip code|String|Zip code where the sourced items are delivered.|

|Field|Field type|Description|
|-----|----------|-----------|
|Integration status|String|Current status of the Sourcing Line Outbound table integration.|
|Line status|String|Current status of the Sourcing line.|
|Processing message|String|A message that describes the current processing status.|
|Purchase line number|String|Purchase line record number associated with the Sourcing Line Outbound table.|
|Sourcing out queue header|Reference|Reference to the sourcing outbound table.|
|Sourcing request number|String|ServiceNow's sourcing request record number.|
|Supplier company name|String|Name of the supplier's company. This can be requested by the requester or existing supplier providing a catalog item.|
|Supplier email address|String|Email address of the supplier.|
|Supplier ERP number|String|Identification number for the supplier in the ERP system.|
|Supplier number|String|ServiceNow's supplier record number.|
|Supplier part number|String|Unique part number of the supplier.|
|Third party tool name|String|Name of the tool used by the third party.|

|Field|Field type|Description|
|-----|----------|-----------|
|Integration status|String|Current status of the Negotiation Event Outbound table integration.|
|Negotiation objectives|String|Objectives or outcome of the negotiation.|
|Negotiation type|String|Type of negotiation, such as quote for example.|
|Number|String|ServiceNow's negotiation event record number|
|Processing message|String|A message that describes the current processing status.|
|Supplier response close|Other Date|Formerly named Bids end date. This is the due date for all suppliers to provide a response to an RFx.|
|Third party negotiation event record|String|Third party's negotiation event record number.|

|Field|Field type|Description|
|-----|----------|-----------|
|Awarded|Boolean|Indicates who is the awarded supplier.|
|Grouped sourcing request number|String|ServiceNow's negotiation event record number|
|Integration status|String|Current status of the Sourcing Bid integration.|
|Manufacturer|String|Name of the manufacturer.|
|Manufacturer part number|String|Unique part number of the manufacturer.|
|Preferred currency|String|Preferred currency of transaction.|
|Processing message|String|A message that describes the current processing status.|
|Product category|String|Category to which this product belongs.|
|Product model|String|Product model name. Required for catalog items.|
|Product model short description|String|Short description of the product model.|
|Product name|String|Name of the product. Required for off-catalog items. This is a mandatory field.|
|Product type|String|Type of product. The options are Good or Service.|
|Purchase line number|String|Purchase line record number associated with the Sourcing Bid Stage table.|
|Quote number|String|Quote number back from Request for Quote \(RFQ\).|
|Quote price|String|Quote unit price back from RFQ.|
|Shipping amount|String|Quote shipping amount from RFQ.|
|Sourcing out queue ID|String|Reference to the sourcing outbound table.|
|Sourcing request number|String|ServiceNow's sourcing request record number. This is a mandatory field.|
|Sourcing request short description|String|ServiceNow's sourcing request short description.|
|Supplier address|String|Address of the supplier.|
|Supplier city|String|Supplier city found on the quote.|
|Supplier company name|String|Name of the supplier's company. This is mandatory field.|
|Supplier country|String|Supplier country found on the quote.|
|Supplier County/District|String|Name of the supplier's county or district.|
|Supplier delivery date|Date/Time|Supplier delivery date of the goods.|
|Supplier email address|String|Email address of the supplier found on the quote.|
|Supplier end date|Date/Time|Supplier end date of the service.|
|Supplier ERP number|String|Identification number for the supplier in the ERP system.|
|Supplier fax number|String|Supplier fax number found on the quote.|
|Supplier lead time \(days\)|String|Supplier's lead time.|
|Supplier notes|String|Notes from the supplier, if any.|
|Supplier number|String|ServiceNow's supplier record number.|
|Supplier part number|String|Unique part number of the supplier.|
|Supplier PO box number|String|Supplier PO box number found on the quote.|
|Supplier primary phone number|String|Supplier primary phone number found on the quote.|
|Supplier quantity|String|Supplier quantity found on the quote. This is a mandatory field.|
|Supplier region|String|Region of the supplier.|
|Supplier start date|Date/Time|Supplier start date of the service.|
|Supplier State/Province|String|Supplier state or province found on the quote.|
|Supplier street address|String|Street address of the supplier.|
|Supplier website|String|Supplier website, if provided on the quote.|
|Supplier Zip / Postal code|String|Supplier zip code found on the quote.|
|Third party tool name|String|Name of the third party tool.|
|Third party tool RFx ID|String|Event number of the third-party tool.|
|Third party tool RFx ID status|String|Event status of the third-party tool.|
|Third party tool RFx URL|String|Event URL of the third-party tool.|
|Unit|String|Unit populated on the product details. This is mandatory field.|
|UNSPSC|String|UNSPSC code on the quote.|

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

