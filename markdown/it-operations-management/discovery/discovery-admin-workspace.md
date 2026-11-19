---
title: Discovery Admin Workspace
description: The Discovery Admin Workspace serves as a central location for monitoring, tracking, and completing discovery-related tasks. Experience a streamlined discovery process and greater efficiency with the integration of schedules, diagnostics, tuning, anomaly detection, and more within this single workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-operations-management/discovery/discovery-admin-workspace.html
release: yokohama
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-10-27"
reading_time_minutes: 2
keywords: [Discovery, Admin, Workspace]
breadcrumb: [Exploring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery Admin Workspace

The Discovery Admin Workspace serves as a central location for monitoring, tracking, and completing discovery-related tasks. Experience a streamlined discovery process and greater efficiency with the integration of schedules, diagnostics, tuning, anomaly detection, and more within this single workspace.

## Prerequisites

Install and activate the Discovery plugin \(com.snc.discovery\) before you install Discovery Admin Workspace \(sn\_disco\_workspace\).

**Warning:** If you install Discovery Admin Workspace first, Discovery schedules may fail to run due to plugin dependencies.

You must also have the latest ServiceNow Store version of the following applications:

-   Visibility Content
-   \(optional\) Discovery and Service Mapping Patterns

## Dependencies

Installing Discovery Admin Workspace \(sn\_disco\_workspace\) activates or installs the following applications:

-   Service Operations WorkspaceService Reliability Management \(SRM\) Common \(sn\_sow\_srm\_common\)
-   CMDB Workspace \(sn\_cmdb\_ws\)
-   ITOM Discovery Admin Workspace \(com.snc.itom.daw\)
-   ITOM Configuration Console \(sn\_itom\_admin\)
-   ITOM Guided Setup - New \(sn\_sow\_guide\_setup\)
-   CMDB CI Class Models \(sn\_cmdb\_ci\_class\)

**Note:** For on-premises deployments, dependencies aren't installed or updated automatically. For more information, see [Getting apps as an on-premise customer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/getting-apps-on-prem.md).

For a list of Discovery Admin Workspace application dependencies, see [Plugins or applications installed with ITOM Visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/itom-visibility/plugin-app-itom-visibility.md).

## Roles

The following roles have access to the Discovery Admin Workspace:

-   discovery\_admin
-   admin

1.  [Discovery Admin Workspace Home](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/discovery/discovery-admin-workspace-home.md)  
The Discovery Admin Workspace Home page features tools to help you identify and address the most critical discovery tasks.
2.  [Discovery Admin Workspace Schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/discovery/discovery-admin-workspace-schedules.md)  
The Schedules page provides a single place to monitor Discovery performance, efficiently manage schedules and statuses, and set up new IP-based or Cloud Discovery schedules.
3.  [Discovery Admin Workspace Diagnostics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/discovery/discovery-admin-workspace-diagnostics.md)  
The Diagnostics page helps you prioritize and address errors and anomalies in IP-based and Cloud Discovery schedules. Resolve issues by creating error tasks, tracking progress, and using support tools and logs.
4.  [Discovery Admin Workspace Content 360](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/discovery/discovery-workspace-content-360.md)  
The Content 360 page enables you to discover applications and evaluate application suggestions based on machine learning or crowd-sourced resources. Then, create configuration items with a single click.
5.  [Discovery Admin Workspace Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/discovery/discovery-admin-workspace-insights.md)  
The Insights page provides widgets, dashboards, and reports for IT operations management and infrastructure monitoring. Use these tools to improve operational visibility and infrastructure health.
6.  [Discovery Admin Workspace Tuning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/discovery/discovery-admin-workspace-tuning.md)  
Use the Discovery Admin Workspace Tuning page to scan your instance for configuration issues and review the checks that failed.
7.  [Discovery Admin Workspace Settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/discovery/discovery-admin-workspace-setup.md)  
The Settings page enables you to customize and manage high-level Discovery properties so they’re tailored to meet your specific needs.
8.  [View and filter ITOM Visibility apps using the Discovery Admin Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/discovery/view-filter-itom-apps-with-disc-admin-workspace.md)  
Access all ITOM Visibility apps from a single location in the Discovery Admin Workspace. View and filter both the applications already installed on your instance and those applications available for installation. Use this feature to integrate applications and enhance the Discovery experience.

**Parent Topic:**[Exploring Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/discovery/c_GetStartedWithDiscovery.md)

**Related topics**  


[Horizontal discovery process flow with probes and sensors]()

[Horizontal discovery process flow with patterns]()

