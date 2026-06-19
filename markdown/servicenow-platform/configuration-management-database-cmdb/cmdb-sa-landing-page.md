---
title: Viewing the CMDB success advisor landing page
description: As a CMDB administrator, you can use the CMDB success advisor landing page to configure and manage data quality dashboards for Data Foundations and Hardware Asset Management \(HAM\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-landing-page.html
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-06-09"
reading_time_minutes: 4
breadcrumb: [CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Viewing the CMDB success advisor landing page

As a CMDB administrator, you can use the CMDB success advisor landing page to configure and manage data quality dashboards for Data Foundations and Hardware Asset Management \(HAM\).

The CMDB success advisor landing page opens when you select CMDB success advisor in CMDB Workspace or in Service Graph Workspace.

\[Omitted image "cmdb-sa-landing-page.png"\] Alt text: Landing page of CMDB success advisor.

## Roles required

You must have the sn\_cmdb\_admin role to access the CMDB success advisor landing page.

**Note:** Users with the sn\_cmdb\_user or sn\_cmdb\_editor role can access CMDB success advisor from the Insights view in Service Graph Workspace v9.1 and view the Dashboard tab only. The Settings and Integrations tabs aren't available to these users.

## Accessing and using the landing page

To access the CMDB success advisor landing page, use the following navigation paths.

<table id="table_ez2_jqs_k3c"><thead><tr><th>

Entry point

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

Product highlights in CMDB Workspace

</td><td>

Navigate to **Workspaces** &gt; **CMDB Workspace**. In the Home view, select the CMDB success advisor card in the Product highlights section.

</td></tr><tr><td>

Management view in CMDB Workspace

</td><td>

In the Management view, select the **CMDB success advisor** link in the Optimize view under Management tools.

</td></tr><tr><td>

Insights view in Service Graph Workspace

</td><td>

Navigate to Service Graph Workspace. In the Insights view, select the CMDB success advisor card.**Tip:** Users with the cmdb\_user or cmdb\_editor role can access CMDB success advisor from this entry point and view the Dashboard tab only.

</td></tr><tr><td>

Service Graph Workspace

</td><td>

Navigate to Service Graph Workspace. In the navigation panel, select the **Governance** icon. In the Governance view, select **Get started** \(first visit\) or **View details** \(subsequent visits\).

</td></tr></tbody>
</table>**Tip:** On first access, select **Get started** in the Get started with CMDB success advisor dialog box, then select **Continue**. Select **Don't show again** to skip the dialog box on future visits.

## Viewing data

From the landing page, you can:

-   View and configure the scope for Data Foundations and application-specific advisors including HAM.
-   Open a product dashboard to review data quality KPIs and trends.
-   Follow guided steps to define scope, identify issues, and drive CMDB outcomes.
-   Access resources and FAQs for additional guidance.

## Advisor cards

The landing page organizes advisors into the following sections:

-   **Data Foundations**

    Central hub for managing and improving foundational CMDB data quality. Gain a unified view of key CMDB data and foundational data quality that drives business outcomes.

    Select **Set principal classes** to configure your Data Foundations advisor scope for the first time. Select **View insights** to open the Data Foundations advisor dashboard. To update the scope after initial setup, select **Manage principal classes** on the Data Foundations advisor dashboard.

    Use Data Foundations to keep your CI data accurate, complete, and reliable for processes such as incidents, problems, and changes. Select the CI classes that matter most to your organization. The selected classes are automatically marked as principal classes, which filters CI picker fields on task records to show only the most relevant items. The default configuration enables you to select up to 200 principal classes.

-   **Application-specific**

    Focused guidance for targeted business use cases. This section contains advisors for specific installed applications. The advisors need the corresponding application to be installed and entitled to work. Currently includes:

    -   **Hardware Asset Management \(HAM\)**

        Build trust in asset life cycle data with a healthier CMDB that drives HAM outcomes like improved normalization, compliance, and cost efficiency. Select **Select model categories** to configure your HAM advisor scope for the first time. Select **View insights** to open the HAM advisor dashboard. To update the scope after initial setup, select **Edit model categories** on the HAM advisor dashboard.


## Right panel

The right panel of the landing page provides additional context and links to enable you to get started and learn more.

-   **Take action with CMDB success advisor**

    A guided three-step process to help you define scope, identify data issues, and drive measurable CMDB outcomes.

-   **Resources**

    Links to related documentation including guidance on principal classes, product documentation, asset and CI mapping guidelines, and the community forum.

-   **FAQs**

    Expandable answers to common questions about using CMDB success advisor, defining scope, aligning rules and policies, and remediating data quality issues.


## Advisor card states

Each advisor card shows action buttons that reflect its current state. Cards for application-specific advisors may also show a badge when the required app is not available.

|State|Description|Action|
|-----|-----------|------|
|Shows **Set principal classes** or **Select model categories**|The advisor is available but scope has not been configured yet.|Select **Set principal classes** or **Select model categories** to define the scope and set up the advisor dashboard.|
|Shows **View insights**|The advisor is configured and the dashboard is available.|Select **View insights** to open the dashboard. To update the scope, use **Manage principal classes** on the Data Foundations advisor dashboard or **Edit model categories** on the HAM advisor dashboard.|
|Needs installation|The app is entitled on your instance but has not been installed.|Select **Learn more** to install the app and gain insights with CMDB success advisor.|
|Needs entitlement|The app has not been entitled on your instance.|Select **Learn more** to request an entitlement and gain insights with CMDB success advisor.|

