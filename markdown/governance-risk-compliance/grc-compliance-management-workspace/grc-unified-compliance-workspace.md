---
title: GRC Compliance Workspace
description: Compliance Workspace is a unified interface where you can manage all your tasks related to policies, control objectives, controls, and policy exceptions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-compliance-management-workspace/grc-unified-compliance-workspace.html
release: australia
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [GRC Compliance workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# GRC Compliance Workspace

Compliance Workspace is a unified interface where you can manage all your tasks related to policies, control objectives, controls, and policy exceptions.

## Compliance Workspace overview

The highlights of the Compliance Workspace are:

-   **Reimagined user experience**

    From the minute you navigate to the Compliance Workspace home page, all the tasks that you can possibly do in the workspace are streamlined to fulfill your business goals.

-   **Workspace designed for different compliance user roles**

    Distinct page views for the exclusive activities of a Corporate compliance manager, Corporate compliance analyst, and IT compliance manager.

-   **Home page with different sections**

    -   **Overview**

        Donut charts display the categorical data of compliant and non-compliant authority documents, policies, and entities.

        \[Omitted image "ComplianceWSHomePage.png"\] Alt text: Compliance workspace home page.

    -   **Control assurance**

        Displays the donut charts, grouping indicators by status, and attestations by state. Control test horizontal bar grouped by control and classification stacked by control effectiveness.

    -   **Tracking**

        Displays controls widget grouped by state and stacked by classification.

    -   **Tasks**

        View your pending tasks and the group's tasks. You can navigate to the unified tasks page by clicking the **View all tasks** link.

    **Note:** Control tests widget, Regulatory change, Compliance case, and Privacy widgets are conditionally visible based on the respective plugins installation status.

-   **Unified Tasks page**

    Track your tasks and team's tasks from a single interface. View your tasks by categories, filter them by various parameters, monitor those tasks that you've initiated, and track through the watchlist.

-   **Lists**

    List view of all compliance-related records, providing the summary of the record in a single view that helps in your analyses and take an informed decision.


**Note:** The **Control tests** widget, **Regulatory changes** widget, and **Domain compliance status** section appear with the installation of audit, regulatory change management, and privacy management plugins, respectively. For more information, see [Other GRC plugins for an overall view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-compliance-management-workspace/compliance-manager-compliance-ws.md).

## Roles in the Compliance Workspace

The targeted users of the Compliance Workspace are the corporate compliance managers, the corporate IT compliance managers, and the corporate compliance analysts.

To access or view the Compliance Workspace, you need one of the following roles:

-   IT Compliance Manager role: sn\_compliance\_ws.it\_compliance\_manager
-   Corporate Compliance Manager role: sn\_compliance\_ws.corporate\_compliance\_manager
-   Corporate Compliance Analyst role: sn\_compliance\_ws.corporate\_compliance\_analyst

For more information on the roles, the responsibilities, and the tasks that the users can accomplish in the Compliance Workspace, see

-   [Compliance Home page for the compliance manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-compliance-management-workspace/compliance-manager-compliance-ws.md).
-   [Compliance Home page for the compliance analyst](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-compliance-management-workspace/compliance-analyst-compliance-ws.md).
-   [Compliance Home page for the IT compliance manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-compliance-management-workspace/it-compliance-manager-compliance-ws.md).

## Email notification redirection

When users receive email notifications for Policy and Compliance Management records, clicking a record link in the notification opens the record in the appropriate workspace, based on the user's assigned roles and installed workspace applications.

The following record types support workspace redirection from email notifications:

-   Controls
-   Evidence response
-   Indicator tasks
-   Policy acknowledgments/Policy acknowledgment instances
-   Policy exceptions

This table shows the Policy and Compliance user roles that redirect to GRC Task page or Compliance Workspace:

|User role|Redirected to|
|---------|-------------|
|BU User|GRC Task page|
|Compliance Manager|GRC Task page|
|Corporate Compliance Manager|Compliance Workspace|
|Corporate Compliance Analyst|Compliance Workspace|
|Approver \(policy exception\)|Compliance Workspace|
|Approver|GRC Task Page|

In addition, if a user has roles associated with other workspaces such as Risk, Privacy, Audit, CAM, or AI Risk and Compliance, the system redirects to the highest-priority workspace based on the role.

The priority order is as follows:

-   Risk Workspace
-   Privacy Workspace
-   AI Risk and Compliance Workspace
-   Audit Workspace
-   CAM Workspace

If no workspace role is assigned and the common workspace is installed, the user is redirected to the GRC Task Page. If the common workspace is not installed, the user is redirected to the classic UI.

