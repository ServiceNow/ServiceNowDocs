---
title: Proactive Engagement overview
description: Proactive Engagement is a solution where the self-resolution remediation process is proactive, seamless, and consistent without the organization having to publish all solution sets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/proactive-engagement-overview.html
release: brazil
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Explore, Digital End-User Experience, IT Service Management]
---

# Proactive Engagement overview

Proactive Engagement is a solution where the self-resolution remediation process is proactive, seamless, and consistent without the organization having to publish all solution sets.

ServiceNow® Proactive Engagement helps an organization in improving employee digital experience, productivity, and satisfaction by proactively enabling employees to self-solve digital issues they experience on a day-to-day basis. The self-remediation process is seamless and consistent without the organization having to publish all solution sets.

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

\[Omitted video\] Description: Proactive Engagement overview

## Proactive Engagement Key features

-   Enables employees to self-solve digital experience issues by using the proactive issue detection and resolution capability of the ServiceNow Digital End-User Experience product.
-   Engages employees to provide a seamless resolution experience through remedial actions \(automations\) and self-service content.
-   Provides quick scaling and consistent support for increasing the range of applications.

## ServiceNow Digital End-User Experience integration with Proactive Engagement

ServiceNow Digital End-User Experience empowers IT to take proactive measures and offers a clear view of end-user applications, devices, and networks. It further along with Proactive Engagement enables employees to independently resolve issues, troubleshoot, and engage with the Virtual Agent.

ServiceNow Proactive Engagement is part of the ServiceNow Digital End-User Experience now. The Proactive Engagement application is installed as part of the Digital End-User Experience bundle. It assists in defining issue detection rules, resolution content, and engagement settings that help employees to self-solve digital experience issues by using proactive identification of issues.

## DEX admin/Engagement admin experience

-   A DEX or engagement admin is part of the customer’s organization.
-   Creates a metric rule for each device or application CI to enable DEX to detect specific issues and defines the specific alert action. An Alert action defines the action to be taken whenever a threshold in the metric rule is reached. It supports a configuration of resolution types like remedial actions, self-help instructions, URL, and create incident. For example, when an application crashes, you can clear the application cache or update the application to the latest version.
-   Configure engagement settings such as channels to notify and engage with the organization’s employees, notification content, and fallback options for unsuccessful resolution of issues.
-   Captures and reports insights that reflect the usage patterns of Proactive Engagement in ITSM Success Dashboard.
-   Customize the Proactive Engagement base system resolutions that are shipped by ServiceNow.
-   Manage the Proactive Engagement resolutions through the Proactive Engagement workbench.

**Note:** The Engagement admin role is required to add an alert action.

## Employee experience

-   Employee is a part of the customer's organization.
-   When an employee experiences an issue for which the metric rule and resolution is already configured, the employee is proactively notified over the configured engagement channel. The employee is offered a resolution for the issue in real-time. The engagement occurs as soon as the issue is detected and before the employee reaches out to the helpdesk.
-   The employee can be more productive and efficient after virtually engaged while self-solving issues. It also reduces the number of incidents and load on agents due to this seamless digital experience.
-   Virtual Agent installation and integration with a third-party messaging application to enable push notifications for proactive employee engagement.

## Proactive issue detection and Resolution

1.  ServiceNow Digital End-User Experience application proactively detects a digital experience issue on an employee device by monitoring the metric rule threshold breach and creates an experience issue.
2.  Proactive Engagement validates the experience issue and sends a notification \(based on the notification settings\) to the employee through configured channels such as Virtual Agent on Employee Centre/Service Portal, integration with any messaging application such as MS Teams. The employee can choose to accept help based on this notification or ignore it.

    **Note:**

    -   When the employee accepts help, the employee is engaged through the configured engagement channel.
    -   Currently, only Virtual Agent is the supported configured channel to send notifications to the employee.
3.  Proactive Engagement retrieves the configured proactive resolution for the metric rule and engages the employee by providing solutions such as URLs, self-help instructions, or executes the relevant remedial action on the employees device with their consent.

    -   If the resolution has successfully resolved the issue, the engagement is marked as successful.
    -   If the resolution has not resolved the issue, the employee is given fallback options such as incident creation or will be connected to an agent.

        **Note:** Fallback options are configured by the DEX or Engagement admin.

    The ServiceNow Proactive Engagement provides base resolution content. You can create your own resolution content as well. For more information, on the base resolutions, see [Proactive Engagement solution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/proactive-engagement-solution.md).


