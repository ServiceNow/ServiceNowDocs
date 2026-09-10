---
title: Link and unlink TISC records to a security incident
description: Link TISC records such as observables, threat actors, and malware to a security incident, or unlink records that you no longer need.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/tisc-link-unlink-records-sir.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-08-18"
reading_time_minutes: 2
keywords: [link, unlink, TISC Context, security incident, Threat Intelligence Security Center]
breadcrumb: [Working with TISC Context, TISC integration within SIR Workspace, Working with Security Incident Records, Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Link and unlink TISC records to a security incident

Link TISC records such as observables, threat actors, and malware to a security incident, or unlink records that you no longer need.

## Before you begin

Role required: sn\_si.analyst, sn\_sec\_tisc.library\_write, sn\_sec\_tisc.case\_write

## About this task

From the **TISC Context** tab of a security incident, you can associate a TISC record directly with the security incident without creating a TISC case first. Linking a record only associates it with the security incident. It doesn't create a copy of the record in Security Incident Response Workspace.

You can also link a security incident from the TISC side. For more information, see [View Internal Intelligence Records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/view-internal-intelligence-records.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace** &gt; **Security Incidents** &gt; **All**.

2.  Open the security incident you're investigating.

3.  Select **TISC Context**.

4.  Select the option that has the record you want to link or unlink.

    The **TISC Context** tab contains the following options.

    |Name|Description|
    |----|-----------|
    |TISC Cases|The TISC cases associated with the security incident. In earlier releases this list was labeled **Cases**.|
    |Observables|The TISC observables associated with the security incident.|
    |Vulnerabilities|The vulnerabilities associated with the security incident.|
    |Campaigns|The campaigns associated with the security incident.|
    |Intrusion Sets|The intrusion sets associated with the security incident.|
    |Malware|The malware associated with the security incident.|
    |Threat Actors|The threat actors associated with the security incident.|
    |Threat Reports|The threat reports associated with the security incident.|

    **Note:**

    The **Threat Actors** list includes threat actor motivation columns, and the **Malware** list includes malware capability columns.

5.  To link records, select **Link**.

    1.  In the link window, apply the advanced filters to narrow the list of available records.

    2.  Select one or more records.

    3.  Select **Link** for TISC Cases or **Add** for the other options.

    The selected records are associated with the security incident. When you close the link window, a single consolidated work note is posted on the security incident for all the records that were linked. Records that failed to link, and records that were already linked, are excluded from the work note.

6.  To remove links, select one or more records and select **Unlink**.

    A confirmation window is displayed. After you confirm, the association is removed.

7.  To create an Observable in the SIR Workspace and link it, select **Create and Link to SI**.

8.  To view the enrichment results for an Observable, select **View Enrichment Results**.

9.  In TISC Cases, select **View Related Artifacts** to view the related records or entities.

10. Select **View Related Info** to view information, such as the threat actors, attack patterns, campaigns, or cases related to the incident.

    **View Related Info** is available for all the options except TISC Cases.


## Result

Linking or Unlinking immediately reflects in TISC in the **Internal Intelligence** tab of records.

**Parent Topic:**[Working with TISC Context](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/working-with-tisc-context.md)

**Related topics**  


[TISC integration with SIR Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-integration-with-sir-workspace.md)

[View Internal Intelligence Records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/view-internal-intelligence-records.md)

