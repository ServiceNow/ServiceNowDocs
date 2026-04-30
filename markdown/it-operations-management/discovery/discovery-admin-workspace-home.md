---
title: Discovery Admin Workspace Home
description: The Discovery Admin Workspace Home page features tools to help you identify and address the most critical discovery tasks. Access critical information and applications to assess discovery, manage the discovery process, and resolve any related errors.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 4
breadcrumb: [Discovery Admin Workspace, Exploring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery Admin Workspace Home

The Discovery Admin Workspace Home page features tools to help you identify and address the most critical discovery tasks. Access critical information and applications to assess discovery, manage the discovery process, and resolve any related errors.

To access the Discovery Admin Workspace, navigate to **Workspaces** &gt; **Discovery Admin Workspace**.

**Note:** The capabilities described here are available in Discovery Admin Workspace v1.8.0 or later. Specific version requirements are noted for individual features where applicable.

## Quick overview

View the status of discovery using data counts and identify any irregularities that might impact discovery. For detailed information, select the appropriate tile.

Select the **More options** icon \(![More options icon](../../health-log-analytics-operator/image/icon-menu-sow.png)\), then select **Refresh** to refresh the data for each visualization in this section.

The following data counts are displayed in the Quick overview section:

-   **Active schedules**

    Displays the number of active IP-based and Cloud Discovery schedules run to date. Selecting this number redirects you to the Schedules page, where you can view all the Discovery schedules that are configured and enabled to run.

-   **Error tasks**

    Displays the active, including pending or in-progress, Discovery error tasks opened in a certain time period. Selecting this number redirects you to the Case management page, where you can view all Discovery error tasks.

    **Note:** You can configure the time scale reflected in the displayed count on the Settings page. For more information, see [Discovery Admin Workspace Settings](discovery-admin-workspace-setup.md).

-   **Schedules with anomalies**

    Displays the number of Discovery schedules with anomalies detected over a certain time period. You can configure this time scale on the Settings page. For more information, see [Discovery Admin Workspace Settings](discovery-admin-workspace-setup.md).

    Selecting this number redirects you to the **Anomaly detection** tab, where you can view details about the type and severity of anomalies.

    **Important:** This count only displays when anomaly detection is enabled. If anomaly detection is inactive, select **Turn on** to be redirected to the Settings page.


## Discovery admin tasks

Review the three most critical Discovery error tasks. Select the **Edit Task** button to access the details page where you can assign or update the error task, or add work notes. To view and manage all discovery error tasks, select **View all** to access the **Case management** page.

**Note:** This section focuses solely on Discovery errors that have associated tasks and not all Discovery errors.

## Discovery tuning advice

Fine-tune Discovery and MID Server settings with automated suggestions derived from scans of your instance. These findings identify potential issues, arranged in order of their criticality. Selecting a finding directs you to the **Tuning Check** page for more details.

## Quick Discovery

Discover devices in your network outside of a scheduled discovery. Enter a single IP address, multiple comma-separated IP addresses, or an IP network as shown in this example:

-   IP network address - 10.0.1.0/24
-   IP address range - 10.0.2.1-10.0.2.15
-   IP address list - 10.0.3.176,10.0.3.222,2001::100,2600:1bdc::fffe

Select a MID Server, a MID cluster, or enable Discovery to select the MID Server automatically.

## ITOM Visibility apps

Enhance the functionality of the Discovery Admin Workspace by integrating additional ITOM Visibility applications. When you select **View all**, you can view both the applications installed on your instance and others that are available for installation.

**Note:** Updating applications requires you to have the admin role.

While you can access details about the apps installed on your instance, information regarding pricing and packages isn’t provided, as it varies based on each contract. For a general overview of licensing and subscription details, see [ITOM/OT SU Licensing and subscriptions](../../it-operations-management/reference/itom-su-licensing-landing-page.md).

## Learnings

Receive guidance on managing the Discovery process and resolving Discovery errors with the ITOM Visibility Knowledge Base. Access relevant articles from the Now Support Knowledge Base, explore blog posts, or watch instructional video tutorials for further information.

**Important:**

-   To view the resources in this section, confirm that you have installed ITOM Content Service version 1.2.8.
-   If you encounter an **Error 153: Video player configuration error** message when attempting to play a video on the **Videos** tab, update the system property **com.glide.security.referrerpolicy** to **origin-when-cross-origin**. For more information, see [Enforce secure referrer policy \[New in Security Center 1.3\]](https://www.servicenow.com/docs/access?context=sc-enforce-secure-referrer-policy&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

**Parent Topic:**[Discovery Admin Workspace](discovery-admin-workspace.md)

**Previous topic:**[Discovery Admin Workspace](discovery-admin-workspace.md)

**Next topic:**[Discovery Admin Workspace Schedules](discovery-admin-workspace-schedules.md)

