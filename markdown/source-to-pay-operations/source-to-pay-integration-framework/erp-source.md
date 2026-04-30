---
title: ERP source
description: An ERP Source \[sn\_fin\_erp\_source\] table is available in Source-to-Pay \(S2P\) as part of the Finance Common Architecture application.
locale: en-US
release: xanadu
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Source-to-Pay integration framework, Source-to-Pay integration with third-party applications, Source-to-Pay Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# ERP source

An ERP Source \[sn\_fin\_erp\_source\] table is available in Source-to-Pay \(S2P\) as part of the Finance Common Architecture application.

You can use the **ERP Source** field available in tables to directly identify the correct ERP source if you have integrations with multiple ERP systems.

**Note:**

-   In some scenarios, for purchase orders, receipts, and invoice integration, the ERP source for records is still determined through the legal entity on those records. This is achieved by adding an **ERP Source** reference field on the Legal Entity \[sn\_fin\_legal\_entity\] table. Also, Legal Entity is added as a related list for the ERP Source table.
-   The ERP source column in the global table should be deprecated and migrated to local tables. Run the data migration script manually to move data from the impacted tables to the new mapping table. For more information, see [Migrate ERP source data from global tables to the mapping table \[KB1733450\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1733450).

    The Multi-ERP data will continue to function without migrating the ERP source column \(for up to the next two family releases from Yokohama\), but ensure migration to local tables is completed.


## Tables containing the ERP Source column

The following tables contain the ERP Source column.

|Application|Table|
|-----------|-----|
|Global|CMDB Categories \[cmdb\_categories\]|
| |Product Model \[cmdb\_model\]|
| |Service Model \[cmdb\_service\_product\_model\]|
| |Cost Center \[cmn\_cost\_center\]|
| |Department \[cmn\_department\]|
| |Location \[cmn\_location\]|
|Source-to-Pay Common Architecture|Negotiation \[sn\_shop\_negotiation\]|
| |Negotiation Event \[sn\_shop\_negotiation\_event\]|
| |Office Location \[sn\_shop\_office\_location\]|
| |Purchase Requisition \[sn\_shop\_purchase\_requisition\]|
| |Sourcing Request \[sn\_shop\_sourcing\_activity\]|
| |Supplier Product \[sn\_shop\_supplier\_product\]|
|Finance Common Architecture|Fixed Asset \[sn\_fin\_fixed\_asset\]|
| |Office Location \[sn\_fin\_office\_location\]|

