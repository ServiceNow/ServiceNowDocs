---
title: View live CI data with Agent Client Collector
description: View live data for incident-related CIs through Agent Client Collector for information that can help resolve the incidents.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector, IT Operations Management]
---

# View live CI data with Agent Client Collector

View live data for incident-related CIs through Agent Client Collector for information that can help resolve the incidents.

## Before you begin

-   Collecting running processes for a macOS system requires `sudo` privileges. If `sudo` privileges aren't granted, only processes run by the Agent Client Collector are collected.

    To enable `sudo` privileges for osqueryi, add the following strings to either the `/etc/sudoers` file or to an individual file in the `/etc/sudoers.d` directory:

    -   `Cmnd_Alias LIVE_CI_VIEW = /Library/Application\ Support/servicenow/agent-client-collector/osquery/bin/osqueryi`
    -   `_servicenow ALL=(ALL) NOPASSWD:LIVE_CI_VIEW`
-   To enable the OSQuery executable to retrieve information on logged-in users in a Windows environment, the agent must run as a local SYSTEM account.

Verify that you have installed Agent Client Collector Framework and Service Operations Workspace on your instance.

Role required: itil

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  Select the Lists icon \(![Lists icon](../image/lists-icon.png)\).

3.  Select **Incidents** &gt; **All**.

4.  Select an incident from the list.

5.  On the &lt;name of incident&gt; form, select the **Live CI Data** tab.

    The CI data is displayed in the cards described in the following table.

<table id="table_v35_3qv_hsb"><thead><tr><th>

Card

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Device details

</td><td>

General details about the CI.

</td></tr><tr><td>

Memory Usage

</td><td>

Amount of memory being used by the CI.

</td></tr><tr><td>

Top 5 running processes by CPU usage

</td><td>

The five CI processes using the most CPU.

</td></tr><tr><td>

Top 5 running processes by memory usage

</td><td>

The five CI processes using the most memory.

</td></tr><tr><td>

Disk Usage %

</td><td>

Percentage of disk space in use on the CI.

</td></tr><tr><td>

Logged-in users

</td><td>

Users logged in to the CI. Whether this data is visible depends on your OS privileges.-   MacOS: Requires sudo privileges
-   Windows system: Requires administrator privileges
-   Linux: No special privileges are required


</td></tr></tbody>
</table>
**Related topics**  


[View live CI data logs](acc-live-ci-view-logs.md)

[Assign a problematic CI to its incident to view live CI data](acc-live-ci-view-assign-ci.md)

