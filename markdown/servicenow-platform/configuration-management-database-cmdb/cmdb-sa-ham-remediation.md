---
title: Improving CMDB data quality for HAM
description: The Remediation actions panel available for a chart in the CMDB success advisor dashboard for Hardware Asset Management \(HAM\) suggests targeted actions to improve the overall quality of your Configuration Management Database \(CMDB\).
locale: en-US
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-09-02"
reading_time_minutes: 2
breadcrumb: [Use HAM advisor, CMDB success advisor, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Improving CMDB data quality for HAM

The Remediation actions panel available for a chart in the CMDB success advisor dashboard for Hardware Asset Management \(HAM\) suggests targeted actions to improve the overall quality of your Configuration Management Database \(CMDB\).

![Example actions in the remediation actions panel shown for virtual CIs with asset.](../image/cmdb-sa-ham-remediation-actions.png "Remediation actions panel")

When remediation actions are available for a chart, the Remediation actions panel appears on the KPI Details page.

You can perform the actions suggested within the Remediation actions panel to address HAM data quality issues in the CMDB. These actions help improve the accuracy, consistency, and usability of configuration items \(CIs\), promoting better alignment with HAM.

The Remediation actions panel:

-   Improves CMDB data quality through guided actions
-   Suggests context-aware actions
-   Supports quick, informed remediation steps
-   Focuses attention on meaningful tasks
-   Appears only when actionable insights are available

## Accessing the Remediation actions panel

To open the Remediation actions panel, select a segment or count on a chart in the CMDB success advisor dashboard for HAM. The KPI Details page opens. If the remediation actions are available for the selected data, the panel appears on the details page suggesting various remediation actions.

## Available remediation actions

The Remediation actions panel provides relevant suggestions and actions based on the information in the selected chart. For example, if the chart shows CIs that weren't updated recently, the panel suggests reviewing retirement policies.

The remediation actions are available for the improvement of the following issues:

-   **CIs with invalid or unpopulated names**

    Identify and correct CIs that lack meaningful or complete naming, which can impact discovery and asset alignment.

-   **CIs with missing model entries**

    Resolve CIs missing any model-related data in the CMDB, including model ID, model name, model number, and manufacturer, all of which are essential for normalization and life cycle tracking.

-   **Stale CIs**

    Remove or update CIs that weren't updated or discovered for an extended period, helping maintain an accurate representation of your environment.

-   **Duplicate CIs**

    Remove or merge duplicate records to avoid data fragmentation and promote a single source of truth.

-   **Virtual CIs with asset**

    Identify and remove hardware assets incorrectly created for virtual CIs, which can lead to inaccurate HAM license consumption and reporting.

-   **CIs missing serial number**

    Identify and resolve CIs that have no assigned serial number, which can affect duplicate detection and hardware asset tracking.

-   **CIs missing location**

    Identify and resolve CIs that have no assigned location, which can cause gaps in asset tracking and service mapping.

-   **CI and asset state mismatch**

    Identify and resolve CIs where the installation status does not align with the corresponding asset state, which can lead to inaccurate asset life cycle reporting.


