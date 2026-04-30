---
title: Exploring chronological data on the alerts in an alert group in Express List
description: Visualize the chronological sequence of events within an alert group in Express List using the Timeline view. This feature provides a comprehensive overview of when the alerts occurred, their severity changes, and other pertinent data for efficient triage and Mean Time to Resolution \(MTTR\).
locale: en-US
release: yokohama
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Express List in the Service Operations Workspace for ITOM, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Exploring chronological data on the alerts in an alert group in Express List

Visualize the chronological sequence of events within an alert group in Express List using the Timeline view. This feature provides a comprehensive overview of when the alerts occurred, their severity changes, and other pertinent data for efficient triage and Mean Time to Resolution \(MTTR\).

In Timeline view, each alert is represented by a bar, enabling you to quickly discern the order of occurrence, severity transitions, and closure status. The timeline begins with the creation of the first alert and extends to the present moment.

![Sample timeline view in Express List.](../image/el-timeline-view.png "Sample timeline view")

Standard severity colors are used in the bars, with gray segments indicating periods before alert creation or after its closure. Hovering over a severity bar reveals a tooltip with key alert details.

|Color|Severity|
|-----|--------|
|![Red used to represent Critical severity in the alert severity bar.](../image/el-timeline-red.png)|Critical|
|![Orange used to represent Major severity in the alert severity bar.](../image/el-timeline-orange.png)|Major|
|![Yellow used to represent Minor severity in the alert severity bar.](../image/el-timeline-yellow.png)|Minor|
|![Blue used to represent Warning severity in the alert severity bar.](../image/el-timeline-blue.png)|Warning|
|![Green used to represent OK in the alert severity bar.](../image/el-timeline-green.png)|OK|

The title of the Timeline view for an alert group summarizes the group's description, number, state, severity, and grouping type, derived from the primary alert. Detailed information including alert number, state, severity, a brief description, and associated Configuration Item \(CI\) or node, when available, is displayed for each alert within the group.

**Related topics**  


[View a timeline of the alerts in an alert group](../task/el-timeline-view.md)

