---
title: Define a campaign
description: Define a campaign to group adversarial behaviors.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Campaigns, IoC Repository, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Define a campaign

Define a campaign to group adversarial behaviors.

## Before you begin

Role required: sn\_ti.admin

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **IoC Repository** &gt; **Campaigns**.

2.  Click **New**.

3.  Complete the fields in the form as appropriate.

<table id="choicetable_sq4_yvf_wmb"><thead><tr><th align="left" id="d351707e84">

Field

</th><th align="left" id="d351707e87">

Description

</th></tr></thead><tbody><tr><td id="d351707e93">

**Name**

</td><td>

Enter a descriptive name for this campaign.

</td></tr><tr><td id="d351707e102">

**Spec Version**

</td><td>

The version of the STIX specification used to represent this object.The value of this property must be 2.1 for STIX Objects defined according to this specification.

</td></tr><tr><td id="d351707e114">

**Source**

</td><td>

Specifies the threat source from which this record is created.

</td></tr><tr><td id="d351707e123">

**Description**

</td><td>

A description that provides more details and context about the campaign. This includes its purpose and its key characteristics.

</td></tr><tr><td id="d351707e133">

**Aliases**

</td><td>

Alternative names to identify this campaign.

</td></tr><tr><td id="d351707e142">

**Objective**

</td><td>

The campaign’s primary goal, objective, desired outcome, or intended effect. What the threat actor or intrusion set hopes to accomplish with this campaign.

</td></tr><tr><td id="d351707e151">

**Source ID**

</td><td>

Unique identifier for this object in the threat source.

</td></tr><tr><td id="d351707e160">

**Created Time in Source**

</td><td>

Specifies the time the object is created in the source.

</td></tr><tr><td id="d351707e169">

**Modified Time in Source**

</td><td>

Specifies the time the object is modified in the source.

</td></tr></tbody>
</table>4.  Click **Submit**.


## What to do next

You can now click any of the following related lists to view additional information about objects associated with the campaign.

<table id="table_zdn_szf_wmb"><thead><tr><th>

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

Attack Patterns

</td><td>

Lists the attack patterns that help categorize attacks that are associated with this object.

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
</table>**Parent Topic:**[Campaigns](../concept/threat-intelligence-campaigns.md)

