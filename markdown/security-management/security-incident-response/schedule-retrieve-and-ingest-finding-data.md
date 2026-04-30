---
title: Schedule the AWS Security Hub finding retrieval
description: Set a schedule to retrieve the finding data and to ingest the AWS Security Hub findings that match the criteria in the profile.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Amazon Web Services \(AWS\) Security Hub integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Schedule the AWS Security Hub finding retrieval

Set a schedule to retrieve the finding data and to ingest the AWS Security Hub findings that match the criteria in the profile.

## Before you begin

Role required: sn\_sni.admin

## About this task

You can plan how often you want to poll for future AWS Security Hub findings that match the AWS Security Hub finding profile configuration.

The polling interval is configured for each profile individually. The different polling intervals may impact the performance of the AWS Security Hub findings integration. When scheduling, plan to balance the system load against the urgency of an incident. A one-minute default value is set for all profiles. You can modify this setting based on the urgency of the incident and the anticipated load on your system.

Any alerts that gets added to the incident in a particular polling interval is processed and then appended to the AWS Security Hub alerts related lists and comments.

## Procedure

1.  On the scheduling form, fill in the fields.

    Configure the schedule to define how and when you pull findings from the AWS Security Hub tenant.

<table id="table_kyc_qbg_p4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Ongoing finding ingestion

</td><td>

Ongoing finding ingestion that the ServiceNow AI Platform instance pulls from the AWS Security Hub tenant for new incidents. Security incidents are created if triggered findings are found and the security incident generation filtering criteria matches.

</td></tr><tr><td>

Poll closed findings

</td><td>

Polling findings that have been resolved.These findings are ingested during ongoing incident ingestion.

</td></tr><tr><td>

Polling increment \(minutes\)

</td><td>

Polling frequency that is defined in minutes.

</td></tr><tr><td>

Set Initial finding ingestion time

</td><td>

Findings ingestion that is based on the configured date and time.You can use this option to define a specific date and time for the initial ingestion. Subsequent ingestions are based on the polling interval period.

</td></tr><tr><td>

Input Initial finding ingestion time

</td><td>

Date and time that you specify for the incident ingestion.

</td></tr><tr><td>

One-Time Retrieval

</td><td>

Select this checkbox to allow one-time retrieval of historical AWS Security Hub findings and then do the reconciliation of the data. When you select this checkbox, the application will pull all the open and closed AWS Security Hub findings for the period up to 90 days approximately.When processing the data both ongoing findings and historical data are pulled, but the processing of the ongoing findings takes precedence over historical pull. Otherwise, the historical pull may take some time based on the duration as well as the number of findings that are ingested.

**Note:** The retrieved historical AWS Security Hub findings undergo de-duplication checks to prevent any duplicates within the Security Incident Response application.

</td></tr><tr><td>

Since date

</td><td>

The date since when the historical findings are ingested from AWS Security Hub.**Note:** The findings data is approximately pulled from the past 90 days.

</td></tr></tbody>
</table>    The scheduling page enables you to define how and when findings are pulled from the AWS Security Hub tenant.

2.  To navigate to the Additional Options page, click **Continue**.


