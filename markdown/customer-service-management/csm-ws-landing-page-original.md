---
title: CSM landing page
description: Use the CSM landing page to view assigned cases, case tasks, and agent, group, and organization metrics.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/csm-ws-landing-page-original.html
release: australia
topic_type: concept
last_updated: "2026-10-22"
reading_time_minutes: 3
breadcrumb: [Landing pages, CRM Workspace features, CRM Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# CSM landing page

Use the CSM landing page to view assigned cases, case tasks, and agent, group, and organization metrics.

Customer service agents and managers can use the CSM landing page to quickly scan and prioritize work, access records, and track performance. Administrators can customize landing pages in [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/using-ui-builder.md) to meet their unique business needs.

The CSM landing page includes components that display case information, plus visualizations that further break down the component data. Each of the visualizations is connected to a data source. For example, the **High priority cases** component includes visualizations for P1 and escalated cases, plus cases that need attention.

**Warning:** To confirm the High priority cases component filters correctly, activate the Customer Service Case Action Status \(com.snc.csm\_action\_status\) plugin. This plugin adds the missing **action\_status** field, which isn't included with the CSM plugin by default. Also, ensure your instance is on Xanadu Patch 7 or later.

The CSM landing page is available with the CRM Workspace plugin \(com.snc.uib.csm\_agent\_workspace\). This landing page is the default landing page for CRM Workspace.

**Note:** Upgrade customers who haven't customized the existing CRM Workspace landing page are automatically upgraded to the landing page available with the Brazil release. Upgrade customers who have customized the existing CRM Workspace landing page must manually accept the Brazil landing page.

\[Omitted image "csm-config-ws-polaris-case-section.png"\] Alt text: Landing page showing active cases and important items. For a text description, see the CSM landing page sections and components table.

## CSM landing page sections and components

The CSM landing page includes different sections and components that display important items, record lists, and performance data.

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
-   **Response time**: Average time to respond to cases assigned to the agent for the last 7 days.
-   **Resolution time**: Average time to resolve cases assigned to the agent for the last 7 days.

Selecting an indicator displays either a filtered list of records or a KPI details page.

</td></tr></tbody>
</table>## Create a landing page for CRM Workspace

UI Builder enables you to create landing pages for your agents. For more information, see [Create a CRM Workspace landing page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/config-csm-config-ws-landing-page.md).

## Create multiple landing pages

You can create multiple landing pages. However, only a single landing page is displayed for a user. The landing page that is displayed depends on the following settings:

-   The setting of the **Active** field. This field must be set to true for a landing page to be displayed.
-   The **Order** of the landing page. Pages with a lower-order value take precedence over pages with a higher-order value. The active page with the lowest order number is displayed.
-   If permissions are defined, users can see a landing page if they have the required role or are a member of the required assignment group. Multiple roles and assignment group conditions are treated as OR conditions.

