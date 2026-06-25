---
title: Define the mitigation coverage
description: Define the mitigation coverage for each mitigation that is associated with a technique so that you gain visibility into how well your organization can prevent the attacks that happen due to a particular technique.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/define-the-mitigation-coverage.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [MITRE-ATT&amp;CK administration, MITRE-ATT&amp;CK framework overview, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Define the mitigation coverage

Define the mitigation coverage for each mitigation that is associated with a technique so that you gain visibility into how well your organization can prevent the attacks that happen due to a particular technique.

## Before you begin

-   Role required: sn\_ti.admin, sn\_si.admin: create, write, delete access
-   Role required: sn\_ti.read: read access

## About this task

The mitigation coverage definitions are used in the overall mitigation and technique coverage mapping. You can use the base system mitigation coverage. The base system mitigation coverage consists of coverage types None, Poor, Fair, Good, Very Good, and Excellent. The base system mitigation coverage is also associated with pre-defined colors, and coverage percentages. You can customize the coverage types \(add or remove coverage types\), coverage percentages for lower limits and higher limits, and colors, or create your custom mitigation coverage.

The customizations that you make to the coverage types, colors, or percentages are used in the mitigation coverage mapping and also in the [heat map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/mitre-att-ck-heatmap-and-navigator.md).

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **MITRE ATT&amp;CK Administration** &gt; **Mitigation Coverage Definition**.

2.  Review the mitigation detection entries and customize the entries for your environment.

<table id="table_nb5_ldk_wnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Overall Technique Mitigation Coverage

</td><td>

Name of the technique mitigation coverage. The [base system mitigation coverage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/technique-mitigation-coverage-definitions.md) consists of None, Poor, Fair, Good, Very Good, or Excellent.

</td></tr><tr><td>

Coverage Percentage Lower Limit

</td><td>

The lower percentage limit of the mitigation coverage. Define the numerical values between 0 through 100.

</td></tr><tr><td>

Coverage Percentage Higher Limit

</td><td>

The higher percentage limit of the mitigation coverage. Define the numerical values between 0 through 100.

</td></tr><tr><td>

Coverage Color

</td><td>

Color that is assigned to the detection coverage score. The color that you define is used for the technique mitigation coverage in the heat map.You can customize the colors using HEX codes and RGB\(A\) values.

</td></tr><tr><td>

Description

</td><td>

Overall mitigation detection coverage. See the base system definition in the [technique mitigation coverage definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/technique-mitigation-coverage-definitions.md).

</td></tr></tbody>
</table>    **Note:** Ensure that you do not overlap the coverage percentage ranges if you customize the percentage limits \(lower or higher\). For example, if a coverage record has the ranges 0 to 20, then the next consecutive record must have lower limit range of 21 or higher to avoid overlapping the coverage percentage range.

    The following illustration shows the mitigation coverage definition list.

    \[Omitted image "mitre-mitigation-definitions.png"\] Alt text: The illustration shows the technique mitigation coverage definition list.

3.  To add an entry, click **New**, complete the entries, and click **Submit**.


-   **[Technique mitigation coverage definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/technique-mitigation-coverage-definitions.md)**  
Define your organization's mitigation coverage so that you can effectively measure and detect specific adversary techniques.

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

[Map your mitigation coverage to a technique]()

[Create and map detection rules]()

[Auto-extract technique rules for importing MITRE-ATT&amp;CK information]()

[Review threat group and MITRE-ATT&amp;CK techniques mapping]()

[Threat group to technique heatmap definition]()

[Review the MITRE-ATT&amp;CK system properties]()

