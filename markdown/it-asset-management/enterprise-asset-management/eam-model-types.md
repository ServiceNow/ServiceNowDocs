---
title: Model types in Enterprise Asset Management
description: Every enterprise model in the Enterprise Asset Management application is assigned a model type that determines its structural nature. Each enterprise model can represent standalone enterprise assets, quantity-tracked consumable assets, or complex assemblies that are comprised of multiple components.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/enterprise-asset-management/eam-model-types.html
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2026-05-20"
reading_time_minutes: 1
breadcrumb: [Enterprise Asset Management data model, Explore, Enterprise Asset Management, IT Asset Management]
---

# Model types in Enterprise Asset Management

Every enterprise model in the Enterprise Asset Management application is assigned a model type that determines its structural nature. Each enterprise model can represent standalone enterprise assets, quantity-tracked consumable assets, or complex assemblies that are comprised of multiple components.

The Enterprise Asset Management application supports the following model types:

<table id="table_b3v_hpz_hjc"><thead><tr><th>

Model type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Consumable models

</td><td>

Represents consumable assets that you can track by quantity, such as safety gloves, printer cartridges, and lubricants. Can also represent individual components within a multi-component model.**Note:** The Enterprise Asset Management application does not classify consumable models through the Consumable model \[cmdb\_consumable\_product\_model\] class that is available in the base CMDB class hierarchy. Instead, you can manually designate any enterprise model in any model category as consumable by setting the **Model type** field to **Consumable** on the corresponding enterprise model record.

</td></tr><tr><td>

Simple models

</td><td>

Represents standalone enterprise assets that you can track individually, such as office furniture and hand-held scanners. These enterprise assets do not have a component structure or any child assets.

</td></tr><tr><td>

Pre-assembled models

</td><td>

Represents equipment that you receive as complete, pre-configured assemblies from a vendor. You must define each assembly component in the corresponding enterprise model record before creating any assets that represent those components.

</td></tr><tr><td>

User-assembled models

</td><td>

Represents equipment that you must assemble on-site using components from your existing inventory. With this model type, all required components must be readily available in your stockrooms before any assembly begins.

</td></tr></tbody>
</table>-   **[Multi-component models and assets in Enterprise Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/complex-models.md)**  
Multi-component models and multi-components assets help you track the maintenance of your enterprise assets.

**Parent Topic:**[Enterprise Asset Management data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/eam-data-model.md)

