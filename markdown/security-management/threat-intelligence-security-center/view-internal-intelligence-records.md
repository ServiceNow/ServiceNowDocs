---
title: View Internal Intelligence Records
description: View the internal intelligence records collected from CMDB, Security Incident Response \(SIR\), Vulnerability Response \(VR\) these records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/threat-intelligence-security-center/view-internal-intelligence-records.html
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-08-18"
reading_time_minutes: 1
breadcrumb: [Working with Internal Intelligence Records, Observables, TISC Library Repository, Threat Intel Library, Use, Threat Intelligence Security Center, Security Operations]
---

# View Internal Intelligence Records

View the internal intelligence records collected from CMDB, Security Incident Response \(SIR\), Vulnerability Response \(VR\) these records.

## Before you begin

Internal Intelligence section provides the context from other applications on the platform such as SIR, VR and CMDB to provide broader perspective of the threat to the analysts.

Role required: sn\_sec\_tisc.analyst

**Note:** The **Internal Intelligence** tab is available for observables, vulnerabilities, threat actors, malware, campaigns, intrusion sets, and threat reports.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Threat Intel Library** &gt; **Observables** &gt; **All Observables**.

2.  Select any observable record.

3.  Go to **Internal Intelligence** tab.

    The Internal intelligence section contains three subsections, Security Incident Response, Business Context, Vulnerability Response.

    **Note:** You must have the respective applications installed on your instance for these sections to be listed within **Internal Intelligence** tab.

    1.  **Security Incident Response**: Displays all the incidents that are linked with the observables.

        **Note:** You can also link and unlink the records by searching the records within the source systems. For more information, see [Link Threat Intel Related Records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/threat-intelligence-security-center/link-threat-intel-releated-records.md).

        Select any record to navigate and view the details in the source system. For example, Associated Observables in Security Incident Response to fetch the associated observable records.

    2.  **Business Context**: Displays the affected users and any other configuration items. As part of the current release, following is the intelligence data that you can fetch from the source \(Business Context\) records:
        -   Configuration Items
        -   Affected Services
        -   Affected Assets
    3.  **Vulnerability Response**: Displays the vulnerabilities intelligence data.
4.  To link a security incident to the entity, select the incident, and select **Link**.

    Select one or more security incidents and confirm your selection. The security incidents appear in the **Security Incidents** subsection.

5.  To unlink a security incident, select one or more security incidents and select **Unlink**.

    After you confirm, the security incidents are removed from the subsection.


## Result

The changes made in the TISC context or TISC internal intelligence tabs reflect bidirectionally in the TISC and SIR workspaces.

**Parent Topic:**[Working with Internal Intelligence Records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/threat-intelligence-security-center/working-with-ti-internal-intelligence-records.md)

