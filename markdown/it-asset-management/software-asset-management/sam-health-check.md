---
title: Software Asset Management health check
description: The Health Check ServiceNow Store application gives a correct and reliable overview of your Software Asset Management configurations and recommends you to correct any errors that may exist.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Software Asset Management health check

The Health Check ServiceNow Store application gives a correct and reliable overview of your Software Asset Management configurations and recommends you to correct any errors that may exist.

The Health Check application can be used by multiple personas such as implementation partners, SAM managers, and support analysts to determine the health check of their configurations.

Use the Health Check ServiceNow Store application at any point during the deployment of the Software Asset Management application to identify errors. For example, configuration errors such as incorrect setup of entitlements or software models, or missing data attributes found from Discovery. For details on running a health check scan, see [Run a health check scan for Software Asset Management](../task/run-healthcheck.md).

The current set of checks include checks for the following configurations:

-   SQL Server Config
-   SQL Server CMDB
-   Windows Server CMDB
-   Windows Server Config
-   Database Server - Oracle
-   Java - Oracle
-   Microsoft 365
-   General

The scheduled job, **SAM - Trigger Full Scan**, runs weekly on the KPI categories, shipped as part of the content service, on your ServiceNow instance. The KPI categories can be related to entitlement misconfiguration, downgrade, allocation, or any other configuration issue. You can configure these KPIs or even add more KPI categories. The scheduled job performs an overall health scan to check for any errors that may exist in your Software Asset Management configuration.

Notifications regarding the health checks can be viewed in the Software Asset overview view.

After the health scan is performed, view the results on the Health Check dashboard. View the results in the form of reports that you can download and those reports give recommendations on resolving the issues. For more information, see [Health check](health-check-dboard.md).

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

**Related topics**  


[Health check](health-check-dboard.md)

[Run a health check scan for Software Asset Management](../task/run-healthcheck.md)

