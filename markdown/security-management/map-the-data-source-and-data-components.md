---
title: Define the data source and data component mapping
description: Use the Data Component Mapping if you are using the latest TAXII collections, and you want to maintain a relationship between the data sources, data components, and the various techniques. Map the data sources with the additional context of data components that provides an extra sublayer of context to data sources that enable you to understand adversary behaviors in MITRE-ATT&amp;CK better.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [MITRE-ATT&amp;CK administration, MITRE-ATT&amp;CK framework overview, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Define the data source and data component mapping

Use the Data Component Mapping if you are using the latest TAXII collections, and you want to maintain a relationship between the data sources, data components, and the various techniques. Map the data sources with the additional context of data components that provides an extra sublayer of context to data sources that enable you to understand adversary behaviors in MITRE-ATT&amp;CK better.

## Before you begin

Role required:

-   sn\_ti.admin, sn\_si.admin: write, delete access
-   sn\_ti.read: read access

## About this task

Mapping the data sources and data components provides visibility into the data sources or components and the techniques that are relevant for your organization.

For example, if your organization focuses on 7 techniques, you may need 5 data sources and 10 data components to monitor these sources. Your evaluation of internal tools reveals that your organization doesn’t have two data sources and four data components. This mapping exercise provides visibility into the data sources, components, &amp; techniques, their relevance to your organization, and to identify the gaps in coverage. You can thus focus your investment on the right data sources and alert sensors to detect and mitigate adversary threats.

The MITRE-ATT&amp;CK framework contains an updated structure for the data sources - Data Source: Data Component. This new form of data source provides an extra context to the data sources. The data source object features the name of the data source as well as key details about the collected data \(file, process, network traffic, and so on\) and specific values or properties required to detect adversary behaviors.

The following illustration shows the MITRE-ATT&amp;CK STIX™ structure representation for data sources and data components. You can see both the data sources and data components captured as custom STIX™ objects. The illustration shows that each data source contains one or more data components, and each data component detects one or more techniques.

![This image shows the general structure of data sources and data components.](../image/mitre-datasourcecomponent.png "General structure of data sources and data components")

You can continue using the [Data Source Mapping](manage-mitre-att-ck-data-sources.md) if your MITRE-ATT&amp;CK repository contains the old TAXII collections, and you’ve mapped your data sources to various techniques. However, use the [Data Component Mapping](map-the-data-source-and-data-components.md) if you’re using the latest TAXII collections, and you want to maintain a relationship between the data sources, data components, and the various techniques.

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **MITRE ATT&amp;CK Administration** &gt; **Data Component Mapping**.

    The following illustration shows the list of tactics, IDs, techniques along with the data sources and data components based on your collection updates.![The following illustration shows the list of tactics, techniques, IDs, along with the data sources and data components that have been populated based on your collection updates.](../image/mitre-data-component-overview.png)

    |Field|Description|
    |-----|-----------|
    |Tactic|Adversary’s objective or the reason for performing an action.|
    |ID|Technique’s unique identity.|
    |Technique|How an adversary achieves a tactical objective by performing an action.|
    |Data Source|Data source that is associated with the technique.|
    |Data Component|Data component that is associated with the data source. A data component can only have one parent data source.|
    |Data Component Revoked|Identifies if the data component has been revoked in the MITRE-ATT&amp;CK knowledge base.|
    |Detection Tool|Tool that supplements the data source by detecting the techniques that are used. The detection tool is mapped with the alert sensor in SIR.|
    |Comment|Description about the data source and data component mapping.|
    |Revoked|Identifies if the data component to technique mapping is revoked by MITRE-ATT&amp;CK.|

2.  Review the listed data sources and data components and modify the values based on your environment.

3.  Follow these steps to add a data component.

    1.  Navigate to **Threat Intelligence** &gt; **MITRE ATT&amp;CK Administration** &gt; **Techniques**.

    2.  Click a technique that you want to modify the data source: data component information.

    3.  Unlock Data Source: Data Component.

    4.  Use the lookup list to select MITRE-ATT&amp;CK data components.

    5.  Lock Data Source: Data Component.

    6.  Click **Update**.

    In the following illustration, you see how to add data components.![This illustration shows how to map data source components to a technique.](../image/mitre-data-source-component-mapping.gif)


**Parent Topic:**[MITRE-ATT&amp;CK administration](../concept/mitre-att-ck-administration.md)

**Related topics**  


[Get started with MITRE-ATT&amp;CK framework](../reference/get-started-with-mitre.md)

[Understand the MITRE to STIX data model](../reference/understand-the-mitre-to-stix-data-model-mapping.md)

[Domain separation and MITRE-ATT&amp;CK](../reference/domain-separation-and-mitre-att-ck.md)

[Set up the MITRE-ATT&amp;CK framework](setup-mitre-profile.md)

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

[Define the technique detection coverage](define-technique-coverage.md)

[Map your technique detection coverage to a technique](map-technique-coverage.md)

[Define the mitigation coverage](define-the-mitigation-coverage.md)

[Map your mitigation coverage to a technique](map-your-mitigation-coverage-to-a-technique.md)

[Create and map detection rules](create-detection-rules.md)

[Auto-extract technique rules for importing MITRE-ATT&amp;CK information](../concept/auto-extract-technique-rules.md#)

[Review threat group and MITRE-ATT&amp;CK techniques mapping](review-threat-group-and-techniques-mapping.md)

[Threat group to technique heatmap definition](threat-group-to-technique-heatmap-definition.md)

[Review the MITRE-ATT&amp;CK system properties](configure-mitre-att-ck-properties.md)

