---
title: Auto-extract technique rules for importing MITRE-ATT&amp;CK information
description: Use the base system auto-extraction rules to import the MITRE-ATT&amp;CK information from any existing third-party integrations.Use the threat lookup auto-extraction rules to import the MITRE-ATT&amp;CK information from any existing Threat Intelligence third-party integrations.Use the SIEM auto-extraction rules to import the MITRE-ATT&amp;CK information from any existing Security Operations SIEM third-party integrations.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [MITRE-ATT&amp;CK administration, MITRE-ATT&amp;CK framework overview, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Auto-extract technique rules for importing MITRE-ATT&amp;CK information

Use the base system auto-extraction rules to import the MITRE-ATT&amp;CK information from any existing third-party integrations.

**Parent Topic:**[MITRE-ATT&amp;CK administration](mitre-att-ck-administration.md)

**Related topics**  


[Get started with MITRE-ATT&amp;CK framework](../reference/get-started-with-mitre.md)

[Understand the MITRE to STIX data model](../reference/understand-the-mitre-to-stix-data-model-mapping.md)

[Domain separation and MITRE-ATT&amp;CK](../reference/domain-separation-and-mitre-att-ck.md)

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

[Review threat group and MITRE-ATT&amp;CK techniques mapping](../task/review-threat-group-and-techniques-mapping.md)

[Threat group to technique heatmap definition](../task/threat-group-to-technique-heatmap-definition.md)

[Review the MITRE-ATT&amp;CK system properties](../task/configure-mitre-att-ck-properties.md)

## Use threat-lookup auto-extraction rules

Use the threat lookup auto-extraction rules to import the MITRE-ATT&amp;CK information from any existing Threat Intelligence third-party integrations.

### Before you begin

Role required:

-   sn\_ti.admin, sn\_si.admin: create, write, delete access
-   sn\_ti.read: read access

### About this task

When any Threat Intelligence integration, such as Sandbox or a TIP, supports the MITRE-ATT&amp;CK framework and if the MITRE-ATT&amp;CK information is parsed at each integration level, then the information is displayed in each threat lookup result record. However, not all Threat Intelligence integrations parse the MITRE-ATT&amp;CK information. The threat lookup global auto-extraction rule can extract MITRE-ATT&amp;CK information from all Threat Intelligence integrations.

You can choose to roll up the MITRE-ATT&amp;CK information automatically from the threat lookup results to a security incident. For automatic rollup of threat lookup results to security incidents, [enable the system property](../task/configure-mitre-att-ck-properties.md). Alternatively, you can [rollup the information manually](../task/associate-mitre-observables.md) for each individual threat lookup.

The base system Threat Intelligence automatically extracts the MITRE-ATT&amp;CK information from the third-party integrations raw payload to the threat lookup result record, if the Threat Intelligence integration provides you with MITRE-ATT&amp;CK information like the technique or tactic.

If the MITRE-ATT&amp;CK information is not available in the raw payload field of the threat lookup record, then you must define your own rule for auto-extraction from the third-party integration.

### Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **MITRE ATT&amp;CK Administration** &gt; **Technique Extraction Rule**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_o41_d3t_wnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Auto-extraction rule name.

</td></tr><tr><td>

Rule Type

</td><td>

Auto-extraction rule type. Select **Threat Lookup**.

</td></tr><tr><td>

Ignore Auto-Extraction

</td><td>

Setting that by default, is cleared. This setting enables automatic extraction of MITRE-ATT&amp;CK techniques.

</td></tr><tr><td>

Source Engine

</td><td>

If a value is specified in this field, then the rule will be applied exclusively to the threat lookup results that include the specified source engine in the source engine field.

</td></tr><tr><td>

Global

</td><td>

Source engine setting. When you set the source engine to **Global**, the extraction runs on all threat lookup integration results.

</td></tr><tr><td>

Description

</td><td>

Description of the auto-extraction rule.

</td></tr><tr><td>

Process Method

</td><td>

Regex or a script method that you specify to link the technique information from the raw payload.

</td></tr><tr><td>

Regex Extraction

</td><td>

Option that you specify for the **Target Field** when using the regex extraction method. Regex is the default.

</td></tr><tr><td>

Script Extraction

</td><td>

Process that you select when running a script. The script reviews the following:-   threatLookupResultSysId:sys\_id of the threat lookup result record
-   sourceName: Name of the threat lookup source.


</td></tr><tr><td>

Tactic Extraction

</td><td>

Option that you specify to extract tactic related information from the raw payload. If a payload contains specific tactic and technique related information, you can extract and append the information to the security incident.

</td></tr></tbody>
</table>4.  Click **Submit**.


## Use SIEM auto-extraction rules

Use the SIEM auto-extraction rules to import the MITRE-ATT&amp;CK information from any existing Security Operations SIEM third-party integrations.

### Before you begin

Role required:

-   sn\_ti.admin, sn\_si.admin: create, write, delete access
-   sn\_ti.read: read access

### About this task

The technique extraction rule is available for all base system Security Operations SIEM integrations such as Splunk, IBM QRadar, and ArcSight integrations. When the ServiceNow AI Platform ingests alert or event data from these SIEM integrations and they contain MITRE-ATT&amp;CK information, the ServiceNow AI Platform processes the raw payload and auto-extracts the MITRE-ATT&amp;CK information.

If your ServiceNow AI Platform contains base system SIEM integrations, that means that the technique extraction rules are already created in the MITRE-ATT&amp;CK module. You should review and modify the rules as needed.

Enable either the SIEM auto-extraction rule or the alert rule at a time.

### Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **MITRE ATT&amp;CK Administration** &gt; **Technique Extraction Rule**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Auto-extraction rule name.|
    |Rule Type|Auto-extraction rule type. Select **SIEM**.|
    |Ignore Auto-Extraction|Setting that by default is cleared. This setting enables automatic extraction of MITRE-ATT&amp;CK techniques.|
    |Import Table|Import table that is automatically mapped for base system SIEM integrations. Review this field for other SIEM integrations for the MITRE-ATT&amp;CK information and map accordingly.|
    |Import Field|Import field that is automatically mapped for base system SIEM integrations. Review this field for other SIEM integrations for the MITRE-ATT&amp;CK information and map accordingly.|
    |Description|Auto-extraction rule.|
    |Process Method|Regex or a script method that you specify to link the technique information from the raw payload.|
    |Regex Extraction|Option that you specify for the **Target Field** when using the regex method. Regex extraction is the default process method.|
    |Script Extraction|Script process method that you use if you want to customize how the MITRE-ATT&amp;CK information is extracted.|
    |Tactic Extraction|Option that you specify to extract tactic related information from the raw payload. If a payload contains specific tactic and technique related information, you can extract and append the information to the security incident.|

    In the following illustration, you see an example of the Splunk Enterprise SIEM technique extraction rule in the form view. This rule is similar to all the other SIEM technique extraction rules.

    ![Splunk technique extraction rule.](../image/mitre-splunk-extraction.gif)

4.  Click **Submit**.


