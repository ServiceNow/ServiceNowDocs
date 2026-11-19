---
title: Activate Scan Engine and review settings
description: Set up the minimum required configuration options to run the first system scan.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/configure-initial-scan-engine-settings.html
release: brazil
topic_type: task
last_updated: "2026-11-10"
reading_time_minutes: 2
breadcrumb: [Configuring Impact, Impact]
---

# Activate Scan Engine and review settings

Set up the minimum required configuration options to run the first system scan.

## Before you begin

Navigation differs depending on whether you're using the [Impact Setup Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/use-impact-setup-hub.md) or the legacy [Guided Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/guided-setup-impact-in-app.md). See whichever applies for the exact path.

[Assign roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/assign-roles.md) before beginning this task.

Role required: sn\_impact\_common.Impact\_App\_Admin or admin

## About this task

Complete the minimum required configuration to run your first scan. After the initial setup, review the additional scanning functionality to configure the optimal setup for your organization.

## Procedure

1.  Configure Instance Scanning and allow application access.

    1.  On the Scan Engine Properties form, an SE Error banner displays.

        \[Omitted image "scan-engine-operation-banner4.png"\] Alt text: The banner to select to activate application access.

    2.  Select the Updated Versions \[sys\_update\_version\] table link to navigate to the Tables page.

        \[Omitted image "guided-setup-app-access.png"\] Alt text: The Table updated versions page with the Application Access tab and the Can read check box selected.

    3.  Select the **Application Access** tab.

    4.  Select the **Can read** check box.

    5.  Select **Update**.

2.  Navigate to **All** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine Properties**.

3.  Configure the following Scan Engine Properties.

    |Field|Value|Description|
    |-----|-----|-----------|
    |Activate Scan Engine|Select the check box to set the value to **true**.|Turns on the Scan Engine feature.|
    |Run scheduled scan|Select the check box to set the value to **true**.|Used to schedule a daily scan to run based on the configured scan time and time zone of the settings selected.|
    |Average Developer Rate|Set an hourly rate in the selected currency.|Default preferred developer hourly rate in the selected currency, used for reporting the return on investment \(ROI\) calculated from the quantity of reduced technical issues.|
    |Configure Platform Health Scan Engine properties|Review each tab to understand the default defined behavior or opt to reconfigure settings.|Review and adjust settings. Each tab has default settings that can be reconfigured.|

4.  Select **Run your first scan** to enable the next step.

    See [Run Scan Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/run-scan-engine.md) to run your first scan.


## What to do next

To further adjust Scan Engine behavior, review the additional scanning configuration options at [Configure Scan Engine properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configure-scan-engine-properties.md)

-   **[Scan Engine properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-properties-overview.md)**  
Use Scan Engine properties to control when scans run, what they cover, who sees findings, and how your teams govern code before it moves to production.
-   **[Scan Engine integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/instance-integration-scan-engine.md)**  
Scan Engine integrates with other ServiceNow instances and external agile systems to synchronize definitions, manage exception reasons, create user stories, and enforce governance over app deployments.

**Parent Topic:**[Configuring Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configuring-impact-platform.md)

**Previous topic:**[Create a development team](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/create-development-team.md)

**Next topic:**[Scan Engine properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-properties-overview.md)

