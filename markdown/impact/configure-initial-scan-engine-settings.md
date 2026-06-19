---
title: Activate Scan Engine and review settings
description: Use Impact Guided Setup to set up the minimum required configuration options in order to run the first system scan.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/configure-initial-scan-engine-settings.html
release: australia
product: Impact
classification: impact
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure the Impact Store Application, Configuring Impact, Impact]
---

# Activate Scan Engine and review settings

Use Impact Guided Setup to set up the minimum required configuration options in order to run the first system scan.

## Before you begin

[Assign users to Platform Health groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/assign-users-scan-engine-groups.md) before beginning this task.

**Note:** You can complete the configuration steps directly in the Guided Setup interface, or can configure the properties using the indicated navigation steps.

Role required: impact app admin or admin

## Procedure

1.  Configure Instance Scanning and allow application access.

    1.  Navigate to **All** &gt; **Impact** &gt; **Guided Setup** &gt; **Impact Platform Health** &gt; **Activate Scan Engine &amp; review settings**.

    2.  On the Scan Engine Properties form, an SE Error banner displays.

        \[Omitted image "scan-engine-operation-banner4.png"\] Alt text: The banner to select to activate application access.

    3.  Select the `sys_update_version` link to navigate to the Tables page.

        \[Omitted image "guided-setup-app-access.png"\] Alt text: The Table updated versions page with the Application Access tab and the Can read check box selected.

    4.  Select the **Application Access** tab.

    5.  Select the **Can read** checkbox.

    6.  Select **Update**.

2.  Navigate to **All** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine Properties** &gt; **.**

3.  Configure Scan Engine Properties to customize and enable as depicted in the table.

<table id="table_lxt_slx_lgc"><thead><tr><th>

Field

</th><th>

Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activate Scan Engine

</td><td>

Select the checkbox to set the value to **true**.

</td><td>

Turns on the Scan Engine feature.

</td></tr><tr><td>

Run scheduled scan

</td><td>

Select the checkbox to set the value to **true**.

</td><td>

Used to schedule a daily scan to run based on the configured scan time and time zone of the settings selected.

</td></tr><tr><td>

Average Developer Rate

</td><td>

Set an hourly rate in the selected currency.

</td><td>

Default preferred developer hourly rate in the selected currency to be used for reporting the ROI \(return on investment\) calculated with the quantity of reduced technical issues.

</td></tr><tr><td>

Configure Platform Health Scan Engine properties

</td><td>

Review each tab to understand the default defined behavior or opt to reconfigure settings.

</td><td>

Review and adjust settings, as each tab has default settings that can be adjusted. **Important:** See [Configure Scan Engine properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-scan-engine-properties.md) for more information.

</td></tr></tbody>
</table>4.  Select **Run your first scan** to enable the next step.

    **Important:** The initial setup configures required options to run the first system scan. Subsequent configuration may occur to adjust Scan Engine behavior.


-   **[Configure Scan Engine properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-scan-engine-properties.md)**  
Configure the primary scanning capabilities and configuration options for scheduled, on-demand and real-time scans.

**Parent Topic:**[Configure the Impact Store Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configuring-impact-platform.md)

**Previous topic:**[Assign users to Platform Health groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/assign-users-scan-engine-groups.md)

**Next topic:**[Configure Scan Engine properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-scan-engine-properties.md)

