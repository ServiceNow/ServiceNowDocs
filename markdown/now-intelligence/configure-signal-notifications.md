---
title: Configure signal notifications
description: As a responsible user, you receive email reminders about signals that have not been resolved. You can configure how frequently you get these reminders and the maximum number of reminders to get for a signal.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [KPI Signals, Platform Analytics]
---

# Configure signal notifications

As a responsible user, you receive email reminders about signals that have not been resolved. You can configure how frequently you get these reminders and the maximum number of reminders to get for a signal.

## Before you begin

Role required: admin, or must be a responsible user

## About this task

As a responsible user, you receive email notifications in the following circumstances:

-   A new signal is detected on a KPI that you are responsible for.
-   No signal has been detected on a KPI long enough for it to be considered long-term stable \(an "anti-signal"\).
-   A signal for a KPI you are responsible for is resolved \(baseline reset or dismissal\).
-   A signal for a KPI you are responsible for has not been resolved, according to subsequent signal collection jobs.

In this last case, you can set how frequently a KPI is checked for resolution. You can also set the maximum number of reminders you get.

## Procedure

1.  Open KPI Signals for a KPI.

2.  Click the cogwheel to open the Configuration options.

    ![KPI Signals panel showing the cogwheel button for opening configuration settings](../image/kpi-signals-open-settings.png)

3.  Open the Notifications tab.

    You see a list of all the KPIs that you are responsible for on this indicator. KPI refers to the combination of the indicator with any breakdown elements.

4.  Select the KPIs that you want to edit.

    If you select one KPI, its settings appear in the **Editing configuration items** panel. If you select more than one KPI, only the values that are the same for all these KPIs appear in the panel. When you enter the new values in that panel, they apply to all selected KPIs.

    ![Notifications tab of KPI Signals Configuration, showing multiple KPIs selected and no values in the Editing panel](../image/kpi-signals-notification-config-2-kpi.png)

5.  Set the interval between getting reminders about unresolved signals.

6.  Set the count of the maximum number of reminders you want to receive about an unresolved signal.

7.  Set the anti-signal factor.

    This factor helps determine when a KPI is stable enough to generate an "anti-signal," according to the following formula:

    ```
    Length of time to calculate the baseline for the KPI * Anti-signal factor
    ```

    The default anti-signal factor is two. Set this factor if you decide it needs to be changed. For more information, see [Signal, no signal, and anti-signal](../concept/signal-no-signal-anti-signal.md).

8.  Click **Save**.


