---
title: Platform Analytics dashboards
description: Platform Analytics dashboards provide Business Continuity Workspace users with a configurable summary of their work items and actions. Unlike Workspace pages built with the UI Builder, most users can set up or customize Platform Analytics dashboards without writing code or configuring UI components.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/pa-dashboard-summary.html
release: australia
topic_type: concept
last_updated: "2026-06-05"
reading_time_minutes: 2
keywords: [Platform Analytics dashboard, BCM dashboard, create dashboard, customize dashboard, home page dashboard, record overview dashboard]
breadcrumb: [Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Platform Analytics dashboards

Platform Analytics dashboards provide Business Continuity Workspace users with a configurable summary of their work items and actions. Unlike Workspace pages built with the UI Builder, most users can set up or customize Platform Analytics dashboards without writing code or configuring UI components.

Platform Analytics dashboards are versatile tools for data analysis and presentation. Starting with the Australia release of the BCM application, BCM administrators and users can create, edit, read, delete, and duplicate Platform Analytics dashboards. BCM administrators have full dashboard management access. All other users can read default dashboards, create new dashboards, and duplicate dashboards they can access.

## Platform Analytics dashboards: Home page and record overview pages

Platform Analytics dashboards are displayed in the Business Continuity Workspace.

-   **Home page**

    The Business Continuity Workspace home page displays a Platform Analytics dashboard as the default landing page. The base system dashboard is personalized for each user and shows the following sections:

    -   My items — Lists the Business impact analysis, Plans, Exercises, and Crisis events assigned to the signed-in user.
    -   My actions — Lists the Event tasks, Action items, Pending reviews, and Pending approvals assigned to the user as shown in the following example.
    \[Omitted image "custom-manager-dashboard.jpg"\] Alt text: Manager dashboard in edit mode showing the base system My items and My actions cards, alongside a new pie chart that groups all exercises by Event type.

    As a user of the Business Continuity Workspace, you can duplicate the default dashboard, rename it, and add your own reports and visualizations without affecting other users. The dashboard menu on the home page lets you switch between the default dashboard and any dashboards that you have created.

    **Note:** The base system dashboard is read-only and must be duplicated before editing.

    The dashboard is personalized for each signed-in BCM user; When you create a dashboard from the drop-down menu, it is visible only to you.

    \[Omitted image "bcm-manager-homepage-dashboard.jpg"\] Alt text: Business continuity management dashboard shown as the home page for a BCM Manager, with My items and My actions sections.

-   **Record overview pages**

    A Platform Analytics dashboard is also embedded in the **Overview** tab of the major BCM record pages: Crisis events, Business impact analysis, and Plans.

    Record page dashboards don't include base system visualizations by default, unlike the home page dashboard — BCM administrators add reports to each overview page. Only BCM administrators can edit record page dashboards; all other users can read them.

    Record page dashboards are different from the home page dashboards:

    -   Edited by administrators only: Only BCM administrators \(sn\_bcm.admin\) can add or modify reports on record page dashboards. Other users cannot duplicate or edit a record page dashboard.
    -   Pre-filtered to the current record: Each report on a record page dashboard is scoped to the record that is open.

        Selecting a pre-filtered visualization opens the underlying records. For example, selecting the activated-plan count on a Crisis event overview opens the list of activated plans that belong to that event only.


**Related topics**  


[Create an inline-editor dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-inline-editor-dashboard.md)

[Configure a record overview dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/conf-record-ov-db.md)

