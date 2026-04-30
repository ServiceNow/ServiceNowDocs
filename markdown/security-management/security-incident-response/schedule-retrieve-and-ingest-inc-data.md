---
title: Schedule detection retrieval
description: Configure a schedule to define how and when you pull detections from the CrowdStrike Next-Gen SIEM tenant.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [CrowdStrike Next-Gen SIEM integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Schedule detection retrieval

Configure a schedule to define how and when you pull detections from the CrowdStrike Next-Gen SIEM tenant.

## Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin because the sn\_si.admin role inherits the required permissions by default.

## Procedure

1.  If you are not continuing from the previous section of the Filtering and Aggregation criteria, access the profile you are defining.

    1.  Navigate to **All** &gt; **CrowdStrike Next-Gen SIEM** &gt; **Detection Profile**.

    2.  Select the profile you are continuing to define.

    3.  Select **Scheduling** in the progress bar.

2.  On the scheduling form, fill in the fields.

<table id="table_kyc_qbg_p4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Ongoing detection ingestion

</td><td>

Option to set ongoing detection ingestion that the ServiceNow AI Platform instance pulls from the CrowdStrike Next-Gen SIEM tenant for new detections. Security incidents are created if triggered detections are found and the detection generation filtering criteria matches.

</td></tr><tr><td>

Polling increment \(minutes\)

</td><td>

Polling frequency defined in minutes.

</td></tr><tr><td>

Set detection ingestion time

</td><td>

Option to add Date and time for the initial ingestion.

</td></tr><tr><td>

Initial detection ingestion time

</td><td>

Date and time that you specify for the detection ingestion.

</td></tr><tr><td>

One-Time Retrieval

</td><td>

Option to enable one-time retrieval of historical CrowdStrike Next-Gen SIEM detections and followed by the reconciliation of the data.When processing the data, both ongoing detections and historical data are pulled.

**Note:** The retrieved historical CrowdStrike Next-Gen SIEM detections undergo de-duplication checks to avoid any duplicates within the Security Incident Response application.

</td></tr><tr><td>

Since date

</td><td>

The date since historical detections were ingested from CrowdStrike Next-Gen SIEM.

</td></tr></tbody>
</table>3.  Complete this section of the profile by selecting **Continue**.


## What to do next

[Automate detection updates and closures](automate-inc-crowdstrike-ng.md)

