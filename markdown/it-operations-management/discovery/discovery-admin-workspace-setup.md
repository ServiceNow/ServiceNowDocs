---
title: Discovery Admin Workspace Settings
description: The Settings page enables you to customize and manage high-level Discovery properties so they’re tailored to meet your specific needs.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 8
keywords: [Discovery, Admin, Workspace]
breadcrumb: [Discovery Admin Workspace, Exploring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery Admin Workspace Settings

The Settings page enables you to customize and manage high-level Discovery properties so they’re tailored to meet your specific needs.

To access the Discovery Admin Workspace Settings page, navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Settings**.

**Note:** The capabilities described here are available in Discovery Admin Workspace v1.13.0. Specific version requirements are noted for individual features where applicable.

## General

The General settings control how Discovery visualizations are displayed in the workspace.

-   **Dashboard time scale**

    Enables you to see the health of your schedules over your preferred time span.

    Use the **Time scale** drop-down list to choose between 7, 14, and 30-day time periods. The default time period is 7 days. After you configure it, all relevant data visualizations across the Home, Schedules, and Diagnostics pages update to measure over this time period.

    **Important:** After these settings are saved, you must refresh your browser to update the data visualizations with the new time scale.


**Note:** No changes are applied until you select **Save**.

## Anomaly Detection

The Anomaly Detection settings control how Discovery identifies and surfaces irregular schedule behavior within the Discovery Admin Workspace.

-   **Anomaly detection**

    Identifies unusual behavior, like failed runs and significant deviations from the thresholds for high error counts, longer discovery status duration, and fewer discovered configuration items \(CIs\) or Cloud resources.

    Anomalies are categorized into the following severity levels:

    -   **Critical**: Schedules that have failed to run
    -   **Major**: Schedules that have a low CI discovery rate
    -   **Minor**: Schedules that have a long run time or a high error count
    The **Enable anomaly detection** toggle enables you to turn the feature on and off. This feature is on by default.

    **Warning:** Turning off this feature significantly impacts the Discovery experience across multiple pages, charts, and tables.

-   **Detection method**

    Identifies anomalies in Discovery schedules with the following approaches:

    -   **ML-based**: Leverages machine learning \(ML\) algorithms to analyze historical schedule data, recognize complex patterns, and detect anomalies without predefined rules.
    -   **Stats-based**: Relies on traditional mathematical techniques, such as calculating standard deviations to identify outliers based on fixed numerical thresholds.
    Select the **Detection method** drop-down list to choose an approach. The ML-based approach is the default detection method.

    You can also adjust the sensitivity of anomaly detection. Lower sensitivity reports more anomalies, which might lead to more false positives, which means that normal scans are flagged as anomalies. Higher sensitivity reports fewer anomalies, which might result in more false negatives, which means that actual anomalies might not be detected.

    Use the **Sensitivity** drop-down list to choose your preferred detection sensitivity. Choices include Lowest, Low, High, Highest. By default, anomaly detection is set to Low sensitivity.

-   **Adjust thresholds**

    Adjusting thresholds helps prevent false positives, making sure that normal scans aren't mistakenly flagged as anomalies. When the anomaly detection method flags a Discovery status as an anomaly, the status metrics are analyzed for deviations from the average measurements based on the specified thresholds.

    Scans are marked as anomalous when the run time, error count, or CI measurements deviate from the average by a specified threshold. The default threshold is 20%, but you can change the number that defines this threshold in the relevant text box. Selecting **Reset** reverts the threshold back to the default 20%.


**Note:** No changes are applied until you select **Save**.

## IP Address Management \(IPAM\)

The IPAM settings manage how Discovery integrates with your IPAM sources, controlling schedule creation and connection behavior within the workspace. For more information, see [IPAM Discovery integration](ipv6-ipam-disco-integration.md).

**Important:** This feature requires the Zurich, ZP8 or later, or YP13 or later version of the ServiceNow AI Platform. You must also install and configure Service Graph Connector Central \(SGC Central\) v2.4.0, as well as Service Graph Connector for Infoblox v1.5.0. For more information, see [Configuring SGC Central](https://www.servicenow.com/docs/access?context=sgcc-configuring&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) and [Configure Service Graph Connector for Infoblox using SGC Central](https://www.servicenow.com/docs/access?context=sgcc-configure-infoblox-integ&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

-   **Auto-create Discovery schedules**

    Automatically create and manage Discovery schedules based on your IPv6 network infrastructure data stored in IPAM.

    After you install and configure the connectors via SGC Central, use the toggle to enable auto-created schedules. Once enabled, Discovery creates schedules from incoming IPAM data and keeps them updated based on your auto‑creation criteria and IP data refresh settings. Schedules created automatically by IPAM are inactive by default. To activate a schedule created by IPAM, see [Activate auto-created Discovery schedules](../task/activate-auto-disco-schedule.md).

    Use the Auto-creation criteria setting to define how Discovery organizes IPs from your IPAM connections into new Discovery schedules. Discovery evaluates the key that you provide, retrieves the corresponding value from your IPAM data by looking it up in the Key Values \[cmdb\_key\_value\] table, where it searches only subnet records. IPs that share values are assigned to the same schedule, allowing the schedule structure to follow meaningful attributes such as location or environment.

    **Note:** If you don't want to provide a key, you can enter a single space in the **Tag key** field.

    Use the data refresh settings to keep auto-created schedules aligned with the latest IPAM information. Discovery checks for new, updated, or removed IPs during each refresh and updates schedule mappings accordingly. This ensures that schedules remain accurate as your network changes.

-   **IPAM connectors and connections**

    Provides a centralized view of your installed IPAM connectors and connections, along with access to their configuration details and drafts.

    The Installed connections tab displays the details of your existing IPAM connections. Selecting a connection from this list opens the connection record, where you can view information such as connection properties, status, and data sources.

    The Installed connectors tab shows the IPAM connectors that are installed on your instance. Selecting a connector from this list opens its connector record, where you can review its configuration and confirm that it's ready to send imported IP data to Discovery.

    The Drafts connections tab lists any IPAM connections that were created but not fully configured. Select **Resume setup** next to the draft connection to complete the required settings before it becomes active.

-   **IP data from IPAM connections**

    Enables you to view the IP address information imported from your IPAM solutions and understand how that data is organized for Discovery. This includes lists that show the IPs retrieved through your IPAM connections and how those IPs are mapped to auto-created schedules.

    Select the **IP schedule mapping** link to access the IPAM Data page, which displays a list of the IPv6 addresses mapped to auto-created schedules.

    **Note:** This link displays only when auto-created schedules are enabled.

    Select the **Imported IPs** link to access the IPAM Data page, displaying a list of IP data imported from your IPAM solutions through SGC connections. To avoid data corruption, don't edit or add IP data to the Imported IPs list.


**Note:** No changes are applied until you select **Save**.

To synchronize your IP data immediately instead of waiting for the next refresh time, select **Refresh IP data**.

## Discovery notifications

Discovery notifications enable administrators to receive real-time alerts or daily summaries of critical Discovery errors and schedule failures via Microsoft Teams and email, directly from the Discovery Admin Workspace.

**Important:** This feature requires the Zurich, Zurich, or YP6 or later version of the ServiceNow AI Platform. Before you can set up notifications, you must configure the Microsoft Teams Graph spoke. For more information, see [Set up the](https://www.servicenow.com/docs/access?context=set-up-msteams&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

-   **Notification destinations**

    Enables you to configure where your team receives Discovery notifications to respond quickly to urgent anomalies, errors, and failures.

    To integrate your Microsoft Teams channel or email for notifications, select **Configure** the first time you set up the integration, or use the **Edit** icon \(![Edit credentials icon.](../../../reuse/itom/image/workspace-icon-edit.png)\) to update it at any time. For Microsoft Teams, enter a channel name and URL in the corresponding fields.

    **Note:** The channel name is unique to Discovery Admin Workspace, but the channel URL must be obtained directly from Microsoft Teams.

    Select **Send test notification** to validate the integration. A failed test displays an error message, while a successful test sends a notification to your Teams channel. Once you send the test notification and select **Save**, the connection status updates. A successfully validated channel URL displays a **Connected** status. If validation fails, the status changes to **Disconnected** and includes a timestamp for the last attempted connection.

    For email, enter a valid email address in the text box and select **Add**. There’s no limit to the number of recipients that you can add. To remove a recipient, select **X**. Recipients can opt out of email notifications by selecting the **Unsubscribe** link in the email and sending the auto-generated response.

    **Note:** The **Unsubscribe** option is available only if the recipient's email address is associated with a sys\_user record.

-   **Notification settings**

    After configuring your notification destinations, you can use the settings here to create and update notification rules, view connected Microsoft Teams channels, and adjust integration details as needed.

    Use the toggle to enable Discovery notifications. This feature is off by default.

    When enabled, the notification table displays four notification categories:

    -   **Auto created IPAM schedules**: Notifies you when an auto-created IPAM schedule requires manual activation.
    -   **Critical anomalies**: Notifies you when anomaly detection identifies a schedule that has failed to run.
    -   **MID cluster down**: Notifies you when a Discovery-specific MID cluster goes down.
    -   **MID server down**: Notifies you when a Discovery-specific MID Server goes down.
    To configure a notification, select the **Edit** icon \(![Edit credentials icon.](../../../reuse/itom/image/workspace-icon-edit.png)\) or the **Name** hyperlink. You can also use in-line editing within the table.

    By default, all Microsoft Teams and email notifications are enabled. The notification frequency is set to **Immediately** for all notifications, except critical anomalies, which is set to **Daily**.


