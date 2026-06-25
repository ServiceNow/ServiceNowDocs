---
title: Auto-extract technique rules for importing MITRE-ATT&amp;CK information
description: Use the base system auto-extraction rules to import the MITRE-ATT&amp;CK information from any existing third-party integrations.Use the threat lookup auto-extraction rules to import the MITRE-ATT&amp;CK information from any existing Threat Intelligence third-party integrations.Use the SIEM auto-extraction rules to import the MITRE-ATT&amp;CK information from any existing Security Operations SIEM third-party integrations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/auto-extract-technique-rules.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [MITRE-ATT&amp;CK administration, MITRE-ATT&amp;CK framework overview, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Auto-extract technique rules for importing MITRE-ATT&amp;CK information

Use the base system auto-extraction rules to import the MITRE-ATT&amp;CK information from any existing third-party integrations.

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

[Extend the MITRE-ATT&amp;CK data]()

[Define the data source and detection tool mapping]()

[Define the data source and data component mapping]()

[Define the technique detection coverage]()

[Map your technique detection coverage to a technique]()

[Define the mitigation coverage]()

[Map your mitigation coverage to a technique]()

[Create and map detection rules]()

[Review threat group and MITRE-ATT&amp;CK techniques mapping]()

[Threat group to technique heatmap definition]()

[Review the MITRE-ATT&amp;CK system properties]()

## Use threat-lookup auto-extraction rules

Use the threat lookup auto-extraction rules to import the MITRE-ATT&amp;CK information from any existing Threat Intelligence third-party integrations.

### Before you begin

Role required:

-   sn\_ti.admin, sn\_si.admin: create, write, delete access
-   sn\_ti.read: read access

### About this task

When any Threat Intelligence integration, such as Sandbox or a TIP, supports the MITRE-ATT&amp;CK framework and if the MITRE-ATT&amp;CK information is parsed at each integration level, then the information is displayed in each threat lookup result record. However, not all Threat Intelligence integrations parse the MITRE-ATT&amp;CK information. The threat lookup global auto-extraction rule can extract MITRE-ATT&amp;CK information from all Threat Intelligence integrations.

You can choose to roll up the MITRE-ATT&amp;CK information automatically from the threat lookup results to a security incident. For automatic rollup of threat lookup results to security incidents, [enable the system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/configure-mitre-att-ck-properties.md). Alternatively, you can [rollup the information manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/associate-mitre-observables.md) for each individual threat lookup.

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

Source engine.

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

    \[Omitted image "mitre-splunk-extraction.gif"\] Alt text: Splunk technique extraction rule.

4.  Click **Submit**.


