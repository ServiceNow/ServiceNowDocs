---
title: Define an intrusion set
description: Define an intrusion set that is a grouped set of adversarial behaviors and resources with common properties.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Intrusion set, IoC Repository, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Define an intrusion set

Define an intrusion set that is a grouped set of adversarial behaviors and resources with common properties.

## Before you begin

Role required: sn\_ti.admin

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **IoC Repository** &gt; **Intrustion Set**.

2.  Click **New**.

3.  Complete the fields in the form as appropriate.

<table id="choicetable_sq4_yvf_wmb"><thead><tr><th align="left" id="d74297e80">

Field

</th><th align="left" id="d74297e83">

Description

</th></tr></thead><tbody><tr><td id="d74297e89">

**Name**

</td><td>

Enter a descriptive name to identify the intrusion set.

</td></tr><tr><td id="d74297e98">

**First Seen**

</td><td>

The time that this intrusion set was first seen performing malicious activities.

</td></tr><tr><td id="d74297e107">

**Last Seen**

</td><td>

The time that this intrusion set was last seen performing malicious activities.

</td></tr><tr><td id="d74297e116">

**Primary Motivation**

</td><td>

The primary reason, motivation, or purpose behind this intrusion set. The motivation is why the Intrusion Set wants to achieve the goal \(what they are trying to achieve\).For example, an intrusion set with a goal to disrupt the finance sector in a country might be motivated by ideological hatred of capitalism.

</td></tr><tr><td id="d74297e129">

**Resource Level**

</td><td>

This property specifies the organizational level at which this intrusion set typically works, which in turn determines the resources available for use in an attack.

</td></tr><tr><td id="d74297e138">

**Source**

</td><td>

Specifies the threat source from which this record is created.

</td></tr><tr><td id="d74297e147">

**Description**

</td><td>

A description that provides more details and context about the intrusion set, potentially including its purpose and its key characteristics.

</td></tr><tr><td id="d74297e156">

**Aliases**

</td><td>

Alternative names to identify this intrusion set.

</td></tr><tr><td id="d74297e165">

**Goals**

</td><td>

The high-level goals of this intrusion set, namely, what are they trying to do. For example, they may be motivated by personal gain, but their goal is to steal credit card numbers. To do this, they may execute specific campaigns that have detailed objectives like compromising point of sale systems at a large retailer.

</td></tr><tr><td id="d74297e177">

**Source ID**

</td><td>

Unique identifier for this object in the threat source.

</td></tr><tr><td id="d74297e187">

**Created Time in Source**

</td><td>

Specifies the time the object is created in the source.

</td></tr><tr><td id="d74297e196">

**Modified Time in Source**

</td><td>

Specifies the time the object is modified in the source.

</td></tr></tbody>
</table>4.  Click **Submit**.


## What to do next

Click any of the following related lists to view additional information about objects associated with the intrusion set.

<table id="table_gwj_x3v_wmb"><thead><tr><th>

Related Links and Related Lists

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

Associated Attack Motivations

</td><td>

Lists any secondary motivations why this intrusion set wants to achieve.

</td></tr><tr><td>

Attack Patterns

</td><td>

Lists the attack patterns that help categorize attacks that are associated with this object.

</td></tr><tr><td>

Campaigns

</td><td>

Lists campaigns associated with this object.

</td></tr><tr><td>

Identities

</td><td>

List of identities associated with this object.

</td></tr><tr><td>

Indicators

</td><td>

Lists related Indicators of Compromise \(IoC\) that have been identified by the threat source associated with this object.

</td></tr><tr><td>

Locations

</td><td>

Lists locations that provide geographic context to this object.

</td></tr><tr><td>

Malware

</td><td>

Lists malicious code associated with this object.

</td></tr><tr><td>

Threat Actors

</td><td>

Lists individuals, groups, or organizations who act with malicious intent associated with this object.

</td></tr><tr><td>

Tools

</td><td>

Lists legitimate software that is used by threat actors to perform attacks associated with this object.

</td></tr><tr><td>

Vulnerabilities

</td><td>

Lists a weakness or defect in a software or hardware that attackers exploit which is associated with this object.

</td></tr></tbody>
</table>**Parent Topic:**[Intrusion set](../concept/threat-intelligence-intrusion-sets.md)

