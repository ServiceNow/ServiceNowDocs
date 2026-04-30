---
title: Define infrastructure
description: Define an Infrastructure that is any systems, software services, and any associated physical or virtual resources intended to support some purpose of an attack.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Infrastructure, IoC Repository, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Define infrastructure

Define an Infrastructure that is any systems, software services, and any associated physical or virtual resources intended to support some purpose of an attack.

## Before you begin

Role required: sn\_ti.admin

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **IoC Repository** &gt; **Infrastructure**.

2.  Click **New**.

3.  Complete the fields in the form as appropriate.

    |Field|Description|
    |-----|-----------|
    |**Name**|Enter a descriptive name to identify the infrastructure.|
    |**First Seen**|The time that this infrastructure was first seen performing malicious activities.|
    |**Last Seen**|The time that this infrastructure was last seen performing malicious activities.|
    |**Source**|Specifies the threat source from which this record is created.|
    |**Description**|A description that provides more details and context about the Infrastructure, potentially including its purpose, how it is being used, how it relates to other intelligence activities captured in related objects, and its key characteristics.|
    |**Aliases**|Alternative names to identify this infrastructure.|
    |**Source ID**|Unique identifier for this object in the threat source.|
    |**Created Time in Source**|Specifies the time the object is created in the source.|
    |**Modified Time in Source**|Specifies the time the object is modified in the source.|

4.  Click **Submit**.


## What to do next

You can now click any of the following related lists to view additional information. You can also associate other objects with the infrastructure.

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

Associated Types

</td><td>

Lists indicator types associated with this object.

</td></tr><tr><td>

Associated Kill Chain Phases

</td><td>

Lists kill chain phases associated with this object.

</td></tr><tr><td>

Associated Observables

</td><td>

Lists observables associated with this object.

</td></tr><tr><td>

Associated Infrastructure

</td><td>

Lists systems, software services, and any associated physical or virtual resources that are associated with this object.

</td></tr><tr><td>

Campaigns

</td><td>

Lists campaigns associated with this object.

</td></tr><tr><td>

Indicators

</td><td>

Lists related Indicators of Compromise \(IoC\) that have been identified by the threat source associated with this object.

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

Observed Data

</td><td>

Lists observed data associated with this object.

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
</table>**Parent Topic:**[Infrastructure](../concept/threat-intelligence-infrastructure.md)

