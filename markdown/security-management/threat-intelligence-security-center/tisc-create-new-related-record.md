---
title: Create a related record to link
description: Create a threat intelligence record directly from a related records list and link it to the record that you're viewing, without leaving your investigation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-create-new-related-record.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-08-15"
reading_time_minutes: 1
keywords: [create, related records, Threat Intelligence Security Center]
breadcrumb: [Observables, TISC Library Repository, Threat Intel Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Create a related record to link

Create a threat intelligence record directly from a related records list and link it to the record that you're viewing, without leaving your investigation.

## Before you begin

Role required: `sn_sec_tisc.analyst`

## About this task

While reviewing a threat intelligence record, create a record and link it within the flow.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Open the record that you want to link the new record to.

3.  Go to the related list for the type of record that you want to create.

    The following table lists the records that support creating a new related record and where the related lists appear.

    |Record|Where the related records appear|
    |------|--------------------------------|
    |Observable|**Related Records** section of the observable record.|
    |Indicator|**Related Records** section of the indicator record.|
    |Object, such as an attack pattern or a malware object|**Related Records** section of the object record.|
    |Case|**Artifacts** tab of the case.|
    |Case task|**Artifacts** tab of the case task.|
    |RSS feed|**Related Records** section of the RSS feed record.|
    |Vulnerabilities|**Related Records** section of the vulnerabilities.|

4.  Select **New**.

    The record form for that record type opens.

5.  Complete the fields on the record form.

6.  Select **Save**, and then select **Continue**.


## Result

The new record appears in the related list of the record you started from.

**Parent Topic:**[Observables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/observables.md)

