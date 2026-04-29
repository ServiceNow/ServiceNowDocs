---
title: Installed with Asset Audit Response
description: Various components are installed on activation of the Asset Audit Response application.
locale: en-US
release: australia
product: Asset Audits
classification: asset-audits
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Asset Audit Response, IT Asset Management]
---

# Installed with Asset Audit Response

Various components are installed on activation of the Asset Audit Response application.

## Store applications installed

<table id="table_sbh_vns_ffc"><thead><tr><th>

Store application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Asset Audit Response\(com.sn\_audit\_response\)

</td><td>

Provides capabilities to track and manage financial regulatory audit engagements, evidence requests, and the responses to those requests.

</td></tr><tr><td>

GRC: Advanced Core\(com.sn\_grc\_advanced\)

</td><td>

Provides common functionality to support forward-looking use cases across GRC applications such as Risk, Policy &amp; Compliance, and Audit. Includes capabilities to manage issue triage workflows and evidence collection.

</td></tr><tr><td>

GRC: Policy and Compliance Management\(com.sn\_compliance\)

</td><td>

Provides capabilities to create and manage policies, standards, and internal control procedures cross-mapped to external regulations. Also provides structured workflows for identifying, assessing, and monitoring control activities.

</td></tr><tr><td>

GRC: Audit Management Workspace\(com.sn\_audit\_workspace\)

</td><td>

Provides a single-pane view where audit supervisors and auditors can view the overall audit timeline and status, track budget and resources for engagements, track high-priority observations and issues, and monitor ongoing control testing and audit task progress. Auditors can also test the effectiveness of controls, request evidence, create observations, and complete other audit activities.

</td></tr><tr><td>

IRM Feature Role\(com.sn\_grc\_ftr\_role\)

</td><td>

Provides access controls to regulate the Governance, Risk, and Compliance \(GRC\) data and capabilities that users can view or use.

</td></tr><tr><td>

GRC: Financial Services Controls Accelerator\(com.sn\_finserv\_cntrl\)

</td><td>

Provides cybersecurity and technology controls for the financial services industry.

</td></tr></tbody>
</table>## Roles installed

<table id="table_zsw_nms_ffc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Asset governance\[sn\_audit\_response.asset\_governance\]

</td><td>

This role can fulfill and respond to evidence requests.

</td><td>

-   sn\_grc\_advanced.evidence\_responder
-   sam\_user \(available only if you have installed the Software Asset Management application on your ServiceNow instance\)
-   sn\_hamp.ham\_user \(available only if you have installed the Hardware Asset Management application on your ServiceNow instance\)
-   asset \(available only if you have installed the Hardware Asset Management application on your ServiceNow instance\)

</td></tr><tr><td>

Asset audit manager\[sn\_audit\_response.grc\_asset\_audit\_manager\]

</td><td>

This role can create audit engagements, activities, evidence requests, and entity scopes.

</td><td>

-   sn\_audit.shared\_manager
-   sn\_grc\_advanced.evidence\_requester

</td></tr></tbody>
</table>## Tables installed

<table id="table_lf2_rms_ffc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Asset Evidence\[amg\_asset\_evidence\]

</td><td>

List of evidence records that you have created for all evidence requests.

</td></tr><tr><td>

Asset Evidence Task\[amg\_asset\_evidence\_task\]

</td><td>

List of asset evidence tasks.

</td></tr><tr><td>

Evidence Remediation Rule\[amg\_evidence\_remediation\_rule\]

</td><td>

List of remediation rules that you have created for your evidence records.

</td></tr><tr><td>

Evidence Remediation Task\[amg\_evidence\_remediation\_task\]

</td><td>

List of remediation tasks that are generated for all evidence requests.

</td></tr></tbody>
</table>**Parent Topic:**[Asset Audit Response reference](../concept/asset-audit-response-references.md)

