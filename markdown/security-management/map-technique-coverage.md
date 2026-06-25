---
title: Map your technique detection coverage to a technique
description: Map your overall technique detection coverage with the technique that enables your organization to detect specific adversary techniques.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/map-technique-coverage.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [MITRE-ATT&amp;CK administration, MITRE-ATT&amp;CK framework overview, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Map your technique detection coverage to a technique

Map your overall technique detection coverage with the technique that enables your organization to detect specific adversary techniques.

## Before you begin

-   Role required: sn\_ti.admin, sn\_si.admin: write access
-   Role required: sn\_ti.read: read access

## About this task

You can use the technique detection coverage to get an overview into your organization's overall technique detection coverage. For example, if an adversary is attacking your organization, you see the kind of coverage that you have to detect the attacker's techniques.

The technique and ID are automatically populated for all the [collections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/setup-mitre-profile.md) and [techniques](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/view-techniques.md) that you have activated. The [coverage type and scoring definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/define-technique-coverage.md) that you have defined are available for as an option that you can select in the overall technique detection coverage.

You can map the overall technique detection coverage with the technique to complete the mapping. You can associate a technique with only one overall technique detection coverage.

The technique detection coverage mapping that you define is used in the [coverage visualization in the heatmap](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/mitre-att-ck-heatmap-and-navigator.md).

**Note:** You can arrive at the overall technique detection coverage using your organization-specific calculations. You may use any Breach &amp; Attack Simulation \(BAS\) products, the Cyber Analytics Repository \(CAR\), or any other methods as necessary to define the scoring definition, and use it in this procedure for the overall technique detection coverage mapping.

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **MITRE ATT&amp;CK Administration** &gt; **Detection Coverage Mapping**.

    In this illustration, you see that the Cloud Accounts \(T1078.004\) sub-technique has excellent coverage in the organization and that the Overall Technique Detection Coverage is mapped to **Excellent**.

    \[Omitted image "mitre-coverage-mapping.gif"\] Alt text: Detection coverage mapping.

2.  Review each technique and map your overall technique detection coverage based on your [detection coverage definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/define-technique-coverage.md) and your organization's coverage availability.


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

[Define the mitigation coverage]()

[Map your mitigation coverage to a technique]()

[Create and map detection rules]()

[Auto-extract technique rules for importing MITRE-ATT&amp;CK information]()

[Review threat group and MITRE-ATT&amp;CK techniques mapping]()

[Threat group to technique heatmap definition]()

[Review the MITRE-ATT&amp;CK system properties]()

