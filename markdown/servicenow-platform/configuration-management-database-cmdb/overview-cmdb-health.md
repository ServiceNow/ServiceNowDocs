---
title: Overview of CMDB Health
description: Learn about the benefits, configuration, and usage of the CMDB Health feature.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Explore, CMDB Health, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Overview of CMDB Health

Learn about the benefits, configuration, and usage of the CMDB Health feature.

The health of the CMDB data is monitored and reported for the following KPIs, each further consisting of sub-metrics:

-   **Completeness**

    CIs are tested for required and recommended fields that are not populated.

-   **Correctness**

    CIs are tested against predefined data integrity rules such as identification rules \(to detect duplicate CIs\), orphan CI rules, and stale CI rules.

-   **Compliance**

    The CMDB data is audited for adherence to predefined certificates.

-   **Relationships**

    The health of CI relationships is tested for indicators such as orphan and duplicate relationships, and for compliance with suggested relationships, hosting and containment rules.


After CIs are tested for various health indicators \(metrics\), the results are aggregated at the class, health group, service, and relationship level, and appear on CMDB Health dashboards. For most metrics, you can configure the health tests themselves to determine how compliance and non-compliance of CIs are evaluated.

For more details about the KPIs and their associated metrics, see [CMDB Health KPIs and metrics](../reference/r_CMDBHealthMetrics.md).

**Note:** CMDB Health doesn't support non-CMDB tables.

## CMDB Health dashboards and reports

You can view CMDB Health dashboards and reports in [CMDB Workspace](cmdb-workspace.md)or in [Service Graph Workspace](sg-workspace.md). Those dashboards show CMDB Health aggregated results for compliant and non-compliant CIs for CMDB Health KPIs and their metrics.

<table id="table_dlz_mff_s5"><thead><tr><th>

Dashboard/Report

</th><th>

Use

</th></tr></thead><tbody><tr><td>

CMDB Health Dashboard1.  Navigate to **Workspaces** &gt; **Service Graph Workspace**.
2.  On the navigation panel, select the Insights icon.
3.  In the Insights navigation panel, select **CMDB Health**.

or:1.  Navigate to **Workspaces** &gt; **CMDB Workspace**.
2.  Select **Home** in the CMDB Workspace menu bar.
3.  In the Quick links section select the **CMDB Health Dashboard** link.

or:1.  Navigate to **All** &gt; **Configuration** &gt; **CMDB Health Dashboard**.
2.  Select one of the views.

</td><td>

Main CMDB Health Dashboard with the following views:**Class View**

-   Shows CIs and classes health reports with aggregations for metrics, KPIs, and class branches.
-   Access to remediation tasks that were generated for CIs that failed a health test.

**Service View**

-   Shows service health reports.
-   Detailed health for CIs per service with aggregations for metrics and services.
-   Access to remediation tasks that were generated for CIs in a service that failed a health test.

**Health Group View**

-   Shows health reports for CMDB groups of type **Health**.
-   Detailed health for CIs in the group, with aggregations for KPIs, metrics, and health groups.

In either dashboard view you can select **CMDB Health settings** to manage the CMDB Health Dashboard jobs and configure other CMDB Health settings. For more information, see [Configuring CMDB Health](c_CMDBHealthSetupandConfig.md).

</td></tr><tr><td>

Relationship Health Dashboard1.  Navigate to **Workspaces** &gt; **CMDB Workspace**.
2.  Select **Home** in the CMDB Workspace menu bar.
3.  In the Quick links section select the **Relationship Health Dashboard** link.

</td><td>

Shows various charts for relationships health, such as duplicate, orphan, and stale relationships. For more information, see [View relationships health](../task/t_ViewRelationshipsHealth.md).

</td></tr><tr><td>

CI health report -   On a CI form that isn't in CMDB Workspace, select **Open in CMDB Workspace**.
-   In CMDB Workspace, select a CI in a list view to open the CI's form. For example, on the CMDB Health Dashboard, drill down a KPI tile and then select a CI in the tile's list view.

</td><td>

On a CI form, the CI Health tile contains widgets that show CIs health reports. Select the right \(&gt;\) or left \(&lt;\) handles in the CI Health tile to scroll through the widgets.

</td></tr></tbody>
</table>## Setup and configuration

To start gathering and aggregating health data, you must enable the CMDB Health-related jobs \(CMDB Health Dashboard jobs\) which are initially disabled. You also need to configure CMDB Health related system properties and health KPIs and metric test rules, to reflect health standards in your organization.

For details about setting up and configuring CMDB Health, see [Configuring CMDB Health](c_CMDBHealthSetupandConfig.md).

<table id="table_jhf_14q_fbc"><thead><tr><th>

Location

</th><th>

Configuration

</th></tr></thead><tbody><tr><td>

[CI Class Manager](../reference/ci-class-manager-landing-page.md)**Configuration** &gt; **CI Class Manager**

</td><td>

Central location to manage CI classes and to configure CMDB health settings. Use the CI Class Manager to Manage rules and definitions that are used for health tests, such as orphan rules, audit certificates, and recommended fields rule.

 For information about configuring KPI and metric tests, see [CMDB Health KPIs and metrics](../reference/r_CMDBHealthMetrics.md).

</td></tr><tr><td>

CMDB Health PreferencesNavigate to **Configuration** &gt; **Health Preferences**, or perform the following steps:

1.  Navigate to **All** &gt; **Configuration** &gt; **CMDB Health Dashboard**.
2.  Select a view.
3.  On the CMDB Health Dashboard, select **CMDB Health settings**.

</td><td>

Central location for configuring CMDB Health settings:-   Configure CMDB Health system properties.
-   Enable and manage the CMDB Health Dashboard jobs.
-   Activate or deactivate KPIs and metrics.
-   Set the maximum failure threshold for the KPIs and metrics.
-   Configure creation of tasks for failed CIs.

</td></tr></tbody>
</table>## CI remediation

CMDB Health provides a framework for configuring [CI remediation](../task/t_CreateCMDBRemediationRule.md). Remediation lets you proactively apply corrective actions to unhealthy CIs in a managed and standardized fashion.

## Domain separation

CMDB Health is domain aware. If the domain separation plugin has been activated, then the CMDB Health Dashboard shows health based on data, rules, and settings from the logged-on user domain. If rules and settings aren't defined for a child domain, then the parent's settings are applied, recursively.

For more information, see [Domain separation in CMDB Health](cmdb-health-domain-separation.md).

**Parent Topic:**[Exploring CMDB Health](exploring-cmdb-health-parent.md)

