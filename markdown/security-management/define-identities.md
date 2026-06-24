---
title: Define identities
description: Define identities who represent actual individuals, organizations, or groups.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/define-identities.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Identities, IoC Repository, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Define identities

Define identities who represent actual individuals, organizations, or groups.

## Before you begin

Role required: sn\_ti.admin

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **IoC Repository** &gt; **Identities**.

2.  Click **New**.

3.  Complete the fields in the form as appropriate.

<table id="choicetable_sq4_yvf_wmb"><thead><tr><th align="left" id="d254211e80">

Field

</th><th align="left" id="d254211e83">

Description

</th></tr></thead><tbody><tr><td id="d254211e89">

**Name**

</td><td>

Enter a descriptive name for this identity.When referring to a specific entity \(an individual or organization\), this property must contain the canonical name of the specific entity.

</td></tr><tr><td id="d254211e101">

**Identity Class**

</td><td>

The type of entity that this identity describes. For example, individual or organization.

</td></tr><tr><td id="d254211e113">

**Source**

</td><td>

Specifies the threat source from which this record is created.

</td></tr><tr><td id="d254211e122">

**Description**

</td><td>

A description that provides more details and context about the identity, potentially including its purpose and its key characteristics.

</td></tr><tr><td id="d254211e132">

**Source ID**

</td><td>

Unique identifier for this object in the threat source.

</td></tr><tr><td id="d254211e141">

**Created Time in Source**

</td><td>

Specifies the time the object is created in the source.

</td></tr><tr><td id="d254211e150">

**Modified Time in Source**

</td><td>

Specifies the time the object is modified in the source.

</td></tr></tbody>
</table>4.  Click **Submit**.


## What to do next

Click any of the following related lists to view additional information about objects associated the identity.

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

Campaigns

</td><td>

Lists campaigns associated with this object.

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

</td></tr></tbody>
</table>**Parent Topic:**[Identities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/threat-intelligence-identities.md)

