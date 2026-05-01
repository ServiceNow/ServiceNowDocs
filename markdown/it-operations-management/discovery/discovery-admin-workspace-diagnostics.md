---
title: Discovery Admin Workspace Diagnostics
description: The Diagnostics page helps you prioritize and address errors and anomalies in IP-based and Cloud Discovery schedules. Resolve issues by creating error tasks, tracking progress, and using support tools and logs.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-05-01"
reading_time_minutes: 6
keywords: [Discovery, Admin, Workspace]
breadcrumb: [Discovery Admin Workspace, Exploring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery Admin Workspace Diagnostics

The Diagnostics page helps you prioritize and address errors and anomalies in IP-based and Cloud Discovery schedules. Resolve issues by creating error tasks, tracking progress, and using support tools and logs.

To access the Discovery Admin Workspace Diagnostics page, navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Diagnostics**.

**Note:** The capabilities described here are available in Discovery Admin Workspace v1.8.0 or later. Specific version requirements are noted for individual features where applicable.

## Key features

-   **Anomaly detection tab**

    Displays all the Discovery schedules with anomalies detected in a certain time period. You can configure this time scale on the Settings page. For more information, see [Discovery Admin Workspace Settings](discovery-admin-workspace-setup.md).

    **Important:** This tab only displays anomalies when anomaly detection is enabled. Starting with version 1.11.0, anomaly detection requires a minimum of five CIs to trigger. For more information, see the [https://support.servicenow.com/kb?id=kb\_article\_view&amp;sysparm\_article=KB2601541](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2601541) article in the Now Support Knowledge Base.

    Select the **More options** icon \(![More options icon](../../health-log-analytics-operator/image/icon-menu-sow.png)\), then select **Refresh** to refresh the data for each visualization in this section.

<table id="table_e1w_2dh_z2c"><thead><tr><th>

Report title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Schedules with anomalies

</td><td>

Indicator

</td><td>

Number of Discovery schedules with anomalies detected over a certain time period. Schedules are categorized as the following:-   Critical anomalies: Failed to run.
-   Major anomalies: Have a low CI discovery rate.
-   Minor anomalies: Have a long run time or a high error count.


</td></tr><tr><td>

Failed schedules

</td><td>

Indicator

</td><td>

Number of Discovery schedules that failed to run.

</td></tr><tr><td>

Low CI discovery rate

</td><td>

Indicator

</td><td>

Number of Discovery schedules that have a low CI discovery rate.**Note:** The threshold for the CI discovery rate can be configured on the Settings page.

</td></tr><tr><td>

Increased error count

</td><td>

Indicator

</td><td>

Number of Discovery schedules that have an increased error count.**Note:** The threshold for the error count can be configured on the Settings page.

</td></tr><tr><td>

Long run time

</td><td>

Indicator

</td><td>

Number of Discovery schedules that had a long run time.**Note:** The threshold for the run time can be configured on the Settings page.

</td></tr></tbody>
</table>    Selecting any of the indicators filters the table to reflect the schedules represented in the data count. For each entry in the table, you can view details around the type and severity of anomalies.

    The **Actions** drop-down menu provides a direct shortcut to the Settings page for configuring anomaly detection. Additionally, the menu includes a **Clear all anomalies** option so that administrators can quickly remove records in the Discovery Schedule Anomaly \[discovery\_schedule\_anomaly\] and Discovery Schedule Anomaly Metrics \[discovery\_schedule\_anomaly\_metrics\] tables.

    Use the **Filter by** options to prioritize and address anomalies. Filter Discovery schedules by name using the **Schedules** drop-down menu. Additionally, you can prioritize the results with the **Severity** drop-down menu, which includes options such as Critical, Major, and Minor. Use the **Anomaly type** drop-down menu to quickly view schedules with the same anomaly. Available options include Failed schedule, Low CI discovery rate, Increased error count, and Long run time.

-   **Diagnostics tab**

    Displays all errors from every discovery. For each entry in the **Discovery errors** table, you can either create an error task or ignore the error using the **Create task** and **Ignore** buttons. If an entry already has an error task, it displays the **Edit task** button along with the task's name and priority.

    Use the **Filter by** options to prioritize and address errors. You can filter by Discovery schedule with the **Schedule** drop-down menu, or search for the name of the error with the **Search** bar. Use the **Sort** drop-down menu to organize the results by Code, Priority, and Total Errors, in either ascending or descending order.

    The error records can also be filtered with the **Filter by** and **Has task** drop-down menus. In the **Filter** menu, you can choose to show only errors related to CMDB, Configuration, Credentials, Internal, or Network. Multiple categories can be selected at the same time. The **Has task** menu shows either all error records, error records that have a task, or error records without a task.

    For each entry in the **Discovery errors** table, the **Total Errors** number can be selected to navigate to the **Error Stats Page**. This page displays information on the error and provides **Instructions**, as well as an associated Knowledge Base article when available. If the error has an associated task, the task number is displayed in the header and can be accessed by selecting the button. The **Action** drop-down menu provides suggested actions based on the type of error. In the **Errors** table, the **Action on selected** drop-down menu can ignore errors for individual IP addresses, retry their discovery, add them to the global exclusion list, or check their Shazzam port status.

-   **Case Management tab**

    Provides an overview of the statuses of error tasks. You can select each task to navigate to its detailed record. New tasks can be created and associated with existing errors using the **Create Task** button. You can filter by Discovery schedule with the **Schedule** drop-down menu, or search for the name of the error task with the **Search** bar. Use the **Kanban Board View** and **List View** to change the display style.

-   **Support tools**

    The **Support tools** tab provides tools to investigate and troubleshoot your instance. For a full list of the tools available on this tab, see [Discovery Admin Workspace support tools](../reference/r_dawSupportTools.md).

-   **Logs**

    The **Logs** tab enables you to access the **ECC Queue** and **Discovery Logs**. Reviewing these logs can help diagnose and resolve errors. You can select an entry in the log to view more details. Additionally, the tables can be filtered or exported using the corresponding buttons.

-   **Ignored Errors tab**

    Keeps a record of all errors ignored in the last 30 days. Errors older than 30 days are deleted. You can add an error back to the **Discovery errors** table using the **Undo ignore** button.


## Virtual agent chat

The Diagnostics page features a virtual agent chatbot in each tab. This chatbot can help retrieve diagnostic information for troubleshooting issues with Discovery. You can either enter a specific request or select **Show me everything** to view all available options.

**Important:** The virtual agent only displays when the **sn\_disco\_workspace.visibility\_diagnostic\_utility.enabled** property is set to **true**.

Selecting the **Discovery &amp; MID Server Health Validation** prompt provides the following options:

-   MID Server Pre-Upgrade Check: Enables you to run on-demand tests on the MID Server before upgrading. It identifies issues that might stop the upgrade process and provides a log to help resolve any issues found.
-   MID Server Status Validation: Validates that the MID Server user is active and is part of the mid\_server group, and checks for basic user authentication errors.
-   MID Server Mutual Authentication: Enables you to select a specific user and verify that the user has an active, non-expired certificate.
-   Pattern Synchronization Validation: Verifies that a pattern and its related libraries are synchronized with the given MID Server and determines if they’re custom.

Selecting the **MID Server Settings Retriever** prompt enables you to retrieve settings from the available MID Servers. If there’s more than one MID Server, the agent provides a list of MID Servers to choose from. Then, you can download the configuration file and analyze the configuration values for the selected MID Server.

**Note:** This option is available beginning with version 1.10.0 of Discovery Admin Workspace.

Selecting the **Discovery Performance Metrics** prompt examines the ECC Queue to gather performance metrics for a discovery status, providing the following information:

-   Average wait times for processing ECC Queue inputs.
-   Average wait times for the MID Server to process ECC Queue outputs.
-   Information about the probes or sensors that took the longest time to complete their tasks.

Selecting the **Retrieve Logs** prompt enables you to access Pattern Logs, Discovery Logs, or Node Logs. Pattern logs can be retrieved using the ECC Queue output ID or the Managed IP address and pattern name. Discovery logs can be accessed by log status or ECC Queue input, and node logs by transaction ID or ECC Queue input.

