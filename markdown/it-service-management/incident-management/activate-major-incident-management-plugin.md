---
title: Activate Major Incident Management
description: You can activate the Incident Management - Major Incident Management plugin \(com.snc.incident.mim\) if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/activate-major-incident-management-plugin.html
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Major Incident Management plugins, Managing major incidents, Incident Management, IT Service Management]
---

# Activate Major Incident Management

You can activate the Incident Management - Major Incident Management plugin \(com.snc.incident.mim\) if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.

## Before you begin

Confirm that the application and all of its associated ServiceNow Store applications have valid ServiceNow® entitlements.

Role required: admin

## About this task

Starting with the Brazil release, a scheduled job is available. The scheduled job executes a batch installation on a newly provisioned instance to automatically install applications such as Major Incident Management applications if the customer has the necessary ServiceNow® entitlements. This job applies only to newly provisioned zBoot instances. If the application isn't installed automatically, you can use this procedure to install and activate the application manually.

You must manually activate the Incident Management - Major Incident Management plugin \(com.snc.incident.mim\) for new and existing customers.

Incident Management - Major Incident Management plugin activates these related plugins if they are not already active:

-   Incident Communications Management \(com.snc.iam\)
-   Incident Updates \(com.snc.incident.updates\)
-   Task-Outage Relationship \(com.snc.task\_outage\)

<table id="table_fd2_xjb_rbb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Notify\[com.snc.notify\]

</td><td>

Provides platform features for workflow-driven voice calls, conference calls, and SMS messages. Requires the Twilio Direct Driver and a separate contract with Twilio for SMS and Voice capabilities.**Note:** Existing users of the Twilio Driver must [migrate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_MigrateToTwilioDirectDriver.md) to Twilio Direct Driver.

</td></tr><tr><td>

On-Call Scheduling\[com.snc.on\_call\_rotation\]

</td><td>

Provides the ability to create on-call schedules and escalation trees. When an incident is created, the escalation is routed dynamically to an on-call resource. On-Call Scheduling enables you to configure and build different on-call schedules per process and assignment group.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).


-   **[Components installed with Major Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/installed-with-mim.md)**  
Activating the Incident Management - Major Incident Management plugin installs several types of components, including tables and user roles.
-   **[Slack notifications installed with Major Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/slack-notification-installed-with-MIM.md)**  
Slack notifications are added when you activate the Incident Management - Major Incident Management plugin \(com.snc.incident.mim\).

**Parent Topic:**[Major Incident Management plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/mim-plugins.md)

**Related topics**  


[Managing major incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/major-incident-management.md)

[Legacy: Major incident overview dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/major-incident-overview.md)

[Major incident workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/major-incident-workbench.md)

[List of Brazil plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/list-of-plugins.md)

