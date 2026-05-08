---
title: CSM Landing Page - Premium
description: The CSM Landing Page - Premium provides users with lists of assigned cases and case tasks as well as agent, group, and organization metrics.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Landing pages, CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# CSM Landing Page - Premium

The CSM Landing Page - Premium provides users with lists of assigned cases and case tasks as well as agent, group, and organization metrics.

Customer service agents and managers can use the CSM Landing Page - Premium to quickly scan and prioritize work, access records, and track performance. Administrators can customize landing pages in UI Builder to meet their unique business needs.

The CSM Landing Page - Premium includes components that display case information, plus visualizations that further break down the component data. For example, the **High priority cases** component includes visualizations for P1 and escalated cases, plus cases that need attention. It also includes additional indicators and visualizations in the **Performance** and **Organization's Performance** sections. Each of the visualizations is connected to a data source.

The CSM Landing Page - Premium is available with the following plugins:

-   CSM Configurable Workspace \(sn\_csm\_wrkspc\)
-   Performance Analytics - Content Pack - Customer Service Management - Advanced \(com.snc.pa.customer\_service\_advanced\)

**Note:** Upgrade customers who haven’t customized the existing CSM Configurable Workspace landing page are automatically upgraded to the landing page available with the Australia release. Upgrade customers who have customized the existing CSM Configurable Workspace landing page must manually accept the Australia landing page.

![Landing page to track your active cases and important items. For the text description, refer to the CSM Landing Page and CSM Landing Page - Premium sections and components table.](../image/csm-config-ws-polaris-case-section.png "CSM landing page - Assigned cases and case tasks")

![Landing page with agent and organization performance data. For the text description, refer to the CSM Landing Page and CSM Landing Page - Premium sections and components table that follows.](../image/csm-config-ws-polaris-performance-section.png "CSM landing page - Performance metrics")

## CSM Landing Page - Premium sections and components

The CSM Landing Page includes different sections and components that display important items, record lists, and performance data.

<table id="table_j5g_b4d_gsb"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Important Items

</td><td>

This section includes single score cards that display an agent's most important items to work on. -   **High priority cases**: Includes P1 cases, escalated cases, and cases that need attention.
-   **SLA breached or due today**
-   **Cases not updated in &gt;3d**
-   **Case tasks**
-   **Unassigned cases**: Cases that are unassigned and belong to one of the agent's assignment groups.

Selecting a score card displays a list of records with the appropriate filter conditions.

</td></tr><tr><td>

Cases

</td><td>

This section includes two lists of records:-   **My active cases**
-   **My team's cases**

Selecting a case number opens a new tab and displays the case record.

</td></tr><tr><td>

Performance

</td><td>

This section includes indicators that track the agent's performance.

-   **Met SLA \(last 7 days\)**
-   **Reopened cases \(last 30 days\)**

 The following indicators are available in the Performance section with activation of the Performance Analytics - Content Pack - Customer Service Management - Advanced plugin:

 -   **CSAT**: Customer satisfaction score based on cases assigned to the agent for the last 7 days.
-   **Response time**
-   **Resolution time**

Select an indicator to display either a filtered list of records or a KPI details page.

</td></tr><tr><td>

Organization's Performance

</td><td>

This section includes indicators that track the organization's performance. -   **CSAT**: Customer satisfaction score for the last 7 days.
-   **New vs closed cases**: Daily aggregation of new and closed cases for the last 7 days.

Select an indicator to view a KPI details page.**Note:** This section is available for the CSM Landing Page - Premium, which requires activation of the Performance Analytics - Content Pack - Customer Service Management - Advanced plugin.

</td></tr></tbody>
</table>## Create a landing page for CSM Configurable Workspace

Use UI Builder to create landing pages for your agents. For more information, see [Create a CSM Configurable Workspace landing page](../task/config-csm-config-ws-landing-page.md).

## Create multiple landing pages

You can create multiple landing pages. However, only a single landing page is displayed for a user. The landing page that is displayed for you depends on the following settings:

-   The setting of the **Active** field. This field must be set to true for a landing page to be displayed.
-   The **Order** of the landing page. Pages with a lower-order value take precedence over pages with a higher-order value.
-   If permissions are defined, you can see a landing page if you have the required role or are a member of the required assignment group. Multiple roles and assignment group conditions are treated as OR conditions.

