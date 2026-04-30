---
title: Schedule incident retrieval
description: Configure a schedule to define how and when you pull incidents from Cortex XSIAM tenant.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-11-11"
reading_time_minutes: 1
breadcrumb: [Security Incident Response Integration with Cortex XSIAM by Palo Alto Networks, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Schedule incident retrieval

Configure a schedule to define how and when you pull incidents from Cortex XSIAM tenant.

## Before you begin

Role required: sn\_si.admin, sn\_si.ingestion\_profile\_admin

## Procedure

1.  If you are not continuing from the previous section of the Filtering and Aggregation criteria, access the profile you are defining.

    1.  Navigate to **All** &gt; **Palo Alto Networks XSIAM** &gt; **XSIAM Profile**.

    2.  Select the profile you are continuing to define.

    3.  Select **Scheduling** in the progress bar.

2.  On the form, fill in the fields.

<table id="table_kyc_qbg_p4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Ongoing incident ingestion

</td><td>

Option to set ongoing incident ingestion that the ServiceNow AI Platform instance pulls from the Cortex XSIAM tenant for new incidents. Security incidents are created if triggered incidents are found and the incident generation filtering criteria matches.

</td></tr><tr><td>

Polling increment \(minutes\)

</td><td>

Polling frequency defined in minutes.

</td></tr><tr><td>

Set incident ingestion time

</td><td>

Option to add Date and time for the initial ingestion.

</td></tr><tr><td>

Initial incident ingestion time

</td><td>

Date and time that you specify for the incident ingestion.

</td></tr><tr><td>

One-Time Retrieval

</td><td>

Option to enable one-time retrieval of historical Cortex XSIAM incidents and followed by the reconciliation of the data.When processing the data, both ongoing incidents and historical data are pulled.

**Note:** The retrieved historical Cortex XSIAM incidents undergo de-duplication checks to avoid any duplicates within the Security Incident Response application.

</td></tr><tr><td>

Since date

</td><td>

The date since historical incidents were ingested from Cortex XSIAM.

</td></tr></tbody>
</table>3.  Select **Continue**.


## What to do next

[Automate incident updates and closures](pan-xsiam-automate-inc-updates.md)

