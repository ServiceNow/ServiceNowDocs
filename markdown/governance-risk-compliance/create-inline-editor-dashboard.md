---
title: Create an inline-editor dashboard
description: Duplicate and customize the base system BCM dashboard to create a personalized homepage view. The inline editor lets any BCM user build a dashboard without technical knowledge. You can start from scratch or duplicate the delivered base system dashboard.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/create-inline-editor-dashboard.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Platform Analytics dashboards, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create an inline-editor dashboard

Duplicate and customize the base system BCM dashboard to create a personalized homepage view. The inline editor lets any BCM user build a dashboard without technical knowledge. You can start from scratch or duplicate the delivered base system dashboard.

## Before you begin

Role required: sn\_bcm.manager, sn\_bcm.user

## About this task

You can create an inline-editor dashboard from scratch, or duplicate the **Business continuity management dashboard** as part of the base system and edit the copy. Duplicating is recommended when you want to preserve the default My items and My actions cards, which you can then extend with additional visualizations.

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace**.

2.  On the homepage, open the dashboard drop-down and select **Create a new dashboard**, or select the base system Business continuity management dashboard and choose **Duplicate**.

    1.  In the Duplicating dashboard dialog, enter a name for the new dashboard — for example, Manager dashboard — and select **Duplicate**.

    \[Omitted image "duplicate-dashboard-dialog.jpg"\] Alt text: Duplicating dashboard dialog with the New name field pre-populated as "Business continuity management dashboard - Copy".

3.  Open the new dashboard and select **Edit**.

4.  To add a report, select **Add new element** and choose a visualization type.

    You can select a visualization type such as a pie chart.

5.  Select a data source.

    You can select a data source such as an event \[sn\_recovery\_event\] to report on crisis events.

    \[Omitted image "add-pie-chart-report.jpg"\] Alt text: Add data source panel showing the Event table selected as the data source for a new visualization.

6.  Apply conditions to filter the data to show only events of a specific type.

7.  Select a metric and a **Group by** field — for example, group by Type to see a breakdown of event types.

    You can add the following components:

    -   Saved data visualizations
    -   New charts
    -   Lists
    -   Filters
    -   Images
    -   Headings
8.  Configure the dashboard settings to control permissions and sharing.

    The dashboard is in the Business Continuity Workspace dashboard picker based on the permissions you set.

9.  To set the new dashboard as your homepage, select it from the dashboard drop-down.

10. To save the dashboard, select **Save**.


## Result

You created an inline-editor dashboard that can be shared across pages and workspaces. The dashboard is personalized per user. Other users logging in to the workspace see their own dashboard selection and are not affected by your changes.

**Related topics**  


[Configure a record overview dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/conf-record-ov-db.md)

