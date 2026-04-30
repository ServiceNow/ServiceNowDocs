---
title: KPI Signals
description: KPI Signals notifies you when the behavior of a process changes significantly. This feature applies standard statistical Process Behavior Charts to Performance Analytics indicators.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Platform Analytics]
---

# KPI Signals

KPI Signals notifies you when the behavior of a process changes significantly. This feature applies standard statistical Process Behavior Charts to Performance Analytics indicators.

**Tip:** A free training for KPI Signals is available from the [NOW Learning Center](https://nowlearning.service-now.com/lxp?id=overview&sys_id=674f2e4b1bea74d4c4b69683b24bcbe2&type=course).

Every process undergoes variation. Most of this variation is normal, or 'common cause' variation, such as the small differences between each time you sign your name. What you need to know about is abnormal, or 'special cause' variation, such as when you sign with your off hand. KPI Signals lets you know when abnormal variation is occurring. KPI Signals incorporates Process Behavior Charts. These charts use standard statistical methods to pick out the signal of special cause variation from the noise of common cause variation.

KPI Signals uses standard 3-sigma parameters. "Three-sigma" means that the indicator scores for the process are expected almost always to remain within three standard deviations of the norm. The charts require at least five consecutive scores to calculate parameters.

## Disabling KPI Signals

KPI Signals is activated by default. If you do not want this feature, request a ServiceNow AI Platform administrator to set the property **com.snc.pa.activate\_kpi\_signals** to **false**. Because this property does not exist by default, the administrator must add it. You can refer them to [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Important:** If you reactivate KPI Signals, signal detection resumes from the time you originally deactivated the feature, not from the time you reactivated it.

