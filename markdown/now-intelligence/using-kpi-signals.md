---
title: Using KPI Signals
description: When a responsible user receives a signal notification, they either dismiss the signal or reset the baseline.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [KPI Signals, Platform Analytics experience, Platform Analytics]
---

# Using KPI Signals

When a responsible user receives a signal notification, they either dismiss the signal or reset the baseline.

## Overview of responses to KPI Signals notification

A responsible user evaluates the KPI Signals notification. If they determine that the underlying issue is a temporary problem, they fix the problem if appropriate and dismiss the signal. If they determine that the notification is due to a long-term change in the behavior of the underlying business process, they update the baseline that is used to generate a signal.

If it is later determined that it was a mistake to dismiss the signal or update the baseline, a responsible user can undo the action.

![Responsible user's reactions to receiving a notification from KPI Signals. For details, see the following text.](../image/kpi-signals-user-workflow.png "Responses to a KPI Signals notification")

1.  Receive a notification from KPI Signals that an indicator should be examined.
2.  Decide whether the signal is showing a temporary change, possibly due to a problem that can be corrected, or the signal is showing a long-term change in process behavior.
3.  If the change is temporary, address the underlying problem, if appropriate, then dismisses the signal.
4.  If the change is long-term, reset the baseline for generating the signal appropriately.
5.  If the decision turns out to be incorrect, undo it.

## Other use topics

-   **[Reset baseline or dismiss signal](../task/reset-baseline-dismiss-signal.md)**  
When you get a signal that abnormal variation has occurred, either dismiss the signal or recalculate the parameters.
-   **[Revert baseline reset or signal dismissal](../task/revert-reset-dismissal.md)**  
Review previous decisions to reset the KPI Signals baseline or dismiss a signal. Revert the decision if necessary.

**Parent Topic:**[KPI Signals](process-behavior-charts-for-kpis.md)

**Related topics**  


[Exploring KPI Signals](exploring-kpi-signals.md)

[Configuring KPI Signals for an indicator](configuring-kpi-signals.md)

[KPI Signals roles](kpi-signals-roles.md)

