---
title: Domain separation and MITRE-ATT&amp;CK
description: This domain separation overview pertains to MITRE-ATT&amp;CK. Domain separation allows you to separate data, processes, and administrative tasks into logical groupings called domains. You can then control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [MITRE-ATT&amp;CK administration, MITRE-ATT&amp;CK framework overview, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Domain separation and MITRE-ATT&amp;CK

This domain separation overview pertains to MITRE-ATT&amp;CK. Domain separation allows you to separate data, processes, and administrative tasks into logical groupings called domains. You can then control several aspects of this separation, including which users can see and access data.

## Support level

Support: Basic.

## How domain separation works with MITRE-ATT&amp;CK

Follow these steps to achieve domain separation:

-   Create a user with the required sn\_ti.admin roles in the respective domain.
-   Replicate the following for every domain:
    -   [TAXII Collections](domain-separation-and-mitre-att-ck.md#section_svm_dry_y4b)

        **Note:**

        -   Do not activate the collections in the global domain. Activate only the collections that are replicated and available in your domain.
        -   Change the **Run as** field in the collections to the user with the sn\_ti.admin role in the respective domain.
    -   Technique Coverage Definition
    -   Technique Extraction Rule
    -   Detection Rules – MITRE ATT&amp;CK Mappings
    -   Mitigation Coverage
        -   Copy all the mitigation coverage definition records.
        -   Copy the mitigate coverage calculator or create a new calculator for the respective domain.
    -   Threat Group - Technique Heatmap Definitions

## Replicate TAXII Collection

1.  Navigate to **Threat Intelligence** &gt; **Sources** &gt; **TAXII Profiles**.
2.  In the header bar, use the domain picker to select your domain.
3.  Select the TAXII collection that is relevant to your organization \(Enterprise ATT&amp;CK, Mobile ATT&amp;CK, or ICS ATT&amp;CK\).
4.  Right-click in the header bar and select **Insert and Stay**. The duplicate TAXII collection is created under the selected domain
5.  Navigate back to the MITRE ATT&amp;CK TAXII Profile to view the duplicate TAXII collection.

The following illustration shows how to select the domain TOP/Initech, replicate the TAXII collection in the domain, and verify the replicated TAXII collection.

![Replicate the TAXII collection using the Insert and Stay option.](../image/mitre-insert-stay.gif)

**Parent Topic:**[MITRE-ATT&amp;CK administration](../concept/mitre-att-ck-administration.md)

**Related topics**  


[Get started with MITRE-ATT&amp;CK framework](get-started-with-mitre.md)

[Understand the MITRE to STIX data model](understand-the-mitre-to-stix-data-model-mapping.md)

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

