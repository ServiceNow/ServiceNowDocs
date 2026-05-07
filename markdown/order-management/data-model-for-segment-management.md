---
title: Data model for Segment Management
description: The Segment Management data model provides a framework to map customers to specific segments to track partner progression toward the next tier.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [Configure Segment Management, Configure Partner Relationship Management, Configure, Sales Customer Relationship Management]
---

# Data model for Segment Management

The Segment Management data model provides a framework to map customers to specific segments to track partner progression toward the next tier.

With the segment admin \(sn\_seg.segment\_mgmt\_admin\) role, you can add data in the segment \(sn\_seg\_segment\) table to create and manage multiple segments.

<table id="table_fzd_ms1_fhc"><thead><tr><th>

Field

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

String

</td><td>

Auto-generated number associated with the segment.

</td></tr><tr><td>

Name

</td><td>

Translated text

</td><td>

Name of the segment.

</td></tr><tr><td>

Description

</td><td>

Translated text

</td><td>

Description of the segment.

</td></tr><tr><td>

Active

</td><td>

True/False

</td><td>

Current state of the segment, whether active or not.

</td></tr><tr><td>

Order

</td><td>

Number

</td><td>

Order of the segment.

</td></tr><tr><td>

Status

</td><td>

Choice -   Draft
-   Approved
-   Rejected
-   Retired

</td><td>

Status to manage the life cycle of the segment.

</td></tr><tr><td>

Work notes

</td><td>

Journal input

</td><td>

Important information associated with the segment.

</td></tr><tr><td>

Domain

</td><td>

Domain ID

</td><td>

Domain to which the segment belongs.

</td></tr></tbody>
</table>## Configuration tasks for Segment Management

Perform the following configuration tasks to set up the data model tables to establish an association between segment management and Partner Relationship Management.

-   [Configure Program Segment Mapping](../task/configure-program-segment-mapping.md)
-   [Configure Program Segment Criteria](../task/configure-program-segment-criteria.md)
-   [Configure Program Criteria](../task/configure-program-criteria.md)

**Parent Topic:**[Configure Segment Management](configure-segment-management.md)

**Related topics**  


[Install Segment Management](../task/install-segment-management.md)

[Roles and components of Segment Management](roles-and-components-of-segment-management.md)

