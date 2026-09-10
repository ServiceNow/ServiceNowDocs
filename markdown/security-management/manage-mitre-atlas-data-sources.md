---
title: Map data sources and detection tools for MITRE ATLAS
description: Map detection tools to MITRE ATLAS techniques and tactics to identify monitoring capabilities for your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/security-management/manage-mitre-atlas-data-sources.html
release: yokohama
topic_type: task
last_updated: "2026-08-07"
reading_time_minutes: 1
breadcrumb: [MITRE ATLAS framework, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Map data sources and detection tools for MITRE ATLAS

Map detection tools to MITRE ATLAS techniques and tactics to identify monitoring capabilities for your organization.

## Before you begin

Role required:

-   sn\_ti.admin, sn\_si.admin: write, delete access
-   sn\_ti.read: read access

## About this task

You can identify the detection tools that you to detect MITRE ATLAS techniques effectively.

Active MITRE ATLAS tactics, techniques, and IDs are automatically populated in this list based on your active MITRE ATLAS TAXII profile, alongside the MITRE-ATT&amp;CK rows.

You can map a detection tool to a MITRE ATLAS technique row using the same steps as for a MITRE-ATT&amp;CK technique row.

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **MITRE ATT&amp;CK Administration** &gt; **Data Source Mapping**.

    This list shows the tactics, techniques, and IDs that have been populated based on your collection updates, for both MITRE-ATT&amp;CK and MITRE ATLAS.

    |Field|Description|
    |-----|-----------|
    |Tactic|Adversary’s objective or the reason for performing an action.|
    |ID|Technique’s unique identity. For MITRE ATLAS techniques, this is an AML-prefixed ID \(for example, `AML.T0000`\).|
    |Technique|How an adversary achieves a tactical objective by performing an action.|
    |Data Source|Data source that is associated with the technique. Not populated for MITRE ATLAS techniques in this release.|
    |Data Source Revoked|Data source is revoked if set to true, however the data source mapping is still retained.|
    |Data Source Available|Availability of the data source.|
    |Detection Tool|Tool that supplements the data source by detecting the techniques that are used. The detection tool is mapped with the alert sensor in SIR. You define this value; it applies to MITRE ATLAS technique rows the same way it applies to MITRE-ATT&amp;CK technique rows.|
    |Revoked|The data source mapping for a record is revoked if the technique and data source relationships are missing from the updated MITRE data.|

2.  In the **Detection Tool** field for a MITRE ATLAS technique row, do the following:

    **Note:** You can't edit this entry from the list view.

    1.  Select the information icon, and select **Open Record**.

    2.  Unlock the **Detection Tool** entry.

    3.  Use the lookup list to select a detection tool.

    4.  Select **Update**.


