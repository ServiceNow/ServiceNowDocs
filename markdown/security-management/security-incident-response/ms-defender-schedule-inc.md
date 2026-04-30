---
title: Schedule incident retrieval
description: Set a schedule that determines how frequently Microsoft Defender incidents are pulled into SIR to ensure timely and efficient ingestion.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-01-06"
reading_time_minutes: 1
breadcrumb: [Microsoft Defender integration for Security Operations, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Schedule incident retrieval

Set a schedule that determines how frequently Microsoft Defender incidents are pulled into SIR to ensure timely and efficient ingestion.

## Before you begin

Role required: sn\_si.admin, sn\_si.ingestion\_profile\_admin

## Procedure

1.  If you aren’t continuing from the previous section of the Filtering and Aggregation criteria, access the profile you’re defining.

    1.  Navigate to **All** &gt; **Microsoft Defender Integration** &gt; **Defender Incident Profiles**.

    2.  Select the profile that you’re continuing to define.

    3.  Select **Scheduling** in the progress bar.

2.  On the form, fill in the fields.

<table id="table_kyc_qbg_p4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Ongoing incident ingestion

</td><td>

Option to set ongoing incident ingestion that the ServiceNow AI Platform instance pulls from the Microsoft tenant for new incidents. Security incidents are created if triggered incidents are found and the incident generation filtering criteria matches.

</td></tr><tr><td>

Polling increment \(minutes\)

</td><td>

Polling frequency defined in minutes.

</td></tr><tr><td>

Set incident ingestion time

</td><td>

Option to add Date and time for the initial ingestion.

</td></tr><tr><td>

Input incident ingestion time

</td><td>

Date and time that you specify for the incident ingestion.

</td></tr><tr><td>

One-Time Retrieval

</td><td>

Option to enable one-time retrieval of historical Microsoft Defender incidents and followed by the reconciliation of the data.When processing the data, both ongoing incidents and historical data are pulled.

**Note:** The retrieved historical Microsoft Defender incidents undergo de-duplication checks to avoid any duplicates within the Security Incident Response application.

</td></tr><tr><td>

Since date

</td><td>

The date since historical incidents were ingested from Microsoft.

</td></tr></tbody>
</table>    ![Schedule incident retrieval](../image/ms-def-scheduling.png)

3.  Select **Continue**.


## What to do next

[Automate incident updates and closures](ms-defender-additional-op.md)

