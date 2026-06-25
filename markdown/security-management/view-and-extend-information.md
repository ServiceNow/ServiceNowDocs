---
title: Extend the MITRE-ATT&amp;CK data
description: Extend the MITRE-ATT&amp;CK repository data in the ServiceNow AI Platform by enriching it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/view-and-extend-information.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [MITRE-ATT&amp;CK administration, MITRE-ATT&amp;CK framework overview, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Extend the MITRE-ATT&amp;CK data

Extend the MITRE-ATT&amp;CK repository data in the ServiceNow AI Platform by enriching it.

## Before you begin

Role required:

-   sn\_ti.admin: delete access
-   sn\_ti.read: read access
-   sn\_ti.write: create, write access

## About this task

You can extend the Malware, Group, Mitigation, and Tool objects to a technique in the MITRE-ATT&amp;CK repository.

You can create a new object and establish a relationship between a technique and the new object in the MITRE ATT&amp;CK Repository module, but you can't define the relationship type in this module. For more information about defining relationship types, see [object to object relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/define-object-object.md). To define a relationship type, navigate to the **Threat Intelligence** &gt; **IoC Repository** &gt; **Object-Object Relationships** module.

If you map the relationship type between an existing technique and an existing object, then you must define the technique as the target object and the object as the source object. To do so, navigate to the **IoC Repository** &gt; **Object-Object Relationships** module.

You can create a group and associate it with an attack pattern, but in the MITRE ATT&amp;CK Repository, you can only establish the relationship between the group and the attack pattern. To define the object-to-object relationship type, you must do so in the IoC Repository.

**Note:** Any customizations that you make to the objects are saved during scheduled updates.

## Procedure

1.  Navigate to **Threat Intelligence** &gt; **MITRE ATT&amp;CK Repository** &gt; **Techniques**.

2.  Click a techniques or sub-technique to view all the associated information with this technique.

    In the following illustration, you can see that the Botnet \(T1584.005\) technique is not associated with any group. If you have additional information about a technique or sub-technique, you can enrich it by adding or modifying the information.\[Omitted image "mitre-botnet.png"\] Alt text: Associate a Botnet with another object.

3.  Click a related list to enrich its data to associate it with a new group.

    In the following illustration, a group, Custom1, has been associated with the Botnet sub-technique.

    \[Omitted image "mitre-extend-object.gif"\] Alt text: Extend MITRE object information by enriching its data.


**Parent Topic:**[MITRE-ATT&amp;CK administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/mitre-att-ck-administration.md)

**Related topics**  


[Get started with MITRE-ATT&amp;CK framework]()

[Understand the MITRE to STIX data model]()

[Domain separation and MITRE-ATT&amp;CK]()

[Set up the MITRE-ATT&amp;CK framework]()

[Manage matrices]()

[Manage techniques]()

[Manage mitigations]()

[Manage groups]()

[Manage malware]()

[Manage tools]()

[Manage MITRE relationships]()

[Manage CVE and technique mapping]()

[Define the data source and detection tool mapping]()

[Define the data source and data component mapping]()

[Define the technique detection coverage]()

[Map your technique detection coverage to a technique]()

[Define the mitigation coverage]()

[Map your mitigation coverage to a technique]()

[Create and map detection rules]()

[Auto-extract technique rules for importing MITRE-ATT&amp;CK information]()

[Review threat group and MITRE-ATT&amp;CK techniques mapping]()

[Threat group to technique heatmap definition]()

[Review the MITRE-ATT&amp;CK system properties]()

