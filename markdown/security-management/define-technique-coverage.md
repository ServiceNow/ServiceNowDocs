---
title: Define the technique detection coverage
description: Define the technique detection coverage that your organization must measure and detect specific adversary techniques.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/define-technique-coverage.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [MITRE-ATT&amp;CK administration, MITRE-ATT&amp;CK framework overview, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Define the technique detection coverage

Define the technique detection coverage that your organization must measure and detect specific adversary techniques.

## Before you begin

-   Role required: sn\_ti.admin, sn\_si.admin: write access
-   Role required: sn\_ti.read: read access

## About this task

The technique coverage definitions are used in the overall technique detection mapping. You can use the base system technique coverage. The [base system technique coverage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/scoring-definition.md) consists of coverage types None, Poor, Fair, Good, Very Good, and Excellent. The base system technique coverage is also associated with pre-defined colors. You can customize the coverage type entries and colors, or create your own entries. For example, you can modify the base system coverage types to Not Applicable, Partial Coverage, and Complete Coverage. Alternatively, you can also create numerical measures for the coverage types such as 0-25 percent, 25–50 percent, and 50–100 percent. The type of modifications done to the base system coverage are not limited to the examples shared.

The customizations that you make to the coverage type and color are used in the [overall technique detection mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/map-technique-coverage.md) and also in the [heat map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/mitre-att-ck-heatmap-and-navigator.md).

**Note:** If you modify the base system coverage definition, the Coverage Type icons do not display with the techniques in the heat map. The heat map works as expected when you modify the same fields as the base system's-defined technique detection coverage and coverage colors. However, if you delete existing fields from the overall technique detection coverage, the heat map does not display the coverage type icons.

\[Omitted image "mitre-heatmap-coverage-type.png"\] Alt text: Coverage type symbols are not displayed if you modify the coverage definition.

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **MITRE ATT&amp;CK Administration** &gt; **Detection Coverage Definition**.

2.  Review the overall technique detection entries and customize the entries for your environment.

<table id="table_nb5_ldk_wnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Overall Technique Detection Coverage

</td><td>

Name of the overall technique detection coverage. The [base system technique coverage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/scoring-definition.md) consists of None, Poor, Fair, Good, Very Good, or Excellent.

</td></tr><tr><td>

Coverage Color

</td><td>

Color that is assigned to the detection coverage score. The color that you define is used for the technique detection coverage in the heat map.You can customize the colors using HEX codes and RGB\(A\) values.

</td></tr><tr><td>

Description

</td><td>

Overall technique detection coverage. See the base system definition in the [Scoring Definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/scoring-definition.md).

</td></tr></tbody>
</table>    The following illustration shows the Detection Coverage Definition list.

    \[Omitted image "mitre-detection-coverage.png"\] Alt text: Define the technique coverage.

3.  To add an entry, click **New**, complete the entries, and click **Submit**.


-   **[MITRE-ATT&amp;CK Scoring definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/scoring-definition.md)**  
Define your organization's MITRE-ATT&amp;CK scoring system so that you can measure how effectively your organization can detect specific adversary techniques.

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

[Map your technique detection coverage to a technique]()

[Define the mitigation coverage]()

[Map your mitigation coverage to a technique]()

[Create and map detection rules]()

[Auto-extract technique rules for importing MITRE-ATT&amp;CK information]()

[Review threat group and MITRE-ATT&amp;CK techniques mapping]()

[Threat group to technique heatmap definition]()

[Review the MITRE-ATT&amp;CK system properties]()

