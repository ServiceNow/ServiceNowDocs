---
title: Configure a record overview dashboard
description: Add Platform Analytics reports to the Overview tab of a BCM record page. Only BCM admins can configure record overview dashboards. Reports added to an overview page are automatically pre-filtered to the current record and are visible in read-only mode to all users who can access that record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/conf-record-ov-db.html
release: australia
topic_type: task
last_updated: "2026-05-29"
reading_time_minutes: 1
breadcrumb: [Platform Analytics dashboards, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Configure a record overview dashboard

Add Platform Analytics reports to the Overview tab of a BCM record page. Only BCM admins can configure record overview dashboards. Reports added to an overview page are automatically pre-filtered to the current record and are visible in read-only mode to all users who can access that record.

## Before you begin

Role required: sn\_bcm.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace**.

2.  Open a record — for example, a crisis event — and select the **Overview** tab.

3.  Select **Add new element** and choose a visualization type.

4.  Select a data source — for example, Activated plan \[sn\_recov\_activated\_plan\].

5.  Select a metric — for example, Count.

6.  Configure grouping or additional filters.

7.  To save the customized dashboard, select **Save**.

    The report displays only the records that belong to the current record. For example, if 13 activated plans exist in the system but only 2 are linked to the current crisis event, the report shows 2. Selecting the visualization drills through to the filtered list of those records.

    Repeat these steps for each record type — Crisis events, Business Impact Analyses, and Plans — to add overview dashboards across all major BCM record pages.


