---
title: Configure signals for breakdown elements
description: Configure signal detection and assign responsibility for multiple breakdowns and breakdown elements on one indicator.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, KPI Signals, Platform Analytics experience, Platform Analytics]
---

# Configure signals for breakdown elements

Configure signal detection and assign responsibility for multiple breakdowns and breakdown elements on one indicator.

## Before you begin

An administrator must activate KPI Signals for the indicator. For more information, see [Activate KPI Signals monitoring for an indicator \(KPI\)](activate-signals-monitor.md).

Role required: responsible user for the indicator or admin.

## About this task

For example, KPI Signals could simultaneously monitor the following indicators and breakdowns:

-   Number of open incidents \(no breakdown\)
-   Number of open incidents, Priority = 1-Critical
-   Number of open incidents, Priority = 2-High
-   Number of open incidents, Category = Software

However, KPI Signals could not monitor "Number of open incidents, Priority = 1-Critical, Category = Software."

## Procedure

1.  Open KPI Signals for the indicator, without first selecting a filtering breakdown in KPI Details.

2.  Click the cogwheel to open the Configuration options.

    ![KPI Signals panel showing the cogwheel button for opening configuration settings](../image/kpi-signals-open-settings.png)

3.  Click **Add breakdowns**.

    The **Add Breakdowns** dialog opens.

4.  Click in the Breakdowns field and select a breakdown.

    A list of elements for the breakdown appears.![Animation showing a breakdown being selected.](../image/kpi-signals-add-breakdown.gif)

5.  Click **Filter** and use the condition builder to build a filter for the elements.

6.  Select at least one element and click **Add**

7.  To monitor signals on elements of another breakdown, click **Add breakdowns** again and repeat the steps.

8.  In the Signal Detection tab, activate monitoring for the KPIs and set the baseline start and number of scores required to calculate the baseline.

    For more information about the settings on the Signal Detection tab, see [Configure signal detection](configure-signal-detection.md).

9.  Open the Responsibility tab and assign a responsible user to each KPI.

    For more information about responsible users and the settings on the Responsibility tab, see [Configure responsibility for KPI Signals](../concept/kpi-signals-responsible-users.md#).

10. Open the Notifications tab and set how often the responsible user should get an email notification for an unresolved signal.

    You can also set the total number of reminders the responsible user gets for an unresolved signal. Also set the anti-signal factor, which is used to calculate how many scores without a signal result in an anti-signal. For more information about anti-signals, see [Signal, no signal, and anti-signal](../concept/signal-no-signal-anti-signal.md). For more information about the settings on the Notifications tab, see [Configure signal notifications](configure-signal-notifications.md).


**Parent Topic:**[Configuring KPI Signals for an indicator](../concept/configuring-kpi-signals.md)

