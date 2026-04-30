---
title: Associate the EAP read-only role to the dashboard
description: Associate the EAP read-only \(sn\_apw\_advanced.eap\_read\_only\) role to the dashboard. The users with this role can view and edit the dashboard for the teams in their Agile configuration.
locale: en-US
release: xanadu
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring custom dashboards in EAP, Configure, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Associate the EAP read-only role to the dashboard

Associate the EAP read-only \(sn\_apw\_advanced.eap\_read\_only\) role to the dashboard. The users with this role can view and edit the dashboard for the teams in their Agile configuration.

## Before you begin

-   [Add a tag to the EAP dashboard](add-tag-to-the-eap-dashboard.md).

-   Set the Application Scope of your ServiceNow instance to Strategic Planning.

Role required: sn\_apw\_advanced.eap\_admin or admin

## Procedure

1.  Navigate to the PAR Dashboard Permissions \[par\_dashboard\_permission\] table.

2.  Locate the dashboard that you created.

3.  Double-click a cell in the Role column and then enter **sn\_apw\_advanced.eap\_read\_only**.

4.  Select **Save**.

    The role is associated with the dashboard.


## What to do next

[Add EAP dashboards to an Agile configuration](associate-the-eap-dashboard-with-agile-configuration.md).

