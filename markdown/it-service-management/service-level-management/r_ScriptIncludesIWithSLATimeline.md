---
title: Script includes installed with SLA timeline
description: When SLA timeline is activated, script includes are installed.
locale: en-US
release: zurich
product: Service Level Management
classification: service-level-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Activate SLA timeline, Plugins, Configure, Service Level Management, IT Service Management]
---

# Script includes installed with SLA timeline

When SLA timeline is activated, script includes are installed.

SLA timeline adds the following script includes.

|Script include|Description|
|--------------|-----------|
|SLATimeline|This script include generates the timeline data for a task SLA record by replaying the task’s history and using the SLATimelineAPI to determine the appropriate stage transitions and timings for the task SLA.|
|SLATimelineAPI|This script include provides a number of functions that simulate how the SLA engine processes a particular task and SLA definition without actually creating any task SLA records.|
|SLATimeLineV2SNC|This script include is used by SLA Timeline internal REST API to inspect audit history of a Task and extract task SLA details to be presented on the UI.|
|ReadOnlyTaskSLAContoller|This script include is a helper script include and is for internal use. This script include is called by SLATimeLineV2SNC to process the task SLA stage details.|

**Parent Topic:**[Activate SLA timeline](../task/t_ActivateSLATimeline.md)

