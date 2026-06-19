---
title: Configure timeline event configurations
description: Create or modify timeline event configurations to control which events appear on the security incident timeline.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/configure-timeline-events-sir.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-05-25"
reading_time_minutes: 2
keywords: [configure timeline events, timeline popover fields]
breadcrumb: [Timeline in Security Incident Response Workspace, Configure, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure timeline event configurations

Create or modify timeline event configurations to control which events appear on the security incident timeline.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace** &gt; **Administration**.

2.  Select **Timeline Event Configuration**.

3.  Select **New** to create a configuration, or open an existing one to modify it.

4.  Fill in the event configuration fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the event as it appears on the timeline.|
    |Description|A brief description of what this event type represents.|
    |Active|When deselected, events of this type do not appear on the timeline.|
    |Event Type|Select **Point** \(single marker at a timestamp\) or **Range** \(bar spanning a start and end time\).|
    |Fetch Type|Select **Table** \(query a table directly\) or **Script** \(use a custom script\). The form fields change based on this selection.|
    |Icon|Icon used to represent this event on the timeline.|
    |Color|Color used to visually distinguish this event type from others.|

    |Field|Description|
    |-----|-----------|
    |Source Table|Table from which to retrieve event data.|
    |SIR Reference Field|Field on the source table that links records to a security incident.|
    |Event Label Field|Field to display as the event label on the timeline.|
    |Additional Filter|Filter conditions to restrict which records appear as events.|
    |Timestamp Field|Date and time field for the position of a point event. Visible when Event Type is Point.|
    |Start Date and Time Field|Date and time field marking the beginning of a range event. Visible when Event Type is Range.|
    |End Date and Time Field|Date and time field marking the end of a range event. Visible when Event Type is Range.|

    |Field|Description|
    |-----|-----------|
    |Script|Server-side script that fetches event data. The script field includes commented template code showing the expected format for both point and range events.|

5.  Select **Save**.

6.  Scroll down to the **Popover Fields** related list.

7.  Select **New** to add a popover field.

8.  Fill in the popover field details and select **Submit**.

    |Field|Description|
    |-----|-----------|
    |Admin Event Configuration|The parent event configuration this popover field belongs to.|
    |Source Table|Automatically populated from the event configuration. Read-only.|
    |Field Name|The field whose value is displayed in the popover.|
    |Label|Display label for this field in the popover.|
    |Is Link|When selected, the field value appears as a clickable link to the related event record.|
    |Order|Sort order in the popover. Lower values appear first.|

    **Note:** For state transition events, the popover automatically displays the state, the previous state \(from/to\), and the duration. Color coding for each state is fixed and consistent across all timelines.


**Parent Topic:**[Timeline in Security Incident Response Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/timeline-sir-workspace.md)

