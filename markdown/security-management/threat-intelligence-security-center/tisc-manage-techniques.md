---
title: Manage Techniques
description: Manage the techniques that are imported from the MITRE TAXII collections. The techniques contain various ways attackers have developed to employ a given tactic. You can review and deactivate techniques that are not relevant to your organization. In STIX, techniques are known as attack patterns.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [MITRE-ATT&amp;CK Repository, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Manage Techniques

Manage the techniques that are imported from the MITRE TAXII collections. The techniques contain various ways attackers have developed to employ a given tactic. You can review and deactivate techniques that are not relevant to your organization. In STIX, techniques are known as attack patterns.

## Before you begin

Role required: sn\_sec\_tisc.analyst

Techniques represents how an adversary achieves a tactical goal by performing an action.

## Procedure

1.  After you enable the MITRE ATT&amp;CK related feed data sources which are available in the base system, click **Execute Now** to run the integrations and fetch the MITRE related information.

    For more information on enabling the integrations

2.  To view the MITRE ATT&amp;CK Repository data, navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Threat Intel Library** &gt; **MITRE ATT&amp;CK** &gt; **Techniques**.

    The MITRE ATT&amp;CK techniques records are displayed. By default all the records are in enabled state.

3.  Select any technique record and click **Disable** if you want to disable any specific record.

4.  Alternatively, you can create new techniques records by clicking **New** to manually create the MITRE ATT&amp;CK techniques.

5.  Fill in the fields appropriately.

<table id="table_xpf_yd5_g1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ID

</td><td>

Unique ID for a technique.

</td></tr><tr><td>

Name

</td><td>

Enter the name of the technique.

</td></tr><tr><td>

Source

</td><td>

Specifies the threat source from which this record is created.

</td></tr><tr><td>

Platforms

</td><td>

Add the platforms required.

</td></tr><tr><td>

Permissions required

</td><td>

Add the required permissions.

</td></tr><tr><td>

Created Time In Source

</td><td>

Specifies the time the object is created in the source.

</td></tr><tr><td>

Modified Time In Source

</td><td>

Specifies the time the object is modified in the source.

</td></tr><tr><td>

Priority

</td><td>

Indicates the priority level assigned to the MITRE Technique such as Low, Moderate, High, or Critical.**Note:** Priorities can be assigned to techniques to add relevance to your organization.

</td></tr><tr><td>

Description

</td><td>

A description that provides more details and context about the intrusion set, potentially including its purpose and its key characteristics.

</td></tr><tr><td>

Detection

</td><td>

The detection technique is used to identify adversary access to or unauthorized activity on computer networks.

</td></tr><tr><td colspan="2">

**Insights**

</td></tr><tr><td>

Notes

</td><td>

Any additional information related to the mitigation.

</td></tr><tr><td colspan="2">

**Additional Information**

</td></tr><tr><td>

Additional Context

</td><td>

Add any additional context for this object type.

</td></tr><tr><td>

Comments

</td><td>

Add any comments that you might have in addition.

</td></tr><tr><td colspan="2">

**TISC Tags**

</td></tr><tr><td>

Select TISC Tags

</td><td>

Select tags to annotate or earmark records ingested into the system from this source.**Note:** Tags can be assigned to techniques to add relevance to your organization.

</td></tr></tbody>
</table>
**Parent Topic:**[MITRE-ATT&amp;CK Repository](tisc-mitre-att-ck-framework-overview.md)

