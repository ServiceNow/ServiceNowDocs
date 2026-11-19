---
title: View and activate a MITRE ATLAS matrix
description: View the tactics and techniques in an imported MITRE ATLAS matrix to understand available threat intelligence data. You can activate the matrix to make it available for use in threat analysis.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/manage-mitre-atlas-matrices.html
release: zurich
topic_type: task
last_updated: "2026-08-07"
reading_time_minutes: 1
breadcrumb: [MITRE ATLAS framework, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# View and activate a MITRE ATLAS matrix

View the tactics and techniques in an imported MITRE ATLAS matrix to understand available threat intelligence data. You can activate the matrix to make it available for use in threat analysis.

## Before you begin

Role required: sn\_ti.admin \(delete access\) or sn\_ti.read \(read access\) or sn\_ti.write \(create, write access\)

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **MITRE ATLAS Repository** &gt; **Matrices**.

    The matrix is inactive by default.

2.  To activate the matrix, move to **Active**, double-click, and select **true**.

3.  To view all the associated information, select the matrix.

4.  To view all the tactics that are associated with this collection, select the **MITRE Tactics** tab.

5.  Open a tactic to view its associated techniques and details.

    \[Omitted image "mitre-atlas-adversary-technique.png"\] Alt text: Screenshot showing the MITRE ATT&amp;CK Techniques tab with a list of techniques associated with the selected tactic

6.  Under the **MITRE ATT&amp;CK Techniques** tab, select a technique.

7.  Under the related lists, view the associations that are available for the technique that you selected.


## What to do next

You can [extend the information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/view-and-extend-information.md) in some of these related list objects based on the technique that you selected. For example, you can add new information for Group, Mitigation, External References, Malware, and Tools.

