---
title: Exploring CMDB success advisor
description: Learn about CMDB success advisor and review the benefits it can provide for different users in your organization.
locale: en-US
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [CMDB success advisor, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Exploring CMDB success advisor

Learn about CMDB success advisor and review the benefits it can provide for different users in your organization.

## CMDB success advisor overview

With the CMDB success advisor application, you can review CMDB Data Manager policies and Configuration Management Database \(CMDB\) settings to identify areas where improvements can be made in Data Foundations and the Hardware Asset Management \(HAM\) application. The advisor uses customized CMDB metrics to improve data quality for targeted configuration item \(CI\) classes, identifying and monitoring the CI classes most critical to your organizational processes to enable complete and accurate data in Data Foundations, and tracking hardware model categories for HAM.

## CMDB success advisor users

<table id="table_xml_sv3_ybc"><thead><tr><th>

User

</th><th>

Description

</th><th>

Additional roles required

</th></tr></thead><tbody><tr><td>

CMDB administrator

</td><td>

Users with the sn\_cmdb\_admin role can configure and improve CMDB data accuracy based on specific business use cases. With targeted CI tracking, practical data integration suggestions, and application-specific dashboards, the CMDB success advisor enables CMDB administrators to improve CMDB data accuracy and achieve key business outcomes.

For Data Foundations, administrators can select and manage principal classes, monitor data quality across the CI classes most critical to incidents, changes, and problems, and use integration coverage analysis to ensure the right data sources are keeping the CMDB accurate and complete.

For Hardware Asset Management, administrators can focus on critical hardware model categories to improve normalization rates, asset life cycle tracking, and data accuracy for business outcomes like HAM.

</td><td>

-   **pa\_viewer**

Required to filter data by principal classes in Data Foundations advisor dashboard and model categories in HAM advisor dashboard.

-   **pa\_data\_collector**

Required to view the last updated data timestamp on an advisor dashboard.

-   **cmdb\_inst\_admin**

Required to manage Service Graph Connector connections in SGC Central through CMDB success advisor.

-   **pd\_user**

Required to view Discovery and Service Mapping Patterns through CMDB success advisor with read-only access.

-   **pd\_admin**

Required to modify Discovery patterns through CMDB success advisor with write access.


</td></tr></tbody>
</table>## CMDB success advisor benefits

The following benefits are available to CMDB administrators across both Data Foundations and HAM.

<table><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Users

</th></tr></thead><tbody><tr><td>

Focused CMDB setup for specific business outcomesFor Data Foundations, advisor dashboard scope is built from principal classes recommended based on incident, problem, and change \(IPC\) activity. If IPC data is unavailable, classes are ranked by how widely they are used across your CMDB. For new instances with no historical data, a set of default classes is suggested.

For HAM, advisor dashboard scope is defined by hardware model categories.

</td><td>

Use-case-driven CMDB configuration. To learn more, see: [Set up CMDB success advisor for Data Foundations](cmdb-sa-df-config-settings.md) and [Set up CMDB success advisor for HAM](cmdb-sa-ham-config-settings.md)

</td><td>

CMDB administrator

</td></tr><tr><td>

Improved visibilityFor Data Foundations, view CI data quality metrics by principal CI class, including missing attributes, stale records, duplicate CIs, and discovery source breakdown.

For HAM, view hardware asset metrics by model category and integration source.

</td><td>

Dashboard with consolidated insights and metricsTo learn more, see: [Monitoring CMDB data quality using dashboard metrics in CMDB success advisor for Data Foundations](cmdb-sa-df-dashboard.md) and [Monitoring CMDB data quality using dashboard metrics in CMDB success advisor for HAM](cmdb-sa-ham-dashboard.md)

</td><td>

CMDB administrator

</td></tr><tr><td>

Continuous data quality improvementFor Data Foundations, track KPIs for CI completeness, stale records, duplicates, and integration coverage across principal classes.

For HAM, track KPIs for missing model ID, serial number, location, duplicates, and asset state.

</td><td>

KPI details access from the dashboard for metric monitoring, remediation tracking, and guided resolution stepsTo learn more, see: [Monitoring CMDB data quality using dashboard metrics in CMDB success advisor for Data Foundations](cmdb-sa-df-dashboard.md) and [Monitoring CMDB data quality using dashboard metrics in CMDB success advisor for HAM](cmdb-sa-ham-dashboard.md)

</td><td>

CMDB administrator

</td></tr><tr><td>

Data quality improvement suggestionsFor Data Foundations, playbooks target principal class issues such as stale CIs and duplicate records.

For HAM, guided playbooks address hardware issues such as missing serial numbers and asset/CI mismatches.

</td><td>

Remediation actions panel available for a chart in the dashboardTo learn more, see: [Improving CMDB data quality for Data Foundations](cmdb-sa-df-remediation.md) and [Improving CMDB data quality for HAM](cmdb-sa-ham-remediation.md)

</td><td>

CMDB administrator

</td></tr><tr><td>

Better alignment of CMDB rules and policiesFor Data Foundations, align CMDB Data Manager ownership policies and reconciliation rules for principal classes.

For HAM, configure synchronization rules, asset creation rules, and status mappings.

</td><td>

Settings summary for gap analysis and configuration guidanceTo learn more, see: [Analyze CMDB settings for Data Foundations](cmdb-sa-df-analyze-settings.md) and [Analyze CMDB settings for HAM](cmdb-sa-ham-analyze-settings.md#)

</td><td>

CMDB administrator

</td></tr><tr><td>

Improved CMDB data coverage and accuracyFor Data Foundations, evaluate integration sources with attribute-level coverage analysis across principal classes.

For HAM, review SGC and Discovery pattern rankings for hardware model categories.

</td><td>

Data integrations summary for reviewing and evaluating integration sourcesTo learn more, see: [Analyzing data integrations for improving Data Foundations](cmdb-sa-df-data-integrations.md) and [Analyzing data integrations for improving HAM data coverage](cmdb-sa-ham-data-integrations.md)

</td><td>

CMDB administrator

</td></tr></tbody>
</table>## Use cases

You can use CMDB success advisor for the following business outcomes:

-   Data Foundations: Improve data quality across the principal classes your organization relies on for incidents, changes, and problems. Monitor attribute completeness, detect stale and duplicate records, and evaluate integration coverage to ensure the right data sources are populating your CMDB. For more information, see [Using CMDB success advisor for Data Foundations](cmdb-sa-df.md).
-   HAM: Improve hardware data quality across model categories such as computers, servers, and printers. Identify and fix missing model IDs, serial numbers, and locations, eliminate duplicate CIs and align asset and CI states to support accurate life cycle tracking and financial reporting. For more information, see [Using CMDB success advisor for HAM](cmdb-sa-ham-use.md).

## What to explore next

To learn more about configuring and using CMDB success advisor for supported business outcomes, see:

-   [Configuring CMDB success advisor](cmdb-sa-configuring.md)
-   [Supported business outcomes](cmdb-sa-outcomes.md)
-   [CMDB success advisor reference](cmdb-sa-reference.md)

