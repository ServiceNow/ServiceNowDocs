---
title: Supplier Legal Entity Mapping inbound staging table
description: The Supplier Legal Entity Mapping inbound \[sn\_sap\_data\_int\_supplier\_stg\] staging table temporarily stores important data about the legal entities of a supplier before this data is sent to the Supplier Legal Entity Mapping \[sn\_fin\_supplier\_detail\] primary table. This staging table is delivered in a separate SAP data-integration scope rather than sn\_fcms\_intg, but it is populated as part of primary supplier data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/erp-slo-supplier-legal-entity-mapping-inbound-table.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-07-01"
reading_time_minutes: 1
breadcrumb: [ERP Integration Framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Supplier Legal Entity Mapping inbound staging table

The Supplier Legal Entity Mapping inbound \[sn\_sap\_data\_int\_supplier\_stg\] staging table temporarily stores important data about the legal entities of a supplier before this data is sent to the Supplier Legal Entity Mapping \[sn\_fin\_supplier\_detail\] primary table. This staging table is delivered in a separate SAP data-integration scope rather than sn\_fcms\_intg, but it is populated as part of primary supplier data.

**Note:** Fields listed are the confirmed core mapping fields. The complete field list for sn\_sap\_data\_int\_supplier\_stg \(SAP data-integration scope\) was not available in the reference source and must be validated with the SME before publishing.

The following table lists the fields for the Supplier Legal Entity Mapping inbound \[sn\_sap\_data\_int\_supplier\_stg\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|Legal entity|String|Name of the legal entity of the supplier.|
|Supplier|String|Name of the supplier.|

