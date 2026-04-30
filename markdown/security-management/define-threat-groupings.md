---
title: Define threat groupings
description: Define threat groupings as objects that have a shared context.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Threat groupings, IoC Repository, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Define threat groupings

Define threat groupings as objects that have a shared context.

## Before you begin

Role required: sn\_ti.admin

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **IoC Repository** &gt; **Threat Groupings**.

2.  Click **New**.

3.  Complete the fields in the form as appropriate.

    |Field|Description|
    |-----|-----------|
    |**Name**|Enter a name to identify the threat grouping.|
    |**Context**|A description of the particular context shared by the content referenced by the grouping.|
    |**Source**|Specifies the threat source from which this record is created.|
    |**Description**|A short description that provides details and context about the grouping. This includes its purpose and its key characteristics.|
    |**Source ID**|Unique identifier for this object in the threat source.|
    |**Created Time in Source**|Specifies the time the object is created in the source.|
    |**Modified Time in Source**|Specifies the time the object is modified in the source.|

4.  Click **Submit**.


## What to do next

Click any of the following related lists to view additional information about objects associated with the threat grouping.

<table id="table_dpt_3rd_xmb"><thead><tr><th>

Related Links and Related Lists

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show Relationships

</td><td>

Opens the STIX Visualizer where you can view the relationship of the STIX object.Show Relationships appears only when the object has an associated object.

</td></tr><tr><td>

Grouped Objects

</td><td>

Lists objects grouped as part of the threat grouping.

</td></tr><tr><td>

Grouped Indicators

</td><td>

Lists indicators grouped as part of the threat grouping.

</td></tr><tr><td>

Grouped Observables

</td><td>

Lists observables grouped as part of the threat grouping.

</td></tr></tbody>
</table>**Parent Topic:**[Threat groupings](../concept/threat-groupings.md)

