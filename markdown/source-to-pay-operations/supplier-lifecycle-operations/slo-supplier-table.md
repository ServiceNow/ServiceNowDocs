---
title: Supplier table
description: The Supplier \[sn\_fin\_supplier\] table stores important information about a supplier.
locale: en-US
release: yokohama
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Primary data tables for Supplier Lifecycle Operations, Supplier Lifecycle Operations reference, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Supplier table

The Supplier \[sn\_fin\_supplier\] table stores important information about a supplier.

## Supplier \[sn\_fin\_supplier\] table

The Supplier \[sn\_fin\_supplier\] table contains the following fields.

|Field|Data type|Description|
|-----|---------|-----------|
|Legal Name|String|Legal name of the supplier that corresponds to its operating location.|
|DUNS number|Integer|Unique, 9-digit identifier for a supplier.|
|ERP supplier code|Integer|Company code of the supplier in the ERP system.|
|Parent entity|Reference|Parent organization of the supplier.|
|Global company|Reference|Global company that the supplier is linked to.|
|Industry|String|Industry to which the supplier belongs.|
|Website|URL|Website of the supplier.|
|Image|Image|Image of the supplier’s logo.|
|Description|String|Detailed description of the supplier.|
|Relationship manager|String|Person responsible for managing the relationship with this supplier.|
|Relationship status|List|Business relationship that is designated to the supplier. The options are Strategic, Valued, Tactical, or Excluded.|
|Onboarded|Boolean|Status of whether the supplier is onboarded into the ERP system. The options are Yes or No.|
|Valid NDA|Boolean|Status of whether the supplier has a valid non-disclosure agreement. The options are Yes or No.|
|Valid risk assessment|Boolean|Status of whether a valid risk assessment has been performed for the supplier. The options are Yes or No.|
|Customer number|String|Unique identifier for the organization to the supplier.|
|On-boarded by|String|The person responsible for onboarding the supplier.|
|On-boarded date|String|Onboarding date of the supplier.|
|Off-boarded date|String|Termination date of the supplier from the organization.|
|Preferred|Boolean|Whether the supplier is preferred. The options are Yes or No.|
|PO box number|String|Post office box number where the supplier correspondence and payments are made.|
|ERP company code|String|Company code of the supplier in the ERP system.|
|ERP source|String|ERP source used by the organization.|
|Parent entity|String|Parent organization of the supplier.|
|Street address|String|Street where the supplier is located.|
|City|String|City where the supplier is located.|
|State/Province|String|State or province where the supplier is located.|
|County/District|String|County or district where the supplier is located.|
|ZIP/Postal code|String|Zip code or postal code where the supplier is located.|
|Country|String|Country where the supplier is located.|
|Region|String|Region where the supplier is operating. Options are AMS, APAC, EMEA, or LATAM.|
|Primary phone number|String|Phone number of the primary contact from the supplier side.|
|Fax number|String|Number to which documents can be faxed to the supplier.|

For more information, see [Supplier Lifecycle Operations data model](slo-data-model.md).

**Parent Topic:**[Primary data tables for Supplier Lifecycle Operations](slo-primary-data-tables.md)

