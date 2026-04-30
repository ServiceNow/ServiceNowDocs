---
title: View Internal Intelligence Records
description: View the internal intelligence records collected from CMDB, Security Incident Response \(SIR\), Vulnerability Response \(VR\) these records.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Working with Internal Intelligence Records, Observables, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# View Internal Intelligence Records

View the internal intelligence records collected from CMDB, Security Incident Response \(SIR\), Vulnerability Response \(VR\) these records.

## Before you begin

Internal Intelligence section provides the context from other applications on the platform such as SIR, VR and CMDB to provide broader perspective of the threat to the analysts.

Role required: sn\_sec\_tisc.analyst

**Note:** Internal intelligence tab is only visible for observables and vulnerability objects.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Threat Intel Library** &gt; **Observables** &gt; **All Observables**.

2.  Select any observable\(s\) record.

3.  Go to **Internal Intelligence** tab.

    The Internal intelligence section comprises of three subsections such as Security Incident Response, Business Context, Vulnerability Response.

    **Note:** You must have the respective applications installed on your instance for these sections to be listed within **Internal Intelligence** tab.

    1.  **Security Incident Response**: Displays all the incidents that are linked with the associated observables, and vulnerability items.

        **Note:** The Observable\(s\) value must match between the SIR incident and also within the TISC only then the associated observables or indicators are listed under Security incident Response section. You can also link and unlink the records by searching the records within the source systems. For more information, see [Link Threat Intel Related Records](link-threat-intel-releated-records.md).

        -   Select any record to navigate and view the details in the source system. For example, Associated Observables in Security Incident Response to fetch the associated observable records.
        -   As part of the current release, following is the intelligence data that you can fetch from the source \(SIR\) records:
            -   Associated Observables
            -   Vulnerability items
    2.  **Business Context**: Displays the affected users and any other configuration items. As part of the current release, following is the intelligence data that you can fetch from the source \(Business Context\) records:
        -   Configuration Items
        -   Affected Services
        -   Affected Assets
    3.  **Vulnerability Response**: Displays the vulnerabilities intelligence data.

        Vulnerability Entries: This option match the vulnerabilities and fetch the related records.


**Parent Topic:**[Working with Internal Intelligence Records](../concept/working-with-ti-internal-intelligence-records.md)

