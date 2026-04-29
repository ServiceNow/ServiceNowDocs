---
title: Activate Scan Engine and review settings
description: Use Impact Guided Setup to set up the minimum required configuration options in order to run the first system scan.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure the Impact Store Application, Configuring Impact, Impact]
---

# Activate Scan Engine and review settings

Use Impact Guided Setup to set up the minimum required configuration options in order to run the first system scan.

## Before you begin

[Assign users to Platform Health groups](assign-users-scan-engine-groups.md) before beginning this task.

**Note:** You can complete the configuration steps directly in the Guided Setup interface, or can configure the properties using the indicated navigation steps.

Role required: impact app admin or admin

## Procedure

1.  Configure Instance Scanning and allow application access.

    1.  Navigate to **All** &gt; **Impact** &gt; **Guided Setup** &gt; **Impact Platform Health** &gt; **Activate Scan Engine &amp; review settings**.

    2.  On the Scan Engine Properties form, an SE Error banner displays.

        ![The banner to select to activate application access.](../image/scan-engine-operation-banner4.png)

    3.  Select the `sys_update_version` link to navigate to the Tables page.

        ![The Table updated versions page with the Application Access tab and the Can read check box selected.](../image/guided-setup-app-access.png)

    4.  Select the **Application Access** tab.

    5.  Select the **Can read** checkbox.

    6.  Select **Update**.

2.  Navigate to **All** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine Properties** &gt; **.**

3.  Configure Scan Engine Properties to customize and enable as depicted in the table.

    |Field|Value|Description|
    |-----|-----|-----------|
    |Activate Scan Engine|Select the checkbox to set the value to **true**.|Turns on the Scan Engine feature.|
    |Run scheduled scan|Select the checkbox to set the value to **true**.|Used to schedule a daily scan to run based on the configured scan time and time zone of the settings selected.|
    |Average Developer Rate|Set an hourly rate in the selected currency.|Default preferred developer hourly rate in the selected currency to be used for reporting the ROI \(return on investment\) calculated with the quantity of reduced technical issues.|
    |Configure Platform Health Scan Engine properties|Review each tab to understand the default defined behavior or opt to reconfigure settings.|Review and adjust settings, as each tab has default settings that can be adjusted. See [Configure Scan Engine properties](configure-scan-engine-properties.md) for more information.|

4.  Select **Run your first scan** to enable the next step.

    **Important:** The initial setup configures the minimum required options to run the first system scan.


## What to do next

[Run your first scan with the Scan Engine](run-scan-engine.md)

**Parent Topic:**[Configure the Impact Store Application](../concept/configuring-impact-platform.md)

**Previous topic:**[Assign users to Platform Health groups](assign-users-scan-engine-groups.md)

**Next topic:**[Run your first scan with the Scan Engine](run-scan-engine.md)

