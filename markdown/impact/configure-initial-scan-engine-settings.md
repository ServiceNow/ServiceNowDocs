---
title: Activate Scan Engine and review settings
description: Use Impact Guided Setup to set up the minimum required configuration options in order to run the first system scan.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-11-19"
reading_time_minutes: 2
breadcrumb: [Configure the Impact Store Application, Configuring Impact, Impact]
---

# Activate Scan Engine and review settings

Use Impact Guided Setup to set up the minimum required configuration options in order to run the first system scan.

## Before you begin

[Assign users to Scan Engine groups](assign-users-scan-engine-groups.md) before beginning this task.

**Note:** You can complete the configuration steps directly in the Guided Setup interface, or can configure the properties using the indicate navigation steps.

Role required: Impact admin role or admin

## Procedure

1.  Configure Instance Scanning and allow application access.

    1.  Navigate to **All** &gt; **Impact** &gt; **Guided Setup** &gt; **Impact Platform Health** &gt; **Activate Scan Engine &amp; review settings**.

    2.  On the Scan Engine Properties form, an SE Error banner displays.

        ![The banner to select to activate application access.](../image/scan-engine-operation-banner4.png)

    3.  Select the `sys_update_version` link to navigate to the Application Access tab.

    4.  Select the **Can read** checkbox.

    5.  Select **Save** to continue to activate Scan Engine directly in Scan Engine properties or select **Update** to return to Guided Setup.

2.  Configure Scan Engine Properties to customize and enable initial scan options.

    **Important:** The initial scan sets up the minimum required configuration options to run the first system scan.

<table id="table_lxt_slx_lgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activate Scan Engine

</td><td>

Select the checkbox to set the value to **true**.

</td></tr><tr><td>

Run scheduled scan

</td><td>

-   Select the checkbox to set the value to **true**.
-   Used to schedule a daily scan to run based on the configured scan time and time zone of the settings selected.


</td></tr><tr><td>

Average Developer Rate

</td><td>

Default preferred developer hourly rate in the selected currency to be used for reporting the ROI \(return on investment\) from reducing technical issues.

</td></tr><tr><td>

Configure Scan Engine properties

</td><td>

Review and adjust settings, as each tab has default settings that can be adjusted. See [Configure Scan Engine properties](configure-scan-engine-properties.md) for more information.

</td></tr></tbody>
</table>3.  Select **Mark as Complete** to enable the next step.


## What to do next

[Run your first scan with the Scan Engine](run-scan-engine.md)

**Parent Topic:**[Configure the Impact Store Application](../concept/configuring-impact-platform.md)

**Previous topic:**[Assign users to Scan Engine groups](assign-users-scan-engine-groups.md)

**Next topic:**[Run your first scan with the Scan Engine](run-scan-engine.md)

