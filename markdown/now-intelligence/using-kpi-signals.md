---
title: Using KPI Signals
description: When a responsible user receives a signal notification, they either dismiss the signal or reset the baseline.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/using-kpi-signals.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [KPI Signals, Platform Analytics experience, Platform Analytics]
---

# Using KPI Signals

When a responsible user receives a signal notification, they either dismiss the signal or reset the baseline.

## Overview of responses to KPI Signals notification

A responsible user evaluates the KPI Signals notification. If they determine that the underlying issue is a temporary problem, they fix the problem if appropriate and dismiss the signal. If they determine that the notification is due to a long-term change in the behavior of the underlying business process, they update the baseline that is used to generate a signal.

If it is later determined that it was a mistake to dismiss the signal or update the baseline, a responsible user can undo the action.

\[Omitted image "kpi-signals-user-workflow.png"\] Alt text: Responsible user's reactions to receiving a notification from KPI Signals. For details, see the following text.

1.  Receive a notification from KPI Signals that an indicator should be examined.
2.  Decide whether the signal is showing a temporary change, possibly due to a problem that can be corrected, or the signal is showing a long-term change in process behavior.
3.  If the change is temporary, address the underlying problem, if appropriate, then dismisses the signal.
4.  If the change is long-term, reset the baseline for generating the signal appropriately.
5.  If the decision turns out to be incorrect, undo it.

## Other use topics

-   **[Reset baseline or dismiss signal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/reset-baseline-dismiss-signal.md)**  
When you get a signal that abnormal variation has occurred, either dismiss the signal or recalculate the parameters.
-   **[Revert baseline reset or signal dismissal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/revert-reset-dismissal.md)**  
Review previous decisions to reset the KPI Signals baseline or dismiss a signal. Revert the decision if necessary.

**Parent Topic:**[KPI Signals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-behavior-charts-for-kpis.md)

**Related topics**  


[Exploring KPI Signals]()

[Configuring KPI Signals for an indicator]()

[KPI Signals roles]()

