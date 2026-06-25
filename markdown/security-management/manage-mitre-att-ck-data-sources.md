---
title: Define the data source and detection tool mapping
description: Define the data source and detection tool mapping for MITRE-ATT&amp;CK tactics and techniques. The data source mapping provides you with insight into the relevance and availability of the data sources and the detection tools for monitoring the data sources in your environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/manage-mitre-att-ck-data-sources.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [MITRE-ATT&amp;CK administration, MITRE-ATT&amp;CK framework overview, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Define the data source and detection tool mapping

Define the data source and detection tool mapping for MITRE-ATT&amp;CK tactics and techniques. The data source mapping provides you with insight into the relevance and availability of the data sources and the detection tools for monitoring the data sources in your environment.

## Before you begin

Role required:

-   sn\_ti.admin, sn\_si.admin: write, delete access
-   sn\_ti.read: read access

## About this task

You can identify the data sources and the detection tools that your organization needs to detect the techniques effectively.

For example, if your organization focuses on 5 techniques, you may need 10 data sources and 10 detection tools to monitor those sources. Let's say that you identify that your organization does not have two data sources and five detection tools. This exercise gives you visibility into the data sources, their relevance to your organization, and to identify gaps in the coverage. You can also focus on enhancing your environment with the right data sources and detection tools.

All the active tactics, techniques, ID, and data sources are automatically populated based on your [TAXII profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/setup-mitre-profile.md)

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **MITRE ATT&amp;CK Administration** &gt; **Data Source Mapping**.

    The following illustration shows the list of tactics, techniques, and their IDs that have been populated based on your collection updates.

    \[Omitted image "mitre-data-source-mapping.png"\] Alt text: Map data sources.

<table id="table_ayl_v1r_znb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tactic

</td><td>

Adversary’s objective or the reason for performing an action.

</td></tr><tr><td>

ID

</td><td>

Technique’s unique identity.

</td></tr><tr><td>

Technique

</td><td>

How an adversary achieves a tactical objective by performing an action.

</td></tr><tr><td>

Data Source

</td><td>

Data source that is associated with the technique.

</td></tr><tr><td>

Data Source Revoked

</td><td>

Data source is revoked if set to true, however the data source mapping is still retained.If the data source value is not found in MITRE, then the Data Source Revoked value is automatically marked as true. The data source mapping for a record is revoked if the technique and data source relationships are missing from the updated MITRE data.

 Default: false

</td></tr><tr><td>

Data Source Available

</td><td>

Availability of the data source.

</td></tr><tr><td>

Detection Tool

</td><td>

Tool that supplements the data source by detecting the techniques that are used. The detection tool is mapped with the alert sensor in SIR.

</td></tr><tr><td>

Revoked

</td><td>

The data source mapping for a record is revoked if the technique and data source relationships are missing from the updated MITRE data.Default: false

</td></tr></tbody>
</table>2.  Review the listed data sources and modify the value in the **Data Source Available** field based on your environment.

3.  **Note:** You cannot edit this entry from the list view.

    In the **Detection Tool** field, do the following steps:

    1.  Click the information icon, and click **Open Record**.
    2.  Unlock **Detection Tool** entry.
    3.  Use the lookup list to select a detection tool. You can multi-select detection tools.
    4.  Click **Update**.
    In the following illustration, multiple detection tools are added to monitor the data source.

    \[Omitted image "mitre-select-detection-tool.gif"\] Alt text: How to map the detection tool.


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

[Define the data source and data component mapping]()

[Define the technique detection coverage]()

[Map your technique detection coverage to a technique]()

[Define the mitigation coverage]()

[Map your mitigation coverage to a technique]()

[Create and map detection rules]()

[Auto-extract technique rules for importing MITRE-ATT&amp;CK information]()

[Review threat group and MITRE-ATT&amp;CK techniques mapping]()

[Threat group to technique heatmap definition]()

[Review the MITRE-ATT&amp;CK system properties]()

