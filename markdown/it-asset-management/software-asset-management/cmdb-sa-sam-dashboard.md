---
title: Monitoring CMDB data quality using dashboard metrics in CMDB success advisor for SAM
description: The CMDB success advisor for Software Asset Management \(SAM\) dashboard enables CMDB administrators to identify and address data quality issues specific to software installs and their related configuration items \(CIs\) in the Configuration Management Database \(CMDB\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-asset-management/software-asset-management/cmdb-sa-sam-dashboard.html
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-07-23"
reading_time_minutes: 7
keywords: [SAM advisor dashboard, monitor SAM data quality, software install data quality metrics, software installs missing edition version, duplicate software installs, virtual server host CI relationships]
breadcrumb: [Use SAM advisor, Software Asset Management, IT Asset Management]
---

# Monitoring CMDB data quality using dashboard metrics in CMDB success advisor for SAM

The CMDB success advisor for Software Asset Management \(SAM\) dashboard enables CMDB administrators to identify and address data quality issues specific to software installs and their related configuration items \(CIs\) in the Configuration Management Database \(CMDB\).

**Important:** Charts display up to the top 10 values. Any remaining values are grouped into an **Others** category. When you select a segment or count on a chart from a CMDB success advisor dashboard, the KPI Details page opens. On the page, you can analyze how a specific metric trends over time. Additionally, the Remediation actions panel appears when remediation actions are available for that card. Use the panel to improve the quality of CMDB. To learn more, see [KPI Details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/kpi-details.md) and [Improving CMDB data quality for SAM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/software-asset-management/cmdb-sa-sam-remediation.md).

If the Performance Analytics data collector exceeds its row limit during data processing, a notification banner appears on the dashboard indicating that some metrics could not be loaded. For more information, see [Data collector Performance Analytics properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/pa-dc-props.md).

## Access the dashboard

To open the dashboard, select **View insights** for SAM on the CMDB success advisor landing page. See [Viewing the CMDB success advisor landing page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/cmdb-sa-landing-page.md).

**Note:** The CMDB success advisor for SAM dashboard is available only after the setup process is complete. For more information, see [CMDB success advisor for SAM setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/software-asset-management/cmdb-sa-sam-config-settings.md).

## Required roles

|Role|Description|
|----|-----------|
|sam\_user|Required to view the SAM advisor dashboard in read-only mode.|
|sam\_admin|Required to select or edit the software products included in the SAM advisor scope.|
|sn\_cmdb\_admin|Provides administrative access to view and edit the scope for any CMDB success advisor product, including SAM.|
|sn\_cmdb\_user|Provides read-only access to CMDB success advisor pages and data.|

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

<table id="table_use_cases"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

CMDB administrator

</td><td>

-   Gain real-time visibility into software install data quality and completeness
-   Identify software installs missing edition, version, or cloud license details
-   Detect duplicate CIs with software installs and stale CI records
-   Verify that virtual server installs have accurate host CI relationships to support licensing compliance
-   Prioritize and track data cleanup and remediation tasks for software asset data
-   Verify that the CMDB stays accurate to support SAM

</td></tr></tbody>
</table>## Dashboard features

The dashboard provides clear, consolidated insights into software install data quality and CI accuracy. Use the dashboard to identify and resolve data quality issues within the CMDB through dedicated sub-tabs, filters, indicators, and visual reports.

Targeted CMDB metrics focus remediation efforts. Regularly monitor these metrics and follow suggested remediation actions to systematically improve CMDB data quality over time.

The dashboard header displays a **Last updated** timestamp reflecting the most recent completed run of the SAM data collector job.

**Important:** The dashboard data is filtered based on the Software publishers, Software products, CI class categories, and CI classes filters. See [Filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/software-asset-management/cmdb-sa-sam-dashboard.md).

|Sub-tab|Description|
|-------|-----------|
|[Installs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/software-asset-management/cmdb-sa-sam-dashboard.md)|Displays key metrics related to issues in software installation data that affect software inventory accuracy and licensing, limited to installs with a normalized product.|
|[Installed on](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/software-asset-management/cmdb-sa-sam-dashboard.md)|Displays key metrics related to CIs on which the selected software products are installed.|
|[Virtual CI relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/software-asset-management/cmdb-sa-sam-dashboard.md)|Displays key metrics related to CI relationships that connect virtual machine installs to their host infrastructure to support licensing compliance.|

## Filters

Filters enable narrowing the data shown in charts and metrics based on software publisher, software product, CI category, or CI class.

|Name|Type|Description|
|----|----|-----------|
|Software publishers|List|Filters data based on the selected software publishers.|
|Software products|List|Filters data based on the selected software products. Narrows to the software products available for the selected publishers.|
|CI class categories|List|Filters data based on CI category. Only available when the CMDB CI Class Models plugin \(sn\_data\_model\_nav\) is active and you have read access to CI class data.|
|CI classes|List|Filters data based on CI class. Only available if you have read access to CI class data.|

**Note:** Filters cascade: narrowing the Software publishers selection narrows the available Software products, CI class categories, and CI classes options.

## Installs

Displays key metrics related to issues in software installation data that affect software inventory accuracy and licensing, limited to installs with a normalized product.

\[Omitted image "cmdb-sa-sam-db-installs.png"\] Alt text: Installs sub-tab on SAM advisor dashboard.

|Card|Description|Indicators|
|----|-----------|----------|
|Software installs|Total number of software installs in scope, broken down by discovery source.|[Software installs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/software-asset-management/cmdb-sa-sam-dashboard-indicators.md)|
|Installs by|Breakdown of software installs by software publisher \(default\), software product, CI class, or latest integration source. Select an option from the drop-down list to change the breakdown.|[Installs by](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/software-asset-management/cmdb-sa-sam-dashboard-indicators.md)|
|Software installs by normalization status|Breakdown of software installs by normalization status.|[Software installs by normalization status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/software-asset-management/cmdb-sa-sam-dashboard-indicators.md)|
|Software installs missing edition|Software installs missing an edition value, affecting normalization and license reconciliation accuracy.|[Software installs missing edition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/software-asset-management/cmdb-sa-sam-dashboard-indicators.md)|
|Software installs missing version|Software installs missing a version value, affecting normalization and license reconciliation accuracy.|[Software installs missing version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/software-asset-management/cmdb-sa-sam-dashboard-indicators.md)|
|Server installs missing cloud license|Installs on servers with a cloud provider populated but no cloud license type, for a defined set of qualifying software products, affecting cloud license reporting accuracy.|[Server installs missing cloud license](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/software-asset-management/cmdb-sa-sam-dashboard-indicators.md)|

## Installed on

Displays key metrics related to CIs on which the selected software products are installed.

The **Installed on** sub-tab name reflects the **Installed on** field on the software installation record, which identifies the CI on which the software is installed. For more information, see [Software installation fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/software-asset-management/software-installation-fields.md).

\[Omitted image "cmdb-sa-sam-db-installedon.png"\] Alt text: Installed on sub-tab on SAM advisor dashboard.

<table id="table_uvg_rz5_zjc"><thead><tr><th>

Card

</th><th>

Description

</th><th>

Indicators

</th></tr></thead><tbody><tr><td>

Installs by CI install status

</td><td>

Breakdown of software installs by the install status, or life cycle stage, of the CI hosting the install.**Note:** On instances where the CSDM Activation plugin \(com.snc.cmdb.csdm.activation\) is active, this card is named **Installs by lifecycle stages** and installs are grouped by life cycle stage instead.

</td><td>

[Installs by CI install status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/software-asset-management/cmdb-sa-sam-dashboard-indicators.md)

</td></tr><tr><td>

CIs missing environment

</td><td>

CIs with a software install that are missing an environment value, leading to incomplete asset context.

</td><td>

[CIs missing environment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/software-asset-management/cmdb-sa-sam-dashboard-indicators.md)

</td></tr><tr><td>

CIs missing assigned to

</td><td>

CIs with a software install that aren't assigned to a specific user, leading to unclear ownership.

</td><td>

[CIs missing assigned to](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/software-asset-management/cmdb-sa-sam-dashboard-indicators.md)

</td></tr><tr><td>

Server CIs missing CPU attributes

</td><td>

CIs with a software install that are missing key CPU attributes needed for accurate license calculations.

</td><td>

[Server CIs missing CPU attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/software-asset-management/cmdb-sa-sam-dashboard-indicators.md)

</td></tr><tr><td>

CIs not updated

</td><td>

CIs with a software install that have not been updated within a selectable time period, causing data gaps and inaccuracies. Select 30, 60, or 90 days from the drop-down list to change the threshold.

</td><td>

[CIs not updated in the last 30 days](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/software-asset-management/cmdb-sa-sam-dashboard-indicators.md)[CIs not updated in the last 60 days](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/software-asset-management/cmdb-sa-sam-dashboard-indicators.md)

[CIs not updated in the last 90 days](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/software-asset-management/cmdb-sa-sam-dashboard-indicators.md)

</td></tr><tr><td>

Duplicate CIs

</td><td>

Software installs on CIs identified as duplicates, with an open de-duplication task, causing data redundancy.

</td><td>

[Duplicate CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/software-asset-management/cmdb-sa-sam-dashboard-indicators.md)

</td></tr></tbody>
</table>## Virtual CI relationships

Displays key metrics related to CI relationships that connect virtual machine installs to their host infrastructure. Accurate mappings enable licensing compliance.

**Note:** Run the **CMDB Health Dashboard - Relationship Compliance Processor** scheduled job to populate virtual machine host relationship data. If the job is inactive, the dashboard displays a `Relationship data incomplete` alert with a **Run job** action. The dashboard metrics update after the **CMDB Advisor - SAM Daily Data Collection** scheduled job runs. For more information, see [Components installed with CMDB success advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/cmdb-sa-components-installed.md) and [Scheduled jobs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/c_ScheduledJobs.md).

\[Omitted image "cmdb-sa-sam-db-virtual-reln.png"\] Alt text: Virtual CI relationships sub-tab on SAM advisor dashboard.

<table id="table_e4p_rz5_zjc"><thead><tr><th>

Card

</th><th>

Description

</th><th>

Indicators

</th></tr></thead><tbody><tr><td>

Virtual machines without host server CI relationships

</td><td>

Software installs on Windows Server or Linux Server virtual CIs that don't have a host server CI relationship, limited to VMware ESX Server and Microsoft Hyper-V virtual infrastructure, leading to gaps in licensing compliance tracking.

</td><td>

[Virtual machines without host server CI relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/software-asset-management/cmdb-sa-sam-dashboard-indicators.md)

</td></tr><tr><td>

Incorrect virtual server infrastructure relationships

</td><td>

Virtualized by or Member of relationships for virtual server CIs, limited to VMware ESX Server and Microsoft Hyper-V virtual infrastructure, that are flagged as incorrect or suggested for removal by relationship health analysis. On the KPI Details page, this indicator appears under the heading Incorrect infrastructure relationships.

</td><td>

[Incorrect virtual server infrastructure relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/software-asset-management/cmdb-sa-sam-dashboard-indicators.md)

</td></tr><tr><td>

Virtual CI-host CI install status distribution

</td><td>

Comparison of the install status, or life cycle stage, between a virtual server install and its related host CI.

</td><td>

[Install status distribution matched](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/software-asset-management/cmdb-sa-sam-dashboard-indicators.md)[Install status distribution mismatched](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/software-asset-management/cmdb-sa-sam-dashboard-indicators.md)

</td></tr></tbody>
</table>