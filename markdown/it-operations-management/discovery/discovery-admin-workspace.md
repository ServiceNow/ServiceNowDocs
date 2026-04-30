---
title: Discovery Admin Workspace
description: The Discovery Admin Workspace serves as a central location for monitoring, tracking, and completing discovery-related tasks. Experience a streamlined discovery process and greater efficiency with the integration of schedules, diagnostics, tuning, and more within this single workspace.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Exploring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery Admin Workspace

The Discovery Admin Workspace serves as a central location for monitoring, tracking, and completing discovery-related tasks. Experience a streamlined discovery process and greater efficiency with the integration of schedules, diagnostics, tuning, and more within this single workspace.

## Discovery Admin Workspace Home page

The Discovery Admin Workspace Home page features tools to help you identify and address the most critical discovery tasks. Access critical information and applications to assess discovery, manage the discovery process, and resolve any related errors.

To access the Discovery Admin Workspace, navigate to **Workspaces** &gt; **Discovery Admin Workspace**.

## Quick Overview

View the status of discovery using data count and visualizations and identify any irregularities that might impact discovery. The count shown represents data from the last 24 hours, and the trend line shows activity patterns from the last 7 days or longer. For detailed information, select the appropriate tile.

Select the **More options** icon \(![More options icon](../../../common/image/icon-menu.png)\), then select **Refresh** to refresh the data for each visualization in this section.

**Note:** Updates only appear once the daily Performance Analytics job completes. For more details, see [Collect data for Platform Analytics Solutions](https://www.servicenow.com/docs/access?context=collect-data-nowintel-solutions&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).

-   **Canceled discoveries**

    Drill down to analyze canceled discoveries using the data displayed. Flat sections of the trend line indicate no cancellations, while spikes represent canceled discoveries. Selecting this visualization redirects you to one of the tabs for the **Discovery schedules** page. To view related canceled discovery statuses, select the **Discovery status** tab.

-   **ECC queue load**

    Troubleshoot potential discovery issues using a data visualization of MID Server tasks currently in the External Communications Channel \(ECC\) queue. Unusual spikes in the trend line may indicate activities that might disrupt the discovery process. Selecting this visualization redirects you to the ECC Queue log. For more information, see [The ECC queue for Discovery](../reference/r_DiscoveryStatusECCQueue.md).

-   **Error tasks**

    The displayed count represents the discovery error tasks opened in the last 24 hours, while the visualization shows those error tasks that were opened over the past 7 days or more. Selecting this visualization redirects you to the **Case management** page, where you can view all discovery error tasks.


## Discovery admin tasks

Review the three most critical discovery error tasks. Select the **Edit Task** button to access the details page where you can assign or update the error task, or add work notes. To view and manage all discovery error tasks, select **View all** to access the **Case management** page.

**Note:** This section focuses solely on discovery errors that have associated tasks and not all discovery errors.

## Discovery tuning advice

Fine-tune discovery and MID Server settings with automated suggestions derived from scans of your instance. These findings identify potential issues, arranged in order of their criticality. Selecting a finding directs you to the **Tuning Check** page for more details.

## Quick Discovery

Discover devices in your network outside of a scheduled discovery. Enter a single IP address, multiple comma-separated IP addresses, or an IP network as shown in this example:

-   IP network address - 10.0.1.0/24
-   IP address range - 10.0.2.1-10.0.2.15
-   IP address list - 10.0.3.176,10.0.3.222,2001::100,2600:1bdc::fffe

Select a MID Server, a MID cluster, or enable Discovery to select the MID Server automatically.

## ITOM Visibility apps

Enhance the functionality of the Discovery Admin Workspace by integrating additional ITOM Visibility applications. When you select **View all**, you can view both the applications installed on your instance and others that are available for installation. To learn more, see [View and filter ITOM Visibility apps using the Discovery Admin Workspace](../task/view-filter-itom-apps-with-disc-admin-workspace.md).

## Learnings

Receive guidance on managing the discovery process and resolving discovery errors with the ITOM Visibility Knowledge Base. Access relevant articles from the ServiceNow Knowledge Base, explore blog posts, or watch instructional video tutorials for further information.

**Important:**

-   To view the resources in this section, confirm that you have installed ITOM Content Service version 1.2.8.
-   If you encounter an **Error 153: Video player configuration error** message when attempting to play a video on the **Videos** tab, update the system property **com.glide.security.referrerpolicy** to **origin-when-cross-origin**. For more information, see [Enforce secure referrer policy \[New in Security Center 1.3\]](https://www.servicenow.com/docs/access?context=sc-enforce-secure-referrer-policy&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## Prerequisites

Plugins and ServiceNow Store applications:

-   Discovery
-   Visibility Content
-   CMDB Workspace
-   Discovery Admin Workspace

**Note:** To enable Discovery Admin Workspace, activate the ITOM Discovery Admin Workspace plugin \(com.snc.itom.daw\) in **Application Manager**.

## Roles

The following roles have access to the Discovery Admin Workspace:

admin or discovery\_admin.

## Dependencies

For a list of Discovery Admin Workspace application dependencies, see [Plugins or applications installed with ITOM Visibility](../../it-operations-management/reference/plugin-app-itom-visibility.md).

