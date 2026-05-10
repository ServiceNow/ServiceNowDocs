---
title: Define threat actors
description: Define threat actors who are individuals, groups, or organizations who act with malicious intent.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Threat actors, IoC Repository, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Define threat actors

Define threat actors who are individuals, groups, or organizations who act with malicious intent.

## Before you begin

Role required: sn\_ti.admin

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **IoC Repository** &gt; **Threat Actors**.

2.  Click **New**.

3.  Complete the fields in the form as appropriate.

<table id="choicetable_sq4_yvf_wmb"><thead><tr><th align="left" id="d462569e84">

Field

</th><th align="left" id="d462569e87">

Description

</th></tr></thead><tbody><tr><td id="d462569e93">

**Name**

</td><td>

Enter a name to identify the malware instance or family, as specified by the producer of the SDO. For a malware family, the name must be defined.

</td></tr><tr><td id="d462569e102">

**First Seen**

</td><td>

The time that this malware instance or family was first seen performing malicious activities.

</td></tr><tr><td id="d462569e111">

**Last Seen**

</td><td>

The time that this malware instance or family was last seen performing malicious activities.

</td></tr><tr><td id="d462569e120">

**Primary Motivation**

</td><td>

The primary reason, motivation, or purpose behind this threat actor. The motivation is why the threat actor wants to achieve the goal \(what they are trying to achieve\). For example, a threat actor with a goal to disrupt the finance sector in a country might be motivated by ideological hatred of capitalism.

</td></tr><tr><td id="d462569e133">

**Resource Level**

</td><td>

The organizational level at which this threat actor typically works, which in turn determines the resources available to this Threat Actor for use in an attack.

</td></tr><tr><td id="d462569e142">

**Source**

</td><td>

Specifies the threat source from which this record is created.

</td></tr><tr><td id="d462569e151">

**Description**

</td><td>

A description that provides more details and context about the threat actor, potentially including its purpose and its key characteristics.

</td></tr><tr><td id="d462569e160">

**Aliases**

</td><td>

A list of other names to identify this threat actor.

</td></tr><tr><td id="d462569e169">

**Goals**

</td><td>

The high-level goals of this threat actor, namely, what are they trying to do. For example, they may be motivated by personal gain, but their goal is to steal credit card numbers.

</td></tr><tr><td id="d462569e178">

**Source ID**

</td><td>

Unique identifier for this object in the threat source.

</td></tr><tr><td id="d462569e188">

**Created Time in Source**

</td><td>

Specifies the time the object is created in the source.

</td></tr><tr><td id="d462569e197">

**Modified Time in Source**

</td><td>

Specifies the time the object is modified in the source.

</td></tr></tbody>
</table>4.  Click **Submit**.


## What to do next

Click any of the following related lists to view additional information about objects associated with the threat actor.

<table id="table_bfx_vlz_wmb"><thead><tr><th>

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

Associated Types

</td><td>

Lists indicator types associated with this object.

</td></tr><tr><td>

Associated Roles

</td><td>

Lists the associated roles with the threat actor.

</td></tr><tr><td>

Associated Attack Motivations

</td><td>

Lists the associated attack motivations with the threat actor.

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

Infrastructure

</td><td>

Lists systems, software services, and any associated physical or virtual resources that are associated with this object.

</td></tr><tr><td>

Intrusion Set

</td><td>

Lists a set of adversarial behaviors and resources with common properties associated with this object.

</td></tr><tr><td>

Locations

</td><td>

Lists locations that provide geographic context to this object.

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
</table>**Parent Topic:**[Threat actors](../concept/threat-actors.md)

