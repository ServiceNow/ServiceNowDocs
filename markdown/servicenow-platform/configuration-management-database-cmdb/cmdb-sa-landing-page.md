---
title: Viewing the CMDB success advisor landing page
description: As a CMDB administrator, you can use the CMDB success advisor landing page to configure and manage data quality dashboards for Data Foundations and Hardware Asset Management \(HAM\).
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-02-26"
reading_time_minutes: 3
breadcrumb: [CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Viewing the CMDB success advisor landing page

As a CMDB administrator, you can use the CMDB success advisor landing page to configure and manage data quality dashboards for Data Foundations and Hardware Asset Management \(HAM\).

The CMDB success advisor landing page opens when you select CMDB success advisor from the Product highlights section in the Home view of CMDB Workspace, the Management view in CMDB Workspace, or the Data Governance tab in Service Graph Workspace.

![Landing page of CMDB success advisor.](../image/cmdb-sa-landing-page.png "CMDB success advisor landing page")

## Role required

You must have the sn\_cmdb\_admin role to access the CMDB success advisor landing page.

## Accessing and using the landing page

To access the CMDB success advisor landing page, use the following navigation paths.

|Entry point|Steps|
|-----------|-----|
|Product highlights in CMDB Workspace|Navigate to **Workspaces** &gt; **CMDB Workspace**. In the Home view, select the CMDB success advisor card in the Product highlights section.|
|Management view in CMDB Workspace|In the Management view, select the **CMDB success advisor** link in the Optimize view under Management tools.|
|Service Graph Workspace|Navigate to Service Graph Workspace. In the Data Governance view, select **Get started** \(first visit\) or **View details** \(subsequent visits\).|

**Tip:** On first access, select **Get started** in the Get started with CMDB success advisor dialog box, then select **Continue**. Select **Don't show again** to skip the dialog box on future visits.

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

    Select **Select principal classes** to configure your Data Foundations advisor scope for the first time or **Edit principal classes** to update an existing scope. Select **View insights** to open the Data Foundations advisor dashboard. You can select up to 50 principal classes.

    Use Data Foundations to keep your CI data accurate, complete, and reliable for processes such as incidents, problems, and changes. Select the CI classes that matter most to your organization. The selected classes are automatically marked as principal classes, which filters CI picker fields on task records to show only the most relevant items. You can select up to 50 principal classes.

-   **Application-specific**

    Focused guidance for targeted business use cases. This section contains advisors for specific installed applications. The advisors need the corresponding application to be installed and entitled to work. Currently includes:

    -   **Hardware Asset Management \(HAM\)**

        Build trust in asset life cycle data with a healthier CMDB that drives HAM outcomes like improved normalization, compliance, and cost efficiency. Select **Select model categories** to configure your HAM advisor scope for the first time or **Edit model categories** to update an existing scope. Select **View insights** to open the HAM advisor dashboard. You can select up to 50 hardware model categories.


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
|Shows **Select principal classes** or **Select model categories**|The advisor is available but scope has not been configured yet.|Select **Select principal classes** or **Select model categories** to define the scope and set up the advisor dashboard.|
|Shows **Edit principal classes** or **Edit model categories** and **View insights**|The advisor is configured and the dashboard is available.|Select **Edit principal classes** or **Edit model categories** to update scope, or **View insights** to open the dashboard.|
|Needs installation|The app is entitled on your instance but has not been installed.|Select **Learn more** to install the app and gain insights with CMDB success advisor.|
|Needs entitlement|The app has not been entitled on your instance.|Select **Learn more** to request an entitlement and gain insights with CMDB success advisor.|

