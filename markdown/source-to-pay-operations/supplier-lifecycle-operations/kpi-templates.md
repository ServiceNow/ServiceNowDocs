---
title: KPI templates
description: KPI templates are created to define KPIs that can be used to measure supplier performance.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2025-12-03"
reading_time_minutes: 1
breadcrumb: [Configure Supplier Relationship and Performance Management, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# KPI templates

KPI templates are created to define KPIs that can be used to measure supplier performance.

You can define KPI templates and thresholds to collect the metrics systematically for evaluating supplier performance. KPI templates can be of the following types:

-   **Manual KPI templates**: KPIs created from the manual KPI templates requires users \(internal or external\) to manually input KPI data based on the frequency schedules. This option is available both for quantitative and qualitative KPIs. For more information, see [Create manual KPI templates](../task/create-kpi-template-slo.md).
-   **Automated KPI templates**: KPIs created from the automated KPI templates extract and calculate data directly from the specified table using a specified method \(count, sum, average, max, min, or latest value\) based on the frequency schedules. This option is only available for quantitative KPIs. For more information, see [Create automated KPI templates](../task/create-auto-kpi-template.md).

    **Note:**

    To enable the Automated KPIs feature after an upgrade, run the fix scripts **KPI - Dec 25 records script** and **KPI - Dec 25 data records script**. For more information, see [Run fix scripts to enable Automated KPI collection](../task/run-fixscript-automated-kpis.md).


-   **[Create manual KPI templates](../task/create-kpi-template-slo.md)**  
Create manual KPI templates to define KPIs that require users to manually input KPI data based on the frequency schedules.
-   **[Create automated KPI templates](../task/create-auto-kpi-template.md)**  
Automated KPI templates can be used to create KPIs that eliminate the dependency on manual input from users. When creating a template for automated KPIs, you can configure the data source and the calculation method.

**Parent Topic:**[Configure Supplier Relationship and Performance Management](configuring-supplier-performance-mgmt.md)

