---
title: View CI health
description: View CMDB Health report for an individual CI, on the CIs form in CMDB Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/servicenow-platform/configuration-management-database-cmdb/t\_ViewCIHealth.html
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [CMDB Health, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# View CI health

View CMDB Health report for an individual CI, on the CIs form in CMDB Workspace.

## Before you begin

Starting with [CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/cmdb-workspace.md) version 7.0, CMDB Health is fully integrated into CMDB Workspace and is required in order to access CMDB Health features, including to view CI health.

Role required: sn\_cmdb\_user \(CMDB user\)

## About this task

CI health scores are based on settings of CMDB Health KPIs and metrics. Aggregations are calculated in real-time from data stored in health-related tables which the CMDB Health Dashboard jobs update on a recurring schedule. The completeness and correctness KPIs are always up to date. However, the compliance KPI depends on audit cycles and on the **CMDB Health Dashboard - Compliance Score Calculation** dashboard job that might not have run yet.

To ensure that the latest updates to these KPIs are reflected, navigate to the respective CMDB Health dashboard job, and select **Execute Now**. For more information, see [Enable and configure a CMDB Health Dashboard job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/t_EnableCMDBHealthDashboardJob.md).

## Procedure

1.  Open the CI form for a CI, in CMDB Workspace.

    -   On a CI form that isn't in CMDB Workspace, select **Open in CMDB Workspace**.

        Role required: sn\_cmdb\_user \(minimum\)

    -   In CMDB Workspace, select a CI in a list view to open the CI's form. For example, on the CMDB Health dashboard, drill down a KPI tile and then select a CI in the tile's list view.
2.  Select the right \(&gt;\) or left \(&lt;\) handles in the CI Health tile to see all CI health-related widgets.


## Result

The widgets in the CI Health tile on the CI form show the aggregated health for the CI using the following color codes:

-   Green: The CI passed the health test \(for example, it isn't a duplicate\).
-   Red: The CI failed the health test \(for example, it is a duplicate\)
-   Grey: The CI wasn't tested for this metric, because the threshold wasn't set for the CI \(class\) in the CI module.

**Note:** Missing rules or other class definitions can prevent some health scores from being evaluated for a CI. The results in the CI Health widget in these situations, are described below:

-   **Duplicate**
    -   If no identification rules \(\[cmdb\_identifier\]\) are defined for the CI’s class or its ancestors: A notification to that effect appears.
    -   If only dependent identification rules are defined: `Not applicable` notification appears.
-   **Orphan**
    -   If the CI is excluded by health inclusion rules: `Not applicable` notification appears.
    -   If no orphan rules \(in the \[cmdb\_health\_orphan\_rule\] table\) are defined for the CI’s class or its ancestors: A notification about missing a rule appears.
-   **Staleness**
    -   If the CI is excluded by health inclusion rules: `Not applicable` notification appears.
    -   If no staleness rules \(in the \[cmdb\_health\_staleness\_rule\] table\) are defined for the CI’s class or its ancestors: A notification about missing a rule appears.
-   **Audit**
    -   If no audits \(\[cert\_audit\]\) are defined for the CI \(The CI Health widget checks only desired states and scripted audits\): `Not applicable` notification appears.
    -   If there are audits defined for the CI but the audits did not run: `Not applicable` notification appears.

**Parent Topic:**[CMDB Health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/c_CMDBHealth.md)

**Related topics**  


[Explore CMDB Health]()

[CMDB Health experience in CMDB Workspace]()

[View CMDB Health dashboard]()

[View relationships health]()

[Create a CMDB remediation rule]()

[CMDB Health process tracking and troubleshooting]()

[CMDB Health reference]()

[Enable and configure a CMDB Health Dashboard job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/t_EnableCMDBHealthDashboardJob.md)

[Timeline of CI changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/c_HistoryTimeline.md)

