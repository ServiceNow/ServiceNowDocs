---
title: Define threat opinions
description: Define threat opinions as an assessment of the accuracy of the information in a STIX object.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Threat opinions, IoC Repository, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Define threat opinions

Define threat opinions as an assessment of the accuracy of the information in a STIX object.

## Before you begin

Role required: sn\_ti.admin

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **IoC Repository** &gt; **Threat Opinions**.

2.  Click **New**.

3.  Complete the fields in the form as appropriate.

    |Field|Description|
    |-----|-----------|
    |**Opinion**|The producer's opinion about the STIX object.|
    |**Explanation**|The producer's explanation about the opinion.|
    |**Authors**|Specifies the name of the author \(example, an analyst\).|
    |**Source**|Specifies the threat source from which this record is created.|
    |**Source ID**|Unique identifier for this object in the threat source.|
    |**Created Time in Source**|Specifies the time the object is created in the source.|
    |**Modified Time in Source**|Specifies the time the object is modified in the source.|

4.  Click **Submit**.


## What to do next

Click any of the following related lists to view additional information about objects associated with the threat opinion.

<table id="table_wlq_2td_xmb"><thead><tr><th>

Related Links and Related Lists

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show Relationships

</td><td>

Opens the STIX Visualizer where you can view the relationship of the STIX object.Show Relationships appears only when the object has an associated object.

</td></tr><tr><td>

Associated Objects

</td><td>

List of objects the threat opinion applies to.

</td></tr><tr><td>

Associated Indicators

</td><td>

List of indicators the threat opinion applies to.

</td></tr><tr><td>

Associated Observables

</td><td>

Lists observables associated with this object.

</td></tr></tbody>
</table>**Parent Topic:**[Threat opinions](../concept/threat-opinions.md)

