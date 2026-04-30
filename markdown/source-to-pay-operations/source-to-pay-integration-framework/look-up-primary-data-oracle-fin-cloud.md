---
title: Look up primary data in Oracle Financial Cloud
description: You can run a job to look up primary data from different ERP sources into ServiceNow.
locale: en-US
release: yokohama
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2025-11-14"
reading_time_minutes: 2
breadcrumb: [Configure, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Look up primary data in Oracle Financial Cloud

You can run a job to look up primary data from different ERP sources into ServiceNow.

Before you start the ERP integration, you must configure the integration services record for the target ERP source using the `sn_fcms_intg_service` table. The `sn_fcms_intg_service` table is a mapping table between sub flows and target ERP source. For more information on creating an integration service record, see [Create Integration Service record](../../accounts-payable-operations/task/create-integration-service-record.md).

You can manually run jobs for the following entities:

|Entity|Table name|
|------|----------|
|Suppliers|[Supplier location inbound staging table](../../supplier-lifecycle-operations/reference/slo-supp-location-inbound-table.md)|
|Payment Terms|[Payment Terms Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-pay-terms-inbound-table.md)|
|Legal entities|[Legal Entity Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-legal-entity-inbound-table.md)|
|Currencies|[FX Currency Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-fx-currency-inbound-table.md)|
|GL Accounts|[GL Account Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-gl-account-inbound-table.md)|
|Purchasing Organizations|[Purchase Entity Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-purch-entity-inbound-table.md)|
|Plant Addresses|[CMN Location Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-loc-inbound-table.md)|
|Cost Centers|[Cost Center Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-cost-center-inbound-table.md)|

## Transformation maps and subflows

To learn more about the Transformation maps and subflows, see [Source-to-Pay integration framework transform maps and subflows](../../sourcing-procurement-operations/concept/s2p-transform-maps-flows.md).

