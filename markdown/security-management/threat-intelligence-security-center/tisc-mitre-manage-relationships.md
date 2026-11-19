---
title: Manage MITRE Relationships
description: Manage the MITRE relationships information that you imported from the MITRE TAXII collections.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/security-management/threat-intelligence-security-center/tisc-mitre-manage-relationships.html
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [MITRE-ATT&amp;CK repository, TISC Library Repository, Threat Intel Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Manage MITRE Relationships

Manage the MITRE relationships information that you imported from the MITRE TAXII collections.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## About this task

MITRE tactics are broad goals, and techniques are the methods used to achieve them. A technique can be linked to more than one tactic. MITRE maintains these tactic-technique mappings and updates them with each release.

When you add a MITRE technique to a case, these mappings determine which tactics are available to select. If MITRE no longer maps a technique to a tactic, that combination won't be available. For details about mappings that MITRE has removed, see [Review revoked MITRE tactic and technique associations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/threat-intelligence-security-center/tisc-review-revoked-mitre-associations.md).

## Procedure

1.  To view the MITRE ATT&amp;CK Repository data, navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Threat Intel Library** &gt; **MITRE ATT&amp;CK** &gt; **Relationships**.

    You can view the listed relationships.

2.  Select any source object to view all the associated information.

3.  Select **New** to manually create the MITRE ATT&amp;CK relationships.

4.  Fill in the fields appropriately.

<table id="table_xpf_yd5_g1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source MITRE Object

</td><td>

Add the source MITRE object.

</td></tr><tr><td>

Target MITRE Object

</td><td>

Add the target MITRE object.

</td></tr><tr><td>

Source MITRE Type

</td><td>

Enter the source MITRE type.

</td></tr><tr><td>

Target MITRE Type

</td><td>

Enter the target MITRE type.

</td></tr><tr><td>

Relationship Type

</td><td>

Specifies the direction of the relationship between the observable and the object. The available options are:-   Inverse - The relationship is defined from the observable to the object.
-   Direct - The relationship is defined from the object to the observable.


</td></tr><tr><td>

Source

</td><td>

Select and define the source object.

</td></tr><tr><td>

Relationship ID

</td><td>

Define the relationship ID.

</td></tr></tbody>
</table>5.  Select **Save**.

6.  To view how these objects are related, select **Relationships**.


**Parent Topic:**[MITRE-ATT&amp;CK repository](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/threat-intelligence-security-center/tisc-mitre-att-ck-framework-overview.md)

