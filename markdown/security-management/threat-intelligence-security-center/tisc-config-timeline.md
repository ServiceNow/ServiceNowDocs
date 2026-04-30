---
title: Configure Custom Event Types for Timeline
description: The Timeline component in the investigation canvas provides a chronological overview of all events related to a selected entity. This feature enables analysts to track actions, updates, and changes over time, offering a comprehensive historical perspective of the entity’s activity. As a result, it supports effective temporal threat analysis.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-10-30"
reading_time_minutes: 3
breadcrumb: [Configure Tooltips for Nodemaps, Administer, Threat Intelligence Security Center, Security Operations]
---

# Configure Custom Event Types for Timeline

The Timeline component in the investigation canvas provides a chronological overview of all events related to a selected entity. This feature enables analysts to track actions, updates, and changes over time, offering a comprehensive historical perspective of the entity’s activity. As a result, it supports effective temporal threat analysis.

## Before you begin

Role required: sn\_sec\_tisc.admin

## About this task

As an administrator, you can configure the custom event types to align the timeline with organizational investigative needs, ensuring relevant events are highlighted and improving temporal threat analysis.

Analysts can add, edit, or remove events associated with the intelligence records. The timeline also preserves the user specific date ranges for each canvas providing a consistent and detailed analysis experience. For more information, see [Adding Timeline Events to the Canvas](tisc-add-timeline-events.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Administration** &gt; **Nodemap Controls** &gt; **Timeline Custom Event Type**.

2.  Select **New**.

3.  Fill in the fields as appropriate.

<table id="choicetable_zrg_dgj_fhc"><thead><tr><th align="left" id="d380289e103">

Field

</th><th align="left" id="d380289e106">

Description

</th></tr></thead><tbody><tr><td id="d380289e112">

**Event Name**

</td><td>

A unique name that identifies the specific activity or event occurrence recorded on the timeline.This serves as a primary label for each event, to help you quickly understand the node created, status updated, or any additional details.

</td></tr><tr><td id="d380289e123">

**Description**

</td><td>

Description of the event type to provide context of the event.

</td></tr><tr><td id="d380289e132">

**Status**

</td><td>

Indicates the current status of an event on the timeline.

</td></tr><tr><td id="d380289e141">

**Icon**

</td><td>

An icon that appears on the timeline to visually represent events of this type.

</td></tr><tr><td id="d380289e151">

**Color**

</td><td>

Specifies the color of the icon that represents the event on the timeline.

</td></tr></tbody>
</table>4.  **Save** the custom timeline event configuration.

    **Note:** By default, the custom timeline event is disabled until you manually enable the event.

5.  Navigate to **Timeline Event Configuration** section to add or remove the objects or observables.

    ![Timeline configuration](../image/tisc-config-timeline.png)

6.  Select **Add** to add or edit the entity and applicable table for an object or observable, which means you can now specify which tables the timeline applies to.

7.  Select the **Entity**.

    You can choose to add either an Object or Observable. When an Object is selected, the application displays all the applicable tables associated with it. You can modify the list by adding or removing entries as required.

    On the section **Timeline Event Configuration**, **Included table** field indicates the specific record types to which each an event applies. As an Admin, for example you can remove an entity such as vulnerability from the list if the event should no longer apply to that vulnerability. When an entity of type vulnerability is removed, the event will no longer be triggered for that vulnerability.

    **Note:**

    **Default events for Observables**: Certain events are automatically displayed for specific observables. For example, File observables include the **First Seen** and **Last Seen** fields.

    The system property `sn_sec_tisc.timeline_node_fields` provisioned in the base system that determines which fields are displayed on the timeline.

    By default, it contains the first\_seen and last\_seen fields. You can modify this property to add new fields or remove the existing ones based on your requirements.

    -   When a file observable is added to the Canvas, these events are shown by default.
    -   These default events are not driven by configuration and they appear automatically based on the values populated in the observables record.
    -   If **First Seen** and **Last Seen** contain values, then the corresponding events are displayed on the Canvas without any additional setup.
8.  Select **Save** to confirm your changes.

    Once this is done, you can go back and enable your custom timeline event. This action confirms that the custom timeline event is applicable to the specified tables.

    **Note:**

    After configuration, each event can be either enabled or disabled.

    -   Enabled events are available for the selection within the Investigation Canvas and can be added to relevant nodes.
    -   Disabled events are hidden from the **Add Timeline Event** list and cannot be added to the timeline.

## What to do next

Once the event is configured, you can navigate to the Investigation Canvas to verify the timeline entry and add or edit entries. For more information, see [Adding Timeline Events to the Canvas](tisc-add-timeline-events.md). To understand more about using timeline feature, see [Using Timeline in Investigation Canvas](tisc-timeline-events.md).

