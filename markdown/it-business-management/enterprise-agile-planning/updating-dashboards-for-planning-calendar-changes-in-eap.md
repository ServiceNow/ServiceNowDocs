---
title: Updating dashboards for planning calendar changes in EAP
description: Update the EAP dashboard configuration whenever there are changes to the planning calendar for any currently active configurations in Enterprise Agile Planning.
locale: en-US
release: zurich
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring custom dashboards in EAP, Configure, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Updating dashboards for planning calendar changes in EAP

Update the EAP dashboard configuration whenever there are changes to the planning calendar for any currently active configurations in Enterprise Agile Planning.

When your product managers update the planning calendars for an EAP configuration with active teams and work items, the reports on the Home tab for those teams are affected. As an admin, you must update the corresponding dashboards for this EAP configuration. This action ensures that the reports and metrics your teams see are accurate.

For example, the Agile Team's Planning Calendar value is updated from **Sprint** to **None** for a Full Configuration. Then, the Home tab should no longer display sprint-related reports such as Burnup or Burndown charts, Sprint velocity, and others.

![Planning calendar changes for a Full configuration in EAP workspace.](../images/eap-planning-calendar-update.png)

To ensure this change, you must configure new dashboards according to the latest planning calendar and replace the existing Agile Team dashboards of the Full Configuration with the new ones.

![Updating Home dashboards for an EAP configuration.](../images/eap-dashboard-update-config-detail.png)

This procedure involves a series of tasks as listed here:

1.  For the latest planning calendar, create a dashboard or duplicate the existing dashboard and add the reports that your teams want to have. See [Create a dashboard in EAP](../task/create-a-dashboard-in-eap.md).
2.  [Add a tag to the EAP dashboard](../task/add-tag-to-the-eap-dashboard.md).
3.  [Associate the EAP read-only role to the dashboard](../task/add-the-eap-read-only-role-to-the-dashboard.md).
4.  Add the newly created dashboard to the EAP configuration that has the planning calendar change. See [Add EAP dashboards to an Agile configuration](../task/associate-the-eap-dashboard-with-agile-configuration.md).
5.  \(Optional\) [Create implementation of a Scripted Extension Point in EAP](../task/create-or-update-scripted-extension-point-in-eap.md).

