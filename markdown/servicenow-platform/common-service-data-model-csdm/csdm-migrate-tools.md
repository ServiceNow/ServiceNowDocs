---
title: Assistance with the CSDM life-cycle sync process
description: Several features help you to ensure accuracy and completeness for the process of syncing legacy data with life-cycle data in the CSDM framework.
locale: en-US
release: yokohama
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Sync existing data, Implement, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Assistance with the CSDM life-cycle sync process

Several features help you to ensure accuracy and completeness for the process of syncing legacy data with life-cycle data in the CSDM framework.

## Before you perform the life-cycle sync process

-   **Data migration script**

    Use the fix script from the ServiceNow Community to identify table dependencies. See [Migrating into CSDM identifying table dependencies](https://community.servicenow.com/community?id=community_article&sys_id=a777f564db9dbfc4d58ea345ca961996).

-   **CMDB Data Foundations dashboard**

    Navigate to **All** &gt; **Configuration** and then select **CMDB Data Foundations Dashboard**.

    -   CMDB dashboard: Each tab provides key metrics that evaluate configuration and customizations in the CMDB.
    -   The metrics provide visible results of evaluation. Color codes and weighted priority help with planning.
    -   Each metric includes a link to a remediation playbook with background and plays for remediation.
    See [Monitor system foundations in the CSDM and the CMDB Data Foundations Dashboards](../../configuration-management/concept/csdm-cmdb-foundations-dashboards.md).

-   **CSDM Data Foundations dashboard**

    Navigate to **All** &gt; **Configuration** and then select **CSDM Data Foundations Dashboard**.

    The CSDM dashboard focuses on key data elements to support you in implementing the CSDM framework. The reports on each tab display the data metrics that are appropriate for the maturity of your organization's CSDM implementation stage \(foundation, crawl, walk, run, and fly\). See [CSDM Data Foundations dashboard](csdm-data-foundations-dashboard.md). In particular, the **Crawl** tab presents a report titled **CIs with Mismatched Operational Status and Life Cycle Stage** that shows a summary of life-cycle value mismatches among CMDB, asset, and IBI and enables you to view mismatch details. See ['Crawl' stage reports on the CSDM Data Foundations dashboard](../reference/csdm-datafdn-dash-crawl-tab.md).

-   **View the contents of life-cycle tables**

    To view how life-cycle value pairs are mapped in the mapping tables, select **All**, and then enter `life_cycle_stage.list` in the search text box.

-   **Migrating nonconforming CIs into the correct CSDM tables**

    If you already have CSDM data but not in the recommended tables, you can run a script to identify dependencies that you may have created on the nonconforming tables. The results of the script identify referenced dependencies such as reports, UI scripts, business rules, and other references for a specified table \(editable in the script\). See this [post on the Now Community site](https://www.servicenow.com/community/common-service-data-model/migrating-into-csdm-identifying-table-dependencies/ta-p/2308617)

-   **The life-cycle sync process presents the discrepancy report**

    When you start the sync process, the discrepancy report [Enabling CSDM life-cycle sync between legacy fields and related assets](../../configuration-management/concept/csdm-life-cycle-standard-values.md#) helps you to isolate and remediate mapping issues or missing data issues before proceeding with migration and syncing. The report identifies issues and presents links that take you to the mappings that must be resolved before you can sync the data.


**Parent Topic:**[Migrate and sync existing data to the CSDM framework](../task/migrate.md)

**Related topics**  


[Enabling CSDM life-cycle sync between legacy fields and related assets](../../configuration-management/concept/csdm-life-cycle-standard-values.md#)

