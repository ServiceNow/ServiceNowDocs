---
title: Tables installed with Privacy Management
description: Tables are added with activation of GRC: Privacy Management.
locale: en-US
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Privacy Management, Governance, Risk, and Compliance]
---

# Tables installed with Privacy Management

Tables are added with activation of GRC: Privacy Management.

<table id="table_kf4_nqk_qjb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assessment configuration

 \[sn\_privacy\_assessment\_configuration\]

</td><td>

Privacy manager or admin can configure the rules for auto creating the processing activity on an assessment response. This table stores the assessment configuration rules on assessment template.

</td></tr><tr><td>

Control Objective to Processing Activity

 \[sn\_privacy\_m2m\_policy\_statement\_processing\_activity\]

</td><td>

Each processing activity can be associated to the applicable control objectives. This table enables tracking the processing activity to CO relationships.

</td></tr><tr><td>

Control to Processing Activity

 \[sn\_privacy\_m2m\_control\_processing\_activity\]

</td><td>

Stores many-to-many relationships between controls and processing activity.

</td></tr><tr><td>

Entity Type to Assessment Instance

 \[sn\_privacy\_m2m\_profile\_type\_assessment\_instance\]

</td><td>

Privacy users can send multiple privacy assessments on Entity Type. This table enables the privacy assessments to processing activity relationships.

</td></tr><tr><td>

Information object to processing activity

 \[sn\_privacy\_m2m\_information\_object\_processing\_activity\]

</td><td>

Each processing activity can be associated to applicable Information objects. This table enables tracking the processing activity to IO relationships.

</td></tr><tr><td>

Privacy Unique User Usage

 \[sn\_privacy\_unique\_user\_usage\]

</td><td>

Collects the unique count of users who are using GRC Privacy Management tables.

</td></tr><tr><td>

Processing activity

 \[sn\_privacy\_processing\_activity\]

</td><td>

Extends task table \[sn\_grc\_item\] and stores processing activities.

</td></tr><tr><td>

Processing activity hierarchy

 \[sn\_privacy\_m2m\_pa\_pa\]

</td><td>

Personal data can be moved from one processing activity to another processing activity. This table stores the upstream and downstream processing activities information for each processing activity.

</td></tr></tbody>
</table>**Parent Topic:**[Privacy Management reference](privacy-mgmt-reference.md)

