---
title: Populate the homepage migration status table for multiple domains
description: By default, the flow to populate the homepage migration status table applies only to the global domain. You can create a flow to apply to the other domains in your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/performance-analytics/populate-hp-migration-status-table-multi-domains.html
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Homepage migration status table, Homepage deprecation, Administering dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Populate the homepage migration status table for multiple domains

By default, the flow to populate the homepage migration status table applies only to the global domain. You can create a flow to apply to the other domains in your instance.

## Before you begin

Role required: admin

## Procedure

1.  Use the domain picker to select a domain scope.

    \[Omitted image "domain-scope-picker.png"\] Alt text: Domain picker with Domain scope: ACME selected

2.  Navigate to **All** &gt; **Flow Designer**.

3.  Find the Populate Homepage migration status table flow and open it.

    \[Omitted image "populate-hpmst-flow.png"\] Alt text: Flow designer list of flows that contain the name Populate Homepage migration status table

4.  Select the **More Actions** menu and choose **Copy Flow**.

    \[Omitted image "flow-designer-copy-flow.png"\] Alt text: Flow designer More Actions menu with the Copy flow option highlighted.

5.  Select the application `Homepage deprecation help tool` and select **Copy**.

6.  Select the **More Actions** menu and choose **Flow properties**.

    The flow points to the selected domain scope.

    \[Omitted image "flow-designer-sub-domain-properties.png"\] Alt text: Properties of the copied homepage migration status table flow pointing to the selected domain


