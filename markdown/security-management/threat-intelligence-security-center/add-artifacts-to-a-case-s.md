---
title: Add artifacts to case\(s\) or case task\(s\)
description: After you have created a case, you can view or add artifacts, such as security incidents, CIs, and indicators of compromise, to the case. These artifacts act as clues in solving the case.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Threat Analyst Workbench, Use, Threat Intelligence Security Center, Security Operations]
---

# Add artifacts to case\(s\) or case task\(s\)

After you have created a case, you can view or add artifacts, such as security incidents, CIs, and indicators of compromise, to the case. These artifacts act as clues in solving the case.

## Before you begin

Role required: admin

**Note:** Artifacts are available only to the existing cases. For observables and indicators, the artifacts can also be added or associated to a case from the import job using the Import Intelligence button. For more information on how to import see, [Import Intelligence in TISC](../concept/importing-threat-intelligence.md)

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click **Threat Analyst Workbench** icon.

3.  Go to **Case Management** &gt; **All Cases**.

    All the cases are displayed.

4.  Select any case or case task.

5.  Go to **Artifacts** tab.

    The associated artifacts are displayed as the related lists for that specific case or case task.

6.  Link or Unlink the records from the case or case task.

    **Note:** For more information, see [Link Threat Intel Related Records](link-threat-intel-releated-records.md)

    Following table lists the artifacts related lists related to the case\(s\) or case task\(s\):

<table id="table_svf_lcn_2yb"><thead><tr><th>

Related List

</th><th>

Description

</th></tr></thead><tbody><tr><td>

MITRE Techniques

</td><td>

List the MITRE techniques related to the case\(s\).MITRE techniques also displays all the associated techniques in a case.

</td></tr><tr><td>

Observable

</td><td>

List of observables related to this cases or case tasks.

</td></tr><tr><td>

Indicators

</td><td>

List of indicators related to this cases or case tasks.

</td></tr><tr><td>

Attack Patterns

</td><td>

List of attack patterns that are related to this cases or case tasks.

</td></tr><tr><td>

Campaigns

</td><td>

List the campaigns that are related to this cases or case tasks.

</td></tr><tr><td>

Course of Actions

</td><td>

List the course of actions that are related to this cases or case tasks.

</td></tr><tr><td>

Data Components

</td><td>

List of Data Components that are related to this cases or case tasks.

</td></tr><tr><td>

Threat Groupings

</td><td>

List the threat groupings that are related to this cases or case tasks.

</td></tr><tr><td>

Identities

</td><td>

List the identities that are related to this cases or case tasks.

</td></tr><tr><td>

Infrastructure

</td><td>

List the Infrastructure such as systems, software services, and any associated physical or virtual resources that are related to this cases or case tasks.

</td></tr><tr><td>

Intrusion Sets

</td><td>

List the intrusion sets such as a set of adversarial behaviors and resources with common properties that are related to this cases or case tasks.

</td></tr><tr><td>

Locations

</td><td>

List the locations records that are related to this cases or case tasks.

</td></tr><tr><td>

Malware

</td><td>

List the malware source records that are related to this cases or case tasks.

</td></tr><tr><td>

Marking Definitions

</td><td>

List the marking definitions records that are related to this cases or case tasks.

</td></tr><tr><td>

Threat Notes

</td><td>

List the marking definitions records that are related to this cases or case tasks.

</td></tr><tr><td>

Observed Data

</td><td>

List the observed data that are related to this cases or case tasks.

</td></tr><tr><td>

Threat Opinions

</td><td>

List the threat opinions that are related to this cases or case tasks.

</td></tr><tr><td>

Threat Reports

</td><td>

List the threat reports that are related to this cases or case tasks.

</td></tr><tr><td>

Sightings

</td><td>

List of sightings that are related to this cases or case tasks.

</td></tr><tr><td>

Threat Actors

</td><td>

List the threat actors that are related to this cases or case tasks.

</td></tr><tr><td>

Tools

</td><td>

List the tools that are related to this cases or case tasks.

</td></tr><tr><td>

Vulnerabilities

</td><td>

If the observable is an IP address, this list shows any resources \(configuration items\) that have a matching IP address that are related to this cases or case tasks.

</td></tr><tr><td>

Related Cases

</td><td>

Lists the related cases.

</td></tr><tr><td>

Related Case Tasks

</td><td>

Lists the related case tasks.

</td></tr><tr><td>

Security Incidents

</td><td>

List the security incidents that are related to this cases or case tasks.

</td></tr><tr><td>

Affected Configuration Items

</td><td>

List the affected configurations items that are related to this cases or case tasks.

</td></tr><tr><td>

Affected Services

</td><td>

List the affected services that are related to this cases or case tasks.

</td></tr><tr><td>

Affected Assets

</td><td>

List the affected assets that are related to this cases or case tasks.

</td></tr><tr><td>

Vulnerability Entries

</td><td>

List the vulnerability entries that are related to this cases or case tasks.

</td></tr></tbody>
</table>
-   **[Roll up of MITRE Techniques from Artifacts to Case](roll-up-mitre-case.md)**  
When intelligence records are added to a case, all associated MITRE Techniques are automatically rolled up to the case level.
-   **[Show MITRE ATT&amp;CK Framework for a Case\(s\)](tisc-show-mitre-fw.md)**  
Displays all the associated techniques of a case on the MITRE ATT&amp;CK framework.

**Parent Topic:**[Threat Analyst Workbench](../concept/threat-analyst-workbench.md)

**Related topics**  


[Workbench Overview](../concept/workbench-overview.md)

[Creating cases using Threat Analyst Workbench](../concept/create-cases-using-threat-analyst-workbench.md)

[Creating case task using Threat Analyst Workbench](tisc-create-case-task.md)

[Working with Investigation Canvas](../concept/tisc-investigation-canvases.md)

[Run Enrichment Actions within a case](run-enrichment-results.md)

[View Case Reports](view-case-reports.md)

[Create a security incident from a TISC case](tisc-create-si-case.md)

[Upload Secure File Attachments](secure-file-attachments.md)

