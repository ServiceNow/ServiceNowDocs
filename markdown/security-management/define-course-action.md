---
title: Define a course of action
description: Define a course of action to prevent an attack or to respond to an attack that is in progress.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Course of actions, IoC Repository, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Define a course of action

Define a course of action to prevent an attack or to respond to an attack that is in progress.

## Before you begin

Role required: sn\_ti.admin

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **IoC Repository** &gt; **Course of Actions**.

2.  Click **New**.

3.  Complete the fields in the form as appropriate.

    |Field|Description|
    |-----|-----------|
    |**Name**|Enter a descriptive name for this course of action.|
    |**Action**|To capture structured or automated courses of action.|
    |**Source**|Specifies the threat source from which this record is created.|
    |**Description**|A description that provides more details and context about the course of action, potentially including its purpose and its key characteristics.|
    |**Source ID**|Unique identifier for this object in the threat source.|
    |**Created Time in Source**|Specifies the time the object is created in the source.|
    |**Modified Time in Source**|Specifies the time the object is modified in the source.|

4.  Click **Submit**.


## What to do next

Click any of the following related lists to view additional information about objects associated with the course of action.

<table id="table_zdn_szf_wmb"><thead><tr><th>

Related Links

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show Relationships

</td><td>

Opens the STIX Visualizer where you can view the relationship of the STIX object.Show Relationships appears only when the object has an associated object.

</td></tr><tr><td>

External References

</td><td>

Lists external references which refer to non-STIX information. This property is used to provide one or more external object identifiers.

</td></tr><tr><td>

Attack Patterns

</td><td>

Lists the attack patterns that help categorize attacks that are associated with this object.

</td></tr><tr><td>

Indicators

</td><td>

Lists related Indicators of Compromise \(IoC\) that have been identified by the threat source associated with this object.

</td></tr><tr><td>

Malware

</td><td>

Lists malicious code associated with this object.

</td></tr><tr><td>

Tools

</td><td>

Lists legitimate software that is used by threat actors to perform attacks associated with this object.

</td></tr><tr><td>

Vulnerabilities

</td><td>

Lists a weakness or defect in a software or hardware that attackers exploit which is associated with this object.

</td></tr></tbody>
</table>**Parent Topic:**[Course of actions](../concept/threat-intelligence-course-actions.md)

