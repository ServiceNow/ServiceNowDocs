---
title: View CMDB Health Dashboard
description: The CMDB Health Dashboard serves as a central location to view detailed health reports for your CMDB at a glance. Also, it provides functions to remediate issues that CMDB Health detected, to improve CMDB health.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [CMDB Health, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# View CMDB Health Dashboard

The CMDB Health Dashboard serves as a central location to view detailed health reports for your CMDB at a glance. Also, it provides functions to remediate issues that CMDB Health detected, to improve CMDB health.

Once you configure CMDB Health and the CMDB Health Dashboard Jobs are enabled, the CMDB Health Dashboard shows meaningful data that is automatically collected and calculated on a recurring schedule. For more information, see [Configuring CMDB Health](c_CMDBHealthSetupandConfig.md).

![Default view in CMDB Health Dashboard](../image/CMDBHealthDashboardYokohama.png "CMDB Health Dashboard")

## Access

Use either of the following ways to access the CMDB Health Dashboard:

-   **Service Graph Workspace:**
    1.  Navigate to **Workspaces &gt; Service Graph Workspace**.
    2.  Select the Insights icon in the navigation panel.
    3.  Select **CMDB Health** in the Insights navigation panel.
-   **CMDB Workspace:**
    1.  Navigate to **Workspaces &gt; CMDB Workspace**.
    2.  Select **Home** in the CMDB Workspace menu bar and then, in the Quick links section, select the **CMDB Health Dashboard** link.
-   **Navigation filter**

    Navigate to **All** &gt; **Configuration** &gt; **CMDB Health Dashboard** and then select one of the following dashboard views:

    -   **Class View**: Default view for the CMDB Health Dashboard, showing health reports for CIs and classes in the CMDB hierarchy.
    -   **Service View**: Health reports for services with details for CIs per service.
    -   **Health Group View**: Health reports for CMDB groups of type Health with details for CIs per group.

Role requirement: Using the CMDB Health Dashboard requires the asset, sn\_cmdb\_editor, cmdb\_user, or itil role.

## Legacy calculation methods

By default, all metrics and KPIs are set with a specific percentage weight in score calculations. However, you can use legacy calculation methods which were used up until the Washington DC release by toggling the **Use legacy calculation methods** switch \(requires the sn\_cmdb\_admin role\) on the CMDB Health Dashboard. In those methods, calculating aggregation scores is based on weights settings for metrics within their KPI, and KPIs within the overall score. Use the legacy calculation methods when it is important to reflect on specific weights of metrics and KPIs in the assessment of CMDB health in your organization.

For more information about customizing calculation weights for metrics, KPIs, and the overall score, see [Configure aggregation weights for CMDB Health scores](../task/config-cmdb-health-metric-weights.md).

## KPI tiles

The Completeness, Correctness, and Compliance KPI tiles on the dashboard, show the aggregated health for CIs of the specified class \(and its descendants\), health group, or service. The KPI's aggregated percentage is represented on the donut as follows:

-   Green: Represents the CIs that are compliant on all of the KPI's metrics
-   Red: Represents the CIs that fail one or more metric

The distribution of metric compliance can vary greatly across CIs. For example, a single CI failing all metrics or 3 unique CIs each failing a different metric will result in a different KPI final score of aggregation.

You can show additional details and further drill down the CMDB Health Dashboard:

-   Point to the green and red portions in the donut reports, to show details.
-   Select the View calculation details icon \("i"\) in a KPI tile to show the calculation details of failure and success for each of the KPI metrics. Calculation details also show the status of the calculation, such as complete.
-   Select a KPI tile and then select a tab for a metric that you want to see more details for. For each metric, the dashboard shows up to ten classes \(each class in its own tile\) with the highest number of non-compliant CIs for the metric. Each tile for a class shows the total number of non-compliant CIs and also pie reports of those non-compliant CIs by discovery source and by owner.

    For example:

    1.  Select the Correctness tile.
    2.  Select the Orphan CIs tab.
    3.  Assuming that the largest number of CIs that aren't compliant with the orphan metric are Windows Servers, the first tile shows details for those CIs. The tile shows the total number of Windows Server CIs that are orphans. This tile also shows pie reports of those CIs, one by discovery source and another by owner.
    4.  Select a CI in the list view to open its CI form.
    5.  Scroll in the CI Health tile to the CMDB Health widgets with details about the CI's health.

The '&lt;x&gt;% since &lt;date&gt;' shows the increase or decrease \(in %\) in the KPI health since &lt;date&gt; \(&lt;date&gt; being the previous time that change was noted\). A ![Warning that max failure is reached.](../image/MaxFailuresCMDBHealth.png) icon indicates that the maximum failure threshold for the metric has been reached. The tests for the metric are halted for this cycle, and all associated aggregated summaries show 0%.

## Overall score

The overall score appears on the dashboard above the KPI tiles and represents the aggregated health score for the CMDB. The overall score is calculated as an aggregation of the three KPIs \(correctness, completeness and compliance\). By default, the overall score is a simple average of the KPI scores. However, if using the legacy calculation methods is in effect, then the overall score is based on any weight settings of any of the KPIs.

## Class view in the CMDB Health Dashboard

The class view shows health reports for CIs and classes in the CMDB hierarchy. Select any class in the CMDB hierarchy to filter all tiles on the dashboard to show health data only for CIs in the selected class and its child classes.

Select the **Class** drop-down to switch to the **Health Group** or the **Service** view.

## Health Group view in the CMDB Health Dashboard

Select the **Health Group** view to show health reports for CIs of a CMDB health group. Select any health group to filter all tiles on the dashboard to show health data only for CIs in the selected health group.

Select the **Health Group** drop-down to switch to the **Class** or the **Service** view.

## Service view in the CMDB Health Dashboard

Select the **Service** view to show health reports for CIs of a service class, such as **Business Service**, including the service CI itself. Select any service to filter all tiles on the dashboard to show health data only for CIs in the selected service.

**Note:** The Event Management and Service Mapping Core plugin must be activated to enable meaningful data in the service view.

Select the **Service** drop-down to switch to the **Health Group** or the **Class** view.

Settings affecting the service view:

-   The service view uses the settings for the **Business Service**, **Manual Service**, and **Technology Management Service** classes.
-   The service view doesn’t include all services from the Service \[cmdb\_ci\_service\] table. Only services from the cmdb\_ci\_service\_auto table and its descendants \(cmdb\_ci\_service\_discovered, cmdb\_ci\_service\_manual, cmdb\_ci\_query\_based\_service\), are included.
-   Property settings, such as **glide.cmdb.services\_query\_limit**, **glide.cmdb.services\_hierarchy\_limit**, and **glide.cmdb.service\_associated\_ci\_query\_limit**. For information about how you can use these properties to control the number of items that appear in the service view, see [Components installed with CMDB Health](../reference/r_TablesInstalledCMDBHealth.md).

**Parent Topic:**[CMDB Health](c_CMDBHealth.md)

**Related topics**  


[Exploring CMDB Health](exploring-cmdb-health-parent.md)

[CMDB Health experience in CMDB Workspace and in Service Graph Workspace](cmdb-health-exp-cmdb-workspace.md)

[View relationships health](../task/t_ViewRelationshipsHealth.md)

[View CI health](../task/t_ViewCIHealth.md)

[Create a CMDB remediation rule](../task/t_CreateCMDBRemediationRule.md)

[CMDB Health process tracking and troubleshooting](c_CMDBHealthTroubleshooting.md)

[CMDB Health reference](cmdb-health-ref-parent.md)

