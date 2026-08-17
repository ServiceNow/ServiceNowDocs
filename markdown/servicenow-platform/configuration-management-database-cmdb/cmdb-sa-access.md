---
title: Access CMDB success advisor
description: You can access CMDB success advisor from the Service Graph Workspace, CMDB Workspace, or Software Asset Workspace to set up and manage application-specific dashboards. Depending on your progress, you can either begin the setup or access the dashboard to monitor and manage targeted configuration items \(CIs\) for an application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-access.html
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-08-04"
reading_time_minutes: 3
keywords: [Access CMDB success advisor, CMDB success advisor entry points, Service Graph Workspace Governance view, CMDB workspace Management view, Get started dialog box, dashboard access roles]
breadcrumb: [CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Access CMDB success advisor

You can access CMDB success advisor from the Service Graph Workspace, CMDB Workspace, or Software Asset Workspace to set up and manage application-specific dashboards. Depending on your progress, you can either begin the setup or access the dashboard to monitor and manage targeted configuration items \(CIs\) for an application.

## Before you begin

**Important:** CMDB success advisor \(sn\_cmdb\_advisor\) is a Next Experience application. It requires CMDB Workspace \(sn\_cmdb\_ws\) and SGC Central \(sn\_sgc\_central\) to be installed on your instance. If the application is not visible, contact your administrator to confirm these dependencies are installed and that you have the sn\_cmdb\_admin role.

CMDB success advisor supports Data Foundations, Hardware Asset Management \(HAM\), and Software Asset Management \(SAM\).

Role access varies by entry point:

-   Users with the sn\_cmdb\_user or sn\_cmdb\_editor role can access CMDB success advisor from the Insights view in Service Graph Workspace and view the Dashboard tab only.
-   Users with the sn\_cmdb\_admin role can access CMDB success advisor from the CMDB Workspace with full access.
-   Users with the sam\_user, sam\_admin, or sn\_cmdb\_admin role can access the CMDB success advisor for SAM advisor dashboard from the Software Asset Workspace.

Role required: sn\_cmdb\_admin for full access to CMDB success advisor for HAM, CMDB success advisor for Data Foundations, and CMDB success advisor for SAM.

## About this task

You can access the CMDB success advisor app from Service Graph Workspace and CMDB Workspace.

## Procedure

-   From the Service Graph Workspace:

    1.  Navigate to Service Graph Workspace.

        To learn more on how to set up Service Graph Workspace, see [Set up Service Graph Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/setup-service-graph-workspace.md).

    2.  In the navigation panel, select the **Governance** icon.

    3.  Locate CMDB success advisor from either of these locations in the Governance view.

        -   In the Product highlights section, select the CMDB success advisor card.
        -   In the Management tools section, under Optimize, select the CMDB success advisor link.
    4.  Select an action based on your progress.

        -   On first access, select **Get started**, and then in the Get started with CMDB success advisor dialog box, select **Continue**.

            **Tip:** Select the **Don't show again** check box to skip the dialog box in the future.

        -   On subsequent visits, select **View details**.
-   From the Insights view in Service Graph Workspace:

    1.  Navigate to Service Graph Workspace.

    2.  In the Insights view, select the CMDB success advisor card.

        **Tip:** Users with the sn\_cmdb\_user or sn\_cmdb\_editor role can access CMDB success advisor from this entry point and view the Dashboard tab only.

-   From the [CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-workspace.md):

    1.  Navigate to **Workspaces** &gt; **CMDB Workspace**.

    2.  Locate the CMDB success advisor application.

        -   In the Home view, select the CMDB success advisor card available within the Product highlights section.
        -   In the Management view, select the CMDB success advisor link, available within the Optimize category in the Management tools section.
    3.  Select an action based on your progress.

        -   On first access, select **Get started**, and then in the Get started with CMDB success advisor dialog box, select **Continue**.

            **Tip:** Select the **Don't show again** check box to skip the dialog box in the future.

        -   On subsequent visits, select **View details**.
-   From the Software Asset Workspace in SAM:

    1.  Navigate to **Workspaces** &gt; **Software Asset Workspace**.

        **Note:** This entry point is available only when the Software Asset Workspace plugin \(com.sn\_sam\_workspace\) is installed on your instance.

    2.  On the Software asset overview page, under Notifications in the Activity center, select **Review CMDB data quality**.

        -   If the SAM advisor scope is already configured, the CMDB success advisor for SAM advisor dashboard opens directly for users with the sam\_user, sam\_admin, or sn\_cmdb\_admin role.
        -   If the SAM advisor scope isn't configured yet, users with the sam\_admin or sn\_cmdb\_admin role can select software products in the **Edit dashboard scope** dialog box instead. The **Review CMDB data quality** notification doesn't appear for users with the sam\_user role until the scope is configured.

## Result

The CMDB success advisor landing page opens, displaying product cards for Data Foundations and application-specific modules like HAM and SAM. Each card includes a brief description and actions to configure dashboards and review data quality insights and metrics.

If you access CMDB success advisor from the Software Asset Workspace after the SAM advisor scope is configured, the SAM advisor dashboard opens directly instead of the landing page.

