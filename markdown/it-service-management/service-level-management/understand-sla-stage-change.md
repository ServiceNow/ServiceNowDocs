---
title: Use SLA timeline to understand SLA stage change
description: Describes how you can understand SLA stage changes using SLA timeline.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/service-level-management/understand-sla-stage-change.html
release: zurich
product: Service Level Management
classification: service-level-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SLA timeline, Reference, Service Level Management, IT Service Management]
---

# Use SLA timeline to understand SLA stage change

Describes how you can understand SLA stage changes using SLA timeline.

Using Task SLA-2 as an example, you can see a period of retroactive and out of schedule time preceding the task update that caused the SLA to attach to INC0010001. The task update is represented by the first triangle. When this event is selected, the detail pane displays and the Start tab has a blue check and is highlighted indicating this is the SLA Definition condition this event met and the task values which matched the SLA Definition start condition.

\[Omitted image "understand-sla-stage-change-1.png"\] Alt text: Start stage

When the second task update represented by the second black triangle, which triggered an SLA stage change occurs, you can see that it triggers a pause condition. If you select this event in the timeline, the detail pane displays the highlighted Pause that contains a blue check indicating a match. Once again, the task values which match the SLA Definition condition are displayed so you easily know why the stage change occurred.

\[Omitted image "understand-sla-stage-change-2.png"\] Alt text: Pause stage

Similarly, when the third task update which triggers a stage change occurs, you can see this resumes the SLA. When that update is clicked, the Stage details section highlights the Resume tab which now contains a blue check and provides detailed information about the task update that occurred and the SLA conditions those updates matched.

\[Omitted image "understand-sla-stage-change-3.png"\] Alt text: Resume stage

The SLA continues to accumulate time, until it is breached and this is visually represented by the yellow, orange, and the red colors. Eventually, another task update occurs which triggers the SLA’s cancel conditions that is represented by the white diamond. The Stage details section highlights the conditions for the task SLA cancellation. In this case, the SLA Definition is defined to cancel when the ‘Start conditions are not met’.

\[Omitted image "understand-sla-stage-change-4.png"\] Alt text: Cancel stage

**Parent Topic:**[SLA timeline](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/service-level-management/c_SLATimeline.md)

