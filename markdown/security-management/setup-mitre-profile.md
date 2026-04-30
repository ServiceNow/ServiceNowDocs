---
title: Set up the MITRE-ATT&amp;CK framework
description: Activate the MITRE-ATT&amp;CK profile, and set up a scheduled job so that you can set up MITRE-ATT&amp;CK collections for threat detection in your organization.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [MITRE-ATT&amp;CK administration, MITRE-ATT&amp;CK framework overview, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Set up the MITRE-ATT&amp;CK framework

Activate the MITRE-ATT&amp;CK profile, and set up a scheduled job so that you can set up MITRE-ATT&amp;CK collections for threat detection in your organization.

## Before you begin

Role required: sn\_ti.admin

## About this task

Structured Threat Information Expression \(STIX™\) is a language for describing cyberthreat information in a standardized and structured manner. Using STIX data and Trusted Automated Exchange of Indicator Information \(TAXII™\) profiles, security teams can use shared cyberthreat information to isolate threats that have been previously identified by your company and from other sources.

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **Sources** &gt; **TAXII Profiles**.

    You see the available TAXII profiles.

2.  Click the **MITRE ATT&amp;CK** profile that is provided with the base system.

    ![Threat Intelligence: MITRE ATT&CK profile.](../image/mitre-attack-profile.png)

3.  To activate the TAXII collection, set the **Active** option to true for the TAXII collection that is relevant to your organization \(Enterprise ATT&amp;CK, Mobile ATT&amp;CK, or ICS ATT&amp;CK\).

<table id="table_k13_xlc_znb"><thead><tr><th>

TAXII collection

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enterprise ATT&amp;CK

</td><td>

Describes the behaviors and actions that an adversary takes to compromise and operate in an enterprise network and cloud.**Note:** The Pre ATT&amp;CK matrix has been deprecated by MITRE and is merged with the Enterprise matrix.

</td></tr><tr><td>

Mobile ATT&amp;CK

</td><td>

Describes the adversary behaviors and actions that focus on mobile devices.

</td></tr><tr><td>

ICS ATT&amp;CK

</td><td>

Describes the actions that an adversary takes while operating within an Industrial Control Systems \(ICS\) network.

</td></tr></tbody>
</table>4.  To periodically refresh the collection, set the **Run** option as appropriate for your organization.

    By default this option is set to On Demand.

    **Note:**

    1.  Collections are packaged as part of Threat Intelligence Core plugin. Installing or updating the Threat Intelligence Support Common - Version 12.0 or higher, and Threat Intelligence - Version 12.0 or higher ensures that your collections data is auto-populated.
    2.  Activate the TAXII collection only for the collection that you intend to use in your organization and disable the other collections. For example, if you intend to use Enterprise ATT&amp;CK matrix, then activate Enterprise ATT&amp;CK at the TAXII collection level and at the [Matrices](view-mitre-collection.md) level. Disable the other Mobile ATT&amp;CK and ICS ATT&amp;CK matrices at the TAXII collection and at the Matrices level.
    3.  In the TAXII Collections related lists, if you select the Run option as Daily, then an error occurs and the option defaults to On Demand. This error occurs as scheduling the MITRE-ATT&amp;CK data refresh daily is restricted to optimize the load on the MITRE servers. Also, MITRE updates the ATT&amp;CK data only twice a year.
    4.  The TAXII collections are not refreshed unless you activate the TAXII collection.
    5.  Updates to existing collections can be retrieved from the MITRE server by scheduling the ‘run’ frequency in each collection.
    6.  The customizations that you make to the MITRE-ATT&amp;CK repository data \(Malware, Group, Mitigation, and Tool objects to a technique\) are saved during scheduled updates.
    7.  MITRE updates the MITRE-ATT&amp;CK knowledge base where some objects are identified as revoked or deprecated, new objects are added, or existing objects are modified. If MITRE revokes any tactic or technique, then these objects are marked as revoked in the ServiceNow AI Platform. The revoked objects are kept in the repository but are not available for use in the ServiceNow AI Platform.

## What to do next

After the TAXII profile setup is complete, the MITRE-ATT&amp;CK repository data is imported at regular intervals to the ServiceNow AI Platform®. You can see this data by navigating to **MITRE ATT&amp;CK Repository** &gt; **Matrices** and **MITRE ATT&amp;CK Repository** &gt; **Techniques**.

**Parent Topic:**[MITRE-ATT&amp;CK administration](../concept/mitre-att-ck-administration.md)

**Related topics**  


[Get started with MITRE-ATT&amp;CK framework](../reference/get-started-with-mitre.md)

[Understand the MITRE to STIX data model](../reference/understand-the-mitre-to-stix-data-model-mapping.md)

[Domain separation and MITRE-ATT&amp;CK](../reference/domain-separation-and-mitre-att-ck.md)

[Manage matrices](view-mitre-collection.md)

[Manage techniques](view-techniques.md)

[Manage mitigations](manage-mitigations.md)

[Manage groups](manage-groups-threat-intel.md)

[Manage malware](manage-malware.md)

[Manage tools](manage-tools.md)

[Manage MITRE relationships](manage-mitre-relationships.md)

[Manage CVE and technique mapping](manage-cve-and-technique-mapping.md)

[Extend the MITRE-ATT&amp;CK data](view-and-extend-information.md)

[Define the data source and detection tool mapping](manage-mitre-att-ck-data-sources.md)

[Define the data source and data component mapping](map-the-data-source-and-data-components.md)

[Define the technique detection coverage](define-technique-coverage.md)

[Map your technique detection coverage to a technique](map-technique-coverage.md)

[Define the mitigation coverage](define-the-mitigation-coverage.md)

[Map your mitigation coverage to a technique](map-your-mitigation-coverage-to-a-technique.md)

[Create and map detection rules](create-detection-rules.md)

[Auto-extract technique rules for importing MITRE-ATT&amp;CK information](../concept/auto-extract-technique-rules.md#)

[Review threat group and MITRE-ATT&amp;CK techniques mapping](review-threat-group-and-techniques-mapping.md)

[Threat group to technique heatmap definition](threat-group-to-technique-heatmap-definition.md)

[Review the MITRE-ATT&amp;CK system properties](configure-mitre-att-ck-properties.md)

