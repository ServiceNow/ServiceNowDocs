---
title: 'Foundation' stage reports on the CSDM Data Foundations dashboard
description: The Foundation tab on the CSDM Data Foundations dashboard identifies data that might be missing from the CMDB.
locale: en-US
release: zurich
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Reference, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# 'Foundation' stage reports on the CSDM Data Foundations dashboard

The **Foundation** tab on the CSDM Data Foundations dashboard identifies data that might be missing from the CMDB.

## Reports on the Foundation tab

In this example, a report on the **Foundation** tab indicates that most named product models don't have associate product owners. Without this data, you might not be able, for example, to identify products that are reaching end-of-life. For more information, see [Products and product models](../concept/foundation-domain.md#dlentry-product-models).

![Foundation tab on the Data Foundations dashboard.](../image/csdm-data-fdns-dash-foundation.png)

-   **CSDM Foundation Indicators report**
    -   The **Priority** value is the product of the weight of the metric and the severity of the actual score. Priority ranges from 1 — Critical \(the highest priority\), to 5 — Low \(the lowest priority\).
    -   The **Result** column displays a color-coded bar showing the percentage of CIs or the measured item that are in compliance for the key foundational metric.

        -   Red: 0–50% are in compliance.
        -   Yellow: 50–90% are in compliance.
        -   Green: More than 90% are in compliance.
        To ensure optimum performance, the system stops collecting data for some metrics when they reach a specified number of non-compliant CIs. For information on managing data collection for a metric that isn't needed or that affects performance of the dashboard, see [Manage performance](../../configuration-management/concept/csdm-cmdb-foundations-dashboards.md#section-manage-performance).

    -   The **Remediation playbook URL** column displays links to knowledge articles in Now Support with instructions for bringing the CIs into compliance. Use your Now Support credentials to access the knowledge article.

To view detailed information on the impact of a metric and for details on working on issues, select the appropriate **Remediation playbook URL**.

-   **Named product models without product**

    Application, service, and software class instance CIs aren't created through Discovery, so their **Model ID \[model\_id\]** values might not refer to product model records. To help you to migrate to a product-centric management paradigm, each instance of a logical CI should be associated with a product model. For recommendations, see [Auto-generate product models for logical CIs](../task/csdm-auto-create-prod-model-for-ci.md).

    For more information, see [Products and product models](../concept/foundation-domain.md#dlentry-product-models).

-   **Locations without parents**

    You can create a hierarchy of location data using the Parent attribute to match your reporting requirements. Missing parent locations break the structure. See [Location \[cmn\_location\] table](../concept/csdm-implement-foundation-stage.md#dlentry-location-table).

-   **Business units without companies**

    The hierarchy of your business is populated in the Business Unit table with a reference to the parent company. A business unit is a part of your organization that is responsible for specific operations, such as finance, human resources \(HR\), or IT. A hierarchy within a business unit is common. For large multinational organizations, you may have business units that identify independent regional operations and the specific operations within the region.


-   **[Auto-generate product models for logical CIs](../task/csdm-auto-create-prod-model-for-ci.md)**  
Use the CSDM Product Model Assignment job to auto-generate a product model record \(application model, service model, or software model\) for each logical CI that is not yet associated with a product model. Product models are ideal for associating CIs that are parts of a single digital product.

**Parent Topic:**[CSDM reference](../concept/csdm-content-frame-reference.md)

**Related topics**  


[CSDM Data Foundations dashboard](../concept/csdm-data-foundations-dashboard.md)

