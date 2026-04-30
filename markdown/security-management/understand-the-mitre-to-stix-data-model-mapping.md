---
title: Understand the MITRE to STIX data model
description: Review the terminology used by MITRE and STIX to efficiently use and understand the MITRE-ATT&amp;CK framework in the ServiceNow AI Platform.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [MITRE-ATT&amp;CK administration, MITRE-ATT&amp;CK framework overview, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Understand the MITRE to STIX data model

Review the terminology used by MITRE and STIX to efficiently use and understand the MITRE-ATT&amp;CK™ framework in the ServiceNow AI Platform.

## MITRE objects to STIX mapping

STIX is a language for describing cyber threat information in a standardized and structured manner. The parent data model in the Threat Intelligence module are the STIX objects. While the MITRE objects are a subset to the parent STIX data model. In the MITRE-ATT&amp;CK framework, MITRE provides similar STIX information with certain labels and objects.

|MITRE terminology|STIX terminology|
|-----------------|----------------|
|Technique|Attack Pattern|
|Mitigation|Course of Action|
|Groups|Intrusion Sets|
|Malware|Malware|
|Tool|Tool|

## Extending data in the Threat Intelligence module

You can maintain a list of Threat Intelligence threat sources and import the needed STIX data that includes an extensive set of cyber threat information. You can also use the TAXII profiles to facilitate automated exchange of cyber threat information.

**Note:** For more information, see [define a threat source](../concept/c_GetStartedWithThreatIntel.md#) and [create a TAXII profile](../concept/c_GetStartedWithThreatIntel.md#).

## Extending data in the MITRE-ATT&amp;CK module

You can extend the Malware, Group, Mitigation, and Tool objects to a technique in the MITRE-ATT&amp;CK repository.

You can create an object and establish a relationship between a technique and the new object in the MITRE ATT&amp;CK Repository module, but you can't define the relationship type in this module. To define a relationship type, navigate to the **Threat Intelligence** &gt; **IoC Repository** &gt; **Object-Object Relationships** module.

If you map the relationship type between an existing technique and an existing object, then you must define the technique as the target object and the object as the source object. To do so, navigate to the **IoC Repository** &gt; **Object-Object Relationships** module.

You can create a group and associate it with an attack pattern, but in the MITRE ATT&amp;CK Repository, you can only establish the relationship between the group and the attack pattern. To define the object-to-object relationship type, you must do so in the IoC Repository.

**Note:** For more information, see [extend MITRE-ATT&amp;CK data](../task/view-and-extend-information.md) and [IoC repository](../concept/ioc-repository.md).

**Parent Topic:**[MITRE-ATT&amp;CK administration](../concept/mitre-att-ck-administration.md)

**Related topics**  


[Get started with MITRE-ATT&amp;CK framework](get-started-with-mitre.md)

[Domain separation and MITRE-ATT&amp;CK](domain-separation-and-mitre-att-ck.md)

[Set up the MITRE-ATT&amp;CK framework](../task/setup-mitre-profile.md)

[Manage matrices](../task/view-mitre-collection.md)

[Manage techniques](../task/view-techniques.md)

[Manage mitigations](../task/manage-mitigations.md)

[Manage groups](../task/manage-groups-threat-intel.md)

[Manage malware](../task/manage-malware.md)

[Manage tools](../task/manage-tools.md)

[Manage MITRE relationships](../task/manage-mitre-relationships.md)

[Manage CVE and technique mapping](../task/manage-cve-and-technique-mapping.md)

[Extend the MITRE-ATT&amp;CK data](../task/view-and-extend-information.md)

[Define the data source and detection tool mapping](../task/manage-mitre-att-ck-data-sources.md)

[Define the data source and data component mapping](../task/map-the-data-source-and-data-components.md)

[Define the technique detection coverage](../task/define-technique-coverage.md)

[Map your technique detection coverage to a technique](../task/map-technique-coverage.md)

[Define the mitigation coverage](../task/define-the-mitigation-coverage.md)

[Map your mitigation coverage to a technique](../task/map-your-mitigation-coverage-to-a-technique.md)

[Create and map detection rules](../task/create-detection-rules.md)

[Auto-extract technique rules for importing MITRE-ATT&amp;CK information](../concept/auto-extract-technique-rules.md#)

[Review threat group and MITRE-ATT&amp;CK techniques mapping](../task/review-threat-group-and-techniques-mapping.md)

[Threat group to technique heatmap definition](../task/threat-group-to-technique-heatmap-definition.md)

[Review the MITRE-ATT&amp;CK system properties](../task/configure-mitre-att-ck-properties.md)

