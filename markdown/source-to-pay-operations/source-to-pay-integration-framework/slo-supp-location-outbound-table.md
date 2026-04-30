---
title: Supplier location outbound staging table
description: The Supplier location outbound \[sn\_spend\_intg\_supplier\_location\_outbound\] staging table stores important data about the geographical location of a supplier so that an ERP integrator can export this data to a third-party ERP system.
locale: en-US
release: yokohama
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Outbound staging tables for Supplier Lifecycle Operations, Outbound staging tables for Source-to-Pay Operations, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Supplier location outbound staging table

The Supplier location outbound \[sn\_spend\_intg\_supplier\_location\_outbound\] staging table stores important data about the geographical location of a supplier so that an ERP integrator can export this data to a third-party ERP system.

## Supplier location outbound staging table

The following table lists the mandatory fields for the Supplier location outbound \[sn\_spend\_intg\_supplier\_location\_outbound\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|Category|String|Category of the supplier location.|
|City|String|Name of the city of the supplier.|
|Company|String|Name of the company that the supplier is linked to.|
|Contact|String|Contact details of the supplier location.|
|Coordinates retrieved on|String|Coordinates of the supplier location.|
|Country|String|Name of the country of the supplier.|
|Duplicate|String|Indicates if the supplier location is a duplicate.|
|ERP company code|String|Company code of the supplier location in the ERP system.|
|ERP source|String|ERP source from which data is imported.|
|External unique ID|String|Unique external ID number generated for the supplier location.|
|Fax phone|String|Fax number of the supplier location.|
|Full name|String|Full name of the supplier location.|
|Integration status|String|Current status of the supplier location integration.|
|Lat long error|String|Indicates if there’s a latitude or longitude error in the supplier location.|
|Latitude|String|Latitude of the supplier location.|
|Location source|String|Source of the supplier location.|
|Location type|String|Type of supplier location.|
|Longitude|String|Longitude of the supplier location.|
|Managed by group|String|The name of the group that manages the supplier location.|
|Name|String|Name of the supplier location.|
|Parent|String|Parent organization of the supplier location.|
|Phone|String|Phone number of the supplier location.|
|Phone territory|String|Name of the phone territory of the location.|
|Primary|String|Name of the primary contact of the supplier location.|
|Primary location|String|Name of the supplier's primary location.|
|Processing message|String|A message that describes the current processing status.|
|State/Province|String|Name of the State/Province of the supplier location.|
|Stock room|String|Stock room details of the supplier location.|
|Street address|String|Street address of the supplier location.|
|Time zone|String|Time zone of the supplier location.|
|Zip/Postal code|String|ZIP or postal code of the supplier location.|

