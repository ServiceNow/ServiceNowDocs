---
title: CMN Location Stage inbound staging table
description: The CMN Location Stage inbound \[sn\_fcms\_intg\_cmn\_location\_stage\] staging table temporarily stores important data about locations before this data is sent to the primary table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/erp-spo-loc-inbound-table.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-07-01"
reading_time_minutes: 1
breadcrumb: [ERP Integration Framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# CMN Location Stage inbound staging table

The CMN Location Stage inbound \[sn\_fcms\_intg\_cmn\_location\_stage\] staging table temporarily stores important data about locations before this data is sent to the primary table.

The following table lists the fields for the CMN Location Stage inbound \[sn\_fcms\_intg\_cmn\_location\_stage\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|City|String|Name of the city where the CMN location belongs.|
|Country|String|Name of the country where the CMN location belongs.|
|Country key|String|Country key of the CMN location.|
|Default|String|Indicates whether the CMN location is default or not.|
|ERP source|String|ERP source from which data is imported. For purchase order, receipt, and invoice integrations, the ERP source is determined through the legal entity associated with these records.|
|Legal entity|String|Name of the legal entity|
|Location|String|Coordinates or details of the CMN location.|
|Name|String|Name of the CMN location.|
|Plant|String|Name of the plant at the CMN location.|
|Postal code|String|Postal code of the CMN location.|
|Region|String|Region name of the CMN location.|
|State|String|State / province of the CMN location.|
|Street|String|Street of the CMN location.|
|Street and house number|String|Street and house number of the CMN location.|
|Zip|String|Zip code of the CMN location.|

