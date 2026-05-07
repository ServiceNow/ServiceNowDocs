---
title: Settings page
description: The Settings page lets you view and modify system-wide settings for the Discovery Console for OT, Discovery Sensor for OT, and the OT Discovery Collector.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Use the Console pages, Discovery Console for OT, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Settings page

The **Settings** page lets you view and modify system-wide settings for the Discovery Console for OT, Discovery Sensor for OT, and the OT Discovery Collector.

## Settings page overview

To open the Settings page, select **Settings** from the main navigation menu. The Settings page is divided into tabs and opens to the **Console** tab view. The Settings page is organized by the following tab configuration options.

**Console**

The Console tab on the main Settings page is divided into the following sections.

-   **About**

    The Console tab includes a link to the End-User License Agreement \(EULA\), the version number of the Console, and the Console ID.

-   **License**

    When you first sign into the Console, a warning banner alerts that you need a license. When you use the interactive configuration wizard, you're also alerted to the license status. For detailed explanation of the Console license, see [Requirements for Discovery Console for OT installation](requirements-installation-deployment.md).

    **Note:** If needed, request a Console license from your ServiceNow account representative.

-   **Configuration**

    The Configuration section displays the Console Name of the local web Console. The Console Name is used in Syslog messages.

    In the Configuration section, use the **High Contrast** setting to change hyperlinks from orange to green for ease in viewing. To change this setting, select the **Edit** button, then slide the **High Contrast** toggle to **Yes**. Select **Save** to save your changes.

    ![High contrast setting](../images/configuration-section-high-contrast.png)

-   **System Statistics**

    The Console settings show disk and memory usage for its host server. It's important to maintain an adequate disk and memory space so that the Console continues operating properly. Check the system statistics periodically to confirm that proper resources are available.


**Certificate**

On the Certificate tab, you can check the Console Certificate status. You can also update the certificate by selecting Generate New Bundle or Upload Bundle \(.p12\) and then selecting the **Generate Bundle** button.

**Note:** The Certificate tab does not function the same as the **Certificates** page.

**API**

The API settings manage active and denied tokens and provide endpoint configuration files for the Service Graph Connector for ServiceNow OT Discovery.

**Email**

The Discovery Console for OT can be configured to send email and SMS text alerts when certain conditions occur within the system. To do so, the Console relies on an external mail server to send messages.

In the Email Server Configuration panel, enter the settings that match your mail server configuration. The Discovery Console for OT uses these settings whenever the **Enable Alert Notifications** setting is activated.

**Exports**

The Export tab downloads data from the Console to JSON files. Available data types include Assets, Sites, Software, Sensors, Network Zones, Notifications, Images, and All. Selecting All bundles and downloads data from all categories in one ZIP file.

**Metadata**

The Metadata tab includes settings for several features related to metadata that can be used to enrich the analysis and reporting of data collected by the Console. For example, you can set up metadata to provide more details about the connections observed in the network.

The following table describes the different sections of the Metadata tab.

<table id="table_ndd_vpk_dhc"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CVE Database Package

</td><td>

Enables you to import a CVE package.You can use the **Import CVE Package** button to import a package locally saved on your computer.

**Note:** You can obtain a current CVE database file from your ServiceNow Operational Technology Discovery representative.

</td></tr><tr><td>

Query Driver

</td><td>

Enables you to import or download query drivers and set the concurrence and speed of Sensor and Scout queries.You can use the **Import Query Driver** button to import a query driver from your computer or **Download Query Driver** to download the current query driver and save locally.

To edit the Query Driver settings, select the **Edit Settings** button.

</td></tr><tr><td>

Common Port Names

</td><td>

Defines a mapping between port numbers and protocol names. This information is used in the Console to display protocol names when you create a ports activity report. This feature must be turned off to import a new port name file. To enable or disable this setting, select the **Edit** button under the Common Port Names and Ethernet vendor sections.A current port names file can be obtained from your Discovery Console for OT representative.

</td></tr><tr><td>

Ethernet vendors

</td><td>

Defines a mapping between MAC addresses and vendor information. This information is used in the Console to provide vendor information for assets. This feature must be turned off to import a new Ethernet vendors file. To enable or disable this setting, select the **Edit** button under the Common Port Names and Ethernet vendor sections.A current Ethernet vendors file can be obtained from your Discovery Console for OT representative.

</td></tr></tbody>
</table>**Package**

In the Package tab, you can use the package source options under the **Package Manager Configuration** section. You can import packages by file upload or from a remote repository.

**Note:** The package manager must be configured so that your Discovery Console for OT sensors can receive firmware updates.

**Reprocess**

The Reprocess feature allows the system to reevaluate previously collected Auto Query scan results using the latest query driver logic. See [Reprocess Auto Query results](reprocess-tab-results.md) for more information.

**Syslog**

In the Syslog tab, you can configure a syslog server. After configuring these settings, syslog data can be forwarded from the Discovery Console for OT to a separate syslog data consumer. For example, the Splunk enterprise security data analysis toolset.

ea**Logs**

From the Logs tab, you can download Discovery Console for OT logs. You have the option to choose whether to download logs on the current day, on a custom date, or on a date range.

For further information on Console and Sensor log files, see [Download Console log files](download-console-log-files.md).

