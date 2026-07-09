---
title: Product Model Stage inbound staging table
description: The Product Model Stage inbound \[sn\_fcms\_intg\_cmdb\_model\_stage\] staging table temporarily stores important data about product models before this data is sent to the primary table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/erp-spo-prod-mod-inbound-table.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-07-01"
reading_time_minutes: 1
breadcrumb: [ERP Integration Framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Product Model Stage inbound staging table

The Product Model Stage inbound \[sn\_fcms\_intg\_cmdb\_model\_stage\] staging table temporarily stores important data about product models before this data is sent to the primary table.

The following table lists the fields for the Product Model Stage inbound \[sn\_fcms\_intg\_cmdb\_model\_stage\] staging table.

<table id="table_erp_spo_prod_mod_inbound_table"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Asset tracking

</td><td>

String

</td><td>

Process by which the model can be tracked.Select one of these options:-   Leave to Category: Model is transparent and the category defines the asset class.
-   Create Consumable Asset: Model forces the asset class to be consumable, regardless of what the category defines as the asset class.
-   Don't create assets: Model blocks asset instantiation, regardless of what the category defines as the asset class.

</td></tr><tr><td>

Description

</td><td>

String

</td><td>

Description of the product model for the buyer.

</td></tr><tr><td>

ERP source

</td><td>

String

</td><td>

ERP source from which data is imported. For purchase order, receipt, and invoice integrations, the ERP source is determined through the legal entity associated with these records.

</td></tr><tr><td>

Model category

</td><td>

String

</td><td>

Category to which the model belongs to.

</td></tr><tr><td>

Model number

</td><td>

String

</td><td>

Specific model number that is assigned to the item by the manufacturer.

</td></tr><tr><td>

Name

</td><td>

String

</td><td>

Name of the product model.

</td></tr><tr><td>

Product category

</td><td>

String

</td><td>

Category to which the product belongs to.

</td></tr><tr><td>

Short description

</td><td>

String

</td><td>

Brief description of the product model.

</td></tr></tbody>
</table>