---
title: Map your mitigation coverage to a technique
description: Map your mitigation coverage with the technique that enables you to detect your organization's overall mitigation strategy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/map-your-mitigation-coverage-to-a-technique.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [MITRE-ATT&amp;CK administration, MITRE-ATT&amp;CK framework overview, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Map your mitigation coverage to a technique

Map your mitigation coverage with the technique that enables you to detect your organization's overall mitigation strategy.

## Before you begin

-   Role required: sn\_ti.admin, sn\_si.admin: write, delete access
-   Role required: sn\_ti.read: read access

## About this task

Mitigations enable you to prevent an adversary from successfully executing techniques or sub-techniques against your organization. Each MITRE-ATT&amp;CK technique contains mitigations that you can deploy in your organization to reduce the chance of being attacked. You can use the mitigation coverage to get an overview of your organization's overall mitigation strategy. For example, if an adversary is attacking your organization, you see the kind of coverage that you have to mitigate the attacker's techniques.

The technique, and mitigation information are automatically populated for all the collections and techniques that you have activated. The [mitigation coverage definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/define-the-mitigation-coverage.md) that you have defined are available for you to select in the technique mitigation coverage.

You can identify mitigations that are relevant to your organization. If a mitigation is relevant, then you can define if the mitigation strategies have been deployed. You can specify if the strategies are applied as part of your organization's SOC Policy. You can also identify if your organization has preventive tools in place to mitigate an attacker's techniques and you can map any security controls that your organization has deployed to minimize security risks. Populate the mitigation coverage \(percentage\) for each of the records.

After mapping the information for each of the techniques, the [mitigation coverage calculator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/mitigation-coverage-calculator.md) auto populates the Calculated Technique Mitigation Coverage. To calculate the overall mitigation coverage for any technique, the technique mitigation mapping records must be active and relevant to the organization. The records which are inactive and not relevant are not considered for calculating the overall technique mitigation coverage. Based on the values in the Calculated Technique Mitigation Coverage and the [mitigation coverage definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/define-the-mitigation-coverage.md), your Overall Technique Mitigation Coverage \(Calculated\) is populated.

The customizations that you make to the coverage types, colors, or percentages are used in the mitigation coverage mapping and also in the [heat map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/mitre-att-ck-heatmap-and-navigator.md).

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **MITRE ATT&amp;CK Administration** &gt; **Mitigation Coverage Mapping**.

2.  Review each technique to mitigation mapping and update the **Mitigation Coverage \(Percentage\)** to calculate your organization's coverage availability.

    |Field|Description|
    |-----|-----------|
    |ID|Technique’s unique identity. The IDs are automatically populated for all the collections and techniques that you have activated.|
    |Technique|How an adversary achieves a tactical objective by performing an action. The technique information is automatically populated for all the collections and techniques that you have activated.|
    |Mitigation|Mitigations that enable you to prevent an adversary from successfully executing techniques or sub-techniques against your organization. The mitigation information is automatically populated for all the collections and techniques that you have activated.|
    |Relevant|Option to specify if the mitigation is relevant to your organization.|
    |Active|Option to specify if the mitigation strategies are deployed in your organization. This is a required option required to calculate the technique mitigation coverage.|
    |Preventive Tools|Option to specify if your organization has preventive tools in place to mitigate an attacker's techniques.|
    |SOC Policy|The SOC policies that define the mitigation strategies in your organization.|
    |Security Controls|Your organization's security controls contain the mitigation strategies to minimize security risks.|
    |Mitigation Coverage \(Percentage\)|A scoring system to calculate the technique mitigation coverage. Define numerical values between 0 through 100. This is a required option required to calculate the technique mitigation coverage.|
    |Calculated Technique Mitigation Coverage \(Percentage\)|The calculated technique mitigation coverage in percentage. This value is determined based on the formula defined in the [mitigation coverage calculator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/mitigation-coverage-calculator.md).|
    |Overall Technique Mitigation Coverage \(Calculated\)|The overall technique mitigation coverage. This value is determined based on the [mitigation coverage that is defined for your organization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/define-the-mitigation-coverage.md).|
    |Comment|Description about the technique and mitigation coverage mapping.|
    |Revoked|The technique to mitigation coverage mapping is revoked.|

    In this illustration, you see that the technique Valid Accounts has five mitigations associated, each with a mitigation coverage of 16 for user training, 92 for application developer guidance, and 16 for password policies, 91 for privileged account management, and 14 for valid accounts mitigation. The calculated technique mitigation coverage is 45.8 percent. \[Omitted image "mitre-mitigation-coverage-mapping.png"\] Alt text: The illustration shows the mitigation coverage mapping for each of the techniques.


-   **[Overall technique mitigation coverage calculator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/mitigation-coverage-calculator.md)**  
The overall technique mitigation coverage is determined based on the formula defined in the mitigation coverage calculator.

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

[Create and map detection rules]()

[Auto-extract technique rules for importing MITRE-ATT&amp;CK information]()

[Review threat group and MITRE-ATT&amp;CK techniques mapping]()

[Threat group to technique heatmap definition]()

[Review the MITRE-ATT&amp;CK system properties]()

