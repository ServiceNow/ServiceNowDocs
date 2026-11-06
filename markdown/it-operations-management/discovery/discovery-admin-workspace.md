---
title: Discovery Admin Workspace
description: The Discovery Admin Workspace serves as a central location for monitoring, tracking, and completing discovery-related tasks. Experience a streamlined discovery process and greater efficiency with the integration of schedules, diagnostics, tuning, anomaly detection, and more within this single workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/discovery/discovery-admin-workspace.html
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-10-27"
reading_time_minutes: 1
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

As of Discovery Admin Workspace v1.17.0, Discovery and Service Mapping Patterns is automatically installed and updated as a dependency. For earlier versions, install or update the application manually as needed.

## Dependencies

Installing Discovery Admin Workspace \(sn\_disco\_workspace\) activates or installs the following applications:

-   Service Operations WorkspaceService Reliability Management \(SRM\) Common \(sn\_sow\_srm\_common\)
-   CMDB Workspace \(sn\_cmdb\_ws\)
-   Discovery and Service Mapping Patterns \(sn\_itom\_pattern\)
-   ITOM Discovery Admin Workspace \(com.snc.itom.daw\)
-   ITOM Configuration Console \(sn\_itom\_admin\)
-   ITOM Guided Setup - New \(sn\_sow\_guide\_setup\)
-   CMDB CI Class Models \(sn\_cmdb\_ci\_class\)

**Note:** For on-premises deployments, dependencies aren't installed or updated automatically. For more information, see [Getting apps as an on-premise customer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/getting-apps-on-prem.md).

For a list of Discovery Admin Workspace application dependencies, see [Plugins or applications installed with ITOM Visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/itom-visibility/plugin-app-itom-visibility.md).

## Roles

The following roles have access to the Discovery Admin Workspace:

-   discovery\_admin
-   admin

