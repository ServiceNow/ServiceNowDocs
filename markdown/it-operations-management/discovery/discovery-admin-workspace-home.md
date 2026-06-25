---
title: Discovery Admin Workspace Home
description: The Discovery Admin Workspace Home page features tools to help you identify and address the most critical discovery errors.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/discovery-admin-workspace-home.html
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-06-25"
reading_time_minutes: 5
keywords: [Discovery, Admin, Workspace]
breadcrumb: [Discovery Admin Workspace, Exploring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery Admin Workspace Home

The Discovery Admin Workspace Home page features tools to help you identify and address the most critical discovery errors.

To access the Discovery Admin Workspace, navigate to **Workspaces** &gt; **Discovery Admin Workspace**.

**Note:** The capabilities described here are available in Discovery Admin Workspace v1.17.0. If the **sn\_disco\_workspace.enable\_error\_framework** system property is turned off, the Home page displays the legacy experience. Specific version requirements are noted for individual features where applicable.

\[Omitted image "daw-home-ef.png"\] Alt text: Discovery Admin Workspace Settings page

## Onboarding for Discovery

The onboarding experience on the Home page changes based on your configuration progress. Before you create an IP or cloud-based Discovery schedule, the Home page displays an Onboarding for Discovery section. Select **Get started** to access the ITOM Configuration Console.

**Note:** Note: The ITOM Configuration Console is available in Zurich Patch 8 or later versions of the ServiceNow AI Platform. For more information, see [ITOM Configuration Console for Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/itom-conf-console.md).

After you create a schedule, the Onboarding for Discovery section is replaced by an Onboard Discovery progress indicator. This indicator displays the number of completed configuration tasks. Select **Continue** to resume configuration in the ITOM Configuration Console.

After you complete configuration, the Home page displays an Onboarding for Discovery link as a persistent entry point to the ITOM Configuration Console.

## Quick overview

View the status of discovery using data counts and identify any irregularities that might impact discovery. For detailed information, select the appropriate tile.

Select the **More options** icon \(\[Omitted image "icon-menu-sow.png"\] Alt text: More options icon\), then select **Refresh** to refresh the data for each visualization in this section.

**Note:** You can configure the time scale reflected in the displayed counts on the [Settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/discovery-admin-workspace-setup.md) page.

The following data counts display in the Quick overview section:

-   **Active schedules**

    Displays the number of active IP-based and Cloud Discovery schedules run to date. Selecting this number opens the [Schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/discovery-admin-workspace-schedules.md) page, where you can view all the Discovery schedules that are configured and enabled to run.

-   **Schedules with anomalies**

    Displays the number of Discovery schedules with anomalies detected over a certain time period. This count only displays when anomaly detection is enabled. If anomaly detection is inactive, select **Turn on** to access the [Settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/discovery-admin-workspace-setup.md) page.

    Selecting this number redirects you to the Anomaly detection tab on the [Diagnostics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/discovery-admin-workspace-diagnostics.md) page, where you can view details about the type and severity of anomalies.

-   **Discovery Operations Monitor**

    Monitor discovery performance across your IT environment. Select **View dashboard** to open the dashboard and view performance metrics for transactions, sensor jobs, MID Server queue load, and probe processing times. For more information, see [Discovery Operations Monitor dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/disco-operations-monitor.md).


## Top discovery errors

View the most critical Discovery errors currently active on your instance, including a summary count of active errors by severity. Each error card displays the error title, severity, refined code, occurrence count, and error category. Selecting an error card or the **Occurrences** link opens the [Error Details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/daw-error-details.md) page, where you can view the root cause, remediation steps, and individual error instances. Select **View all** to access the [Diagnostics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/discovery-admin-workspace-diagnostics.md) page.

## Discovery tuning advice

Fine-tune Discovery and MID Server settings with automated suggestions derived from scans of your instance. These findings identify potential issues, arranged in order of their criticality. Selecting a finding redirects you to the **Tuning check** page for more details. To view all tuning checks and latest reports, select **View all** to access the [Tuning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/discovery-admin-workspace-tuning.md) page.

## Quick Discovery

Discover devices in your network outside of a scheduled discovery. Enter a single IP address, multiple comma-separated IP addresses, or an IP network as shown in this example:

-   IP network address - 10.0.1.0/24
-   IP address range - 10.0.2.1-10.0.2.15
-   IP address list - 10.0.3.176,10.0.3.222,2001::100,2600:1bdc::fffe

Select a MID Server, a MID cluster, or enable Discovery to select the MID Server automatically.

## ITOM Visibility apps

Enhance the functionality of the Discovery Admin Workspace by integrating additional ITOM Visibility applications. When you select **View all**, you can view both the applications installed on your instance and others that are available for installation.

**Note:** Updating applications requires you to have the admin role.

While you can access details about the apps installed on your instance, information regarding pricing and packages isn't provided, as it varies based on each contract. For a general overview of licensing and subscription details, see [ITOM/OT SU Licensing and subscriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-su-licensing-landing-page.md).

## Learnings

Receive guidance on managing the Discovery process and resolving Discovery errors with the ITOM Visibility Knowledge Base. Access relevant articles from the ServiceNow Knowledge Base, explore blog posts, or watch instructional video tutorials for further information.

**Important:**

-   To view the resources in this section, confirm that you have installed ITOM Content Service version 1.2.8.
-   If you encounter an **Error 153: Video player configuration error** message when attempting to play a video on the **Videos** tab, update the system property **com.glide.security.referrerpolicy** to **origin-when-cross-origin**. For more information, see [Enforce secure referrer policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/sc-enforce-secure-referrer-policy.md).

