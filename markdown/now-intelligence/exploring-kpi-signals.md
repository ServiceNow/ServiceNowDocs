---
title: Exploring KPI Signals
description: KPI Signals notifies you when the behavior of a process changes significantly. This feature applies standard statistical Process Behavior Charts to Performance Analytics indicators.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [KPI Signals, Platform Analytics experience, Platform Analytics]
---

# Exploring KPI Signals

KPI Signals notifies you when the behavior of a process changes significantly. This feature applies standard statistical Process Behavior Charts to Performance Analytics indicators.

## KPI Signals overview

**Tip:** A free training for KPI Signals is available from the [NOW Learning Center](https://nowlearning.service-now.com/lxp?id=overview&sys_id=674f2e4b1bea74d4c4b69683b24bcbe2&type=course).

Every process undergoes variation. Most of this variation is normal, or 'common cause' variation, such as the small differences between each time you sign your name. What you need to know about is abnormal, or 'special cause' variation, such as when you sign with your off hand. KPI Signals lets you know when abnormal variation is occurring. KPI Signals incorporates Process Behavior Charts. These charts use standard statistical methods to pick out the signal of special cause variation from the noise of common cause variation.

KPI Signals uses standard 3-sigma parameters. "Three-sigma" means that the indicator scores for the process are expected almost always to remain within three standard deviations of the norm. The charts require at least five consecutive scores to calculate parameters.

## KPI Signals users

|User|Description|
|----|-----------|
|Process owner|Requests signals monitoring on an indicator in the following circumstances: The indicator is important enough that the process owner wants to know if the trends deteriorate significantly and wants to be notified of this off-platform. However, the process owner does not want to track the trends continuously. Instead, they want the system to inform them when they need to look more closely. Alternatively, the process owner wants to catch the trend early in the process, before it is bad enough to be obvious to the human eye.|
|KPI Signals administrator|Sets up KPI Signals for an indicator at the request of the process owner. Also assigns responsible users for the indicator, generally also at the request of the process owner.|
|Responsible user|Receives signal notifications and acts upon them. The process owner is usually the key responsible user, but they can delegate this responsibility to other users as well.|

## KPI Signals workflow

The following diagram shows the workflow for setting up KPI Signals for a Performance Analytics indicator, and the workflow for responding to a signal notification.

![How an administrator sets up KPI Signals for an indicator, and the steps a responsible user takes after receiving a signal. For details, refer to the following description.](../image/kpi-signals-workflow.png "Setting up and using KPI Signals")

1.  Process owner requests an administrator to enable KPI Signals for an indicator.
2.  Administator makes themselves a responsible user for the indicator. Doing so activates KPI Signals monitoring for the indicator.
3.  Administrator sets start date for monitoring indicator.
4.  Administrator adds other responsible users.
5.  Responsible user receives a notification from KPI Signals that an indicator should be examined.
6.  Responsible user decides whether the signal is showing a temporary change, possibly due to a problem that can be corrected, or the signal is showing a long-term change in process behavior.
7.  If the change is temporary, the responsible user addresses the underlying problem, if appropriate, then dismisses the signal.
8.  If the change is long-term, the responsible user resets the baseline for generating the signal appropriately.

## Other exploration topics

-   **[Signal, no signal, and anti-signal](signal-no-signal-anti-signal.md)**  
When KPI Signals detects abnormal variation in the scores of a KPI, it generates a signal. When KPI Signals does not detect abnormal variation for a significant amount of time, it generates an "anti-signal." The anti-signal lets you know that your workflow is under control.
-   **[View KPI Signals](../task/view-kpi-signals.md)**  
Access KPI Signals from the KPI Details page.

**Parent Topic:**[KPI Signals](process-behavior-charts-for-kpis.md)

**Related topics**  


[Configuring KPI Signals for an indicator](configuring-kpi-signals.md)

[Using KPI Signals](using-kpi-signals.md)

[KPI Signals roles](kpi-signals-roles.md)

