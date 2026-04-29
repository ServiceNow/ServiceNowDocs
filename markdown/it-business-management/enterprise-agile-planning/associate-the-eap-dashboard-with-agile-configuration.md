---
title: Add EAP dashboards to an Agile configuration
description: Add dashboards to your Agile configuration so that product managers or scrum team members can access them from the Home tab of their Agile teams in Enterprise Agile Planning workspace.
locale: en-US
release: australia
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring custom dashboards in EAP, Configure, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Add EAP dashboards to an Agile configuration

Add dashboards to your Agile configuration so that product managers or scrum team members can access them from the Home tab of their Agile teams in Enterprise Agile Planning workspace.

## Before you begin

-   [Associate the EAP read-only role to the dashboard](add-the-eap-read-only-role-to-the-dashboard.md).
-   Set the Application Scope of your ServiceNow instance to Strategic Planning.

Role required: sn\_apw\_advanced.eap\_admin

## About this task

You can add single or multiple dashboards to your Agile configuration. If you are using a default configuration, a default dashboard is automatically associated with your Agile configuration. However, when you create a custom configuration, you must associate a dashboard with the configuration to view the metrics from selected data sources.

## Procedure

1.  Navigate to **sn\_apw\_advanced\_eap\_configuration\_detail.list**.

2.  Using the column options, group the records by Enterprise agile configuration.

3.  For your Agile configuration, select an Agile Team to view its details.

4.  From the **Home dashboards** field, add the dashboards that your team needs.

5.  Select **Update**.

    The selected dashboard or dashboards are added to the **Home** tab of the selected configuration.


