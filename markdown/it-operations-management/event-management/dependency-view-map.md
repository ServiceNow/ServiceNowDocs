---
title: View the Dependency map for CMDB alerts
description: The Dependency map illustrates how and why alerts are grouped, simplifying troubleshooting and issue management. It reveals connections between CIs within a CMDB alert group, enhancing visibility into their relationships. Additionally, if a CI is not part of the group but connects to other alert CIs, it remains visible on the map, aiding alert resolution and proactive management.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [CMDB based alert grouping, Alert grouping types and creation methods, Alert grouping, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# View the Dependency map for CMDB alerts

The Dependency map illustrates how and why alerts are grouped, simplifying troubleshooting and issue management. It reveals connections between CIs within a CMDB alert group, enhancing visibility into their relationships. Additionally, if a CI is not part of the group but connects to other alert CIs, it remains visible on the map, aiding alert resolution and proactive management.

## Before you begin

Role required: evt\_mgmt\_user, evt\_mgmt\_operator

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **All Alerts**.

2.  Search for the CMDB group.

3.  Open a CMDB group alert.

4.  Scroll down and select the **Activities** tab.

    You may see a message similar to the following:

    `Alert2405199 and Alert2405219 were grouped together because of CI relationships. Open Dependency Map for CMDB Group Alerts. Open Dependency Map for CMDB Group Alerts`.

    ![Select the link to view dependency map.](../image/open-dependency-map.png)

5.  Select the link to see the dependency view of the CMDB alerts.

    ![View dependency map for CMDB alerts.](../image/view-dependency-map.png)


