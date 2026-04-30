---
title: Schedule the DLP IR Microsoft incident retrieval
description: Set a schedule to retrieve the incident data and ingest Microsoft DLP IR incidents that match the criteria in the profile. Configure the schedule to define how and when you pull incidents from Microsoft.
locale: en-US
release: xanadu
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create a new incident profile for Microsoft DLP integration, Data Loss Prevention Incident Response with Microsoft, DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Schedule the DLP IR Microsoft incident retrieval

Set a schedule to retrieve the incident data and ingest Microsoft DLP IR incidents that match the criteria in the profile. Configure the schedule to define how and when you pull incidents from Microsoft.

## Before you begin

Role required: sn\_dlir.admin\(Create, edit, and delete\)

sn\_dlir.analyst - View \(read-only\)

## About this task

You can plan how often you’ll poll for future incidents that match the incident profile configuration. To enable automated incident ingestion, you must configure the scheduling and incident retrieval before you activate the profile. The profile can be configured to do one-time retrieval using the **One-Time Retrieval** check box. The historical date can be up to the last three months from the current date.

The polling interval is configured for each profile individually. The different polling intervals may impact the performance of the Microsoft DLP IR incident integration. When scheduling, plan to balance the system load against the urgency of an incident.

## Procedure

1.  Set a schedule to retrieve data and ingest incidents that match the criteria in the profile.

2.  On the form, fill in the fields.

<table id="table_jyk_kcz_2tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Ongoing Incident Ingestion

</td><td>

The ongoing incident ingestion that the ServiceNow AI Platform instance pulls from Microsoft for new incidents. DLP IR incidents are created if triggered incidents are found and the incident generation filtering criteria matches.

</td></tr><tr><td>

Polling increment \(minutes\)

</td><td>

The polling frequency from Microsoft. This field is automatically set to 300 minutes.

</td></tr><tr><td>

Set Initial Incident Ingestion Time

</td><td>

Option to define a date and time for the initial ingestion. Subsequent ingestions are based on the polling interval period. This option is visible only when the **Ongoing incident ingestion** field is selected.

</td></tr><tr><td>

Input Initial Incident Ingestion Time

</td><td>

Date and time that you specify for the incident ingestion.-   If the value is set, then data retrieving from Microsoft will start from the added future date.
-   This field is visible only when the **Set Initial ingestion time** is selected.


</td></tr><tr><td>

Initial Incident Ingestion Time

</td><td>

First time when the data is ingested.You can see the that values start showing up when the initial incident ingestion time is set.

</td></tr><tr><td>

Next Incident Ingestion Time \(estimated\)

</td><td>

The next period for an estimated incident ingestion.

</td></tr><tr><td>

One-Time Retrieval

</td><td>

Option to enable one-time historical data pulls.If this field is selected, then historical data is pulled from Microsoft DLP IR according to the date added in the **Since Date** field.

</td></tr><tr><td>

Since Date

</td><td>

Date from when data is supposed to be retrieved from Microsoft. This field can be set to a maximum of 7 days.

</td></tr></tbody>
</table>3.  Save the created profile configuration by clicking **Finish** on the pop-up window.

4.  Activate the profile.

    1.  Open the created profile.

    2.  Enable the **Active** option.

    3.  Click **Update**.


## Result

After the successful creation and activation of the profile, the incidents are retrieved periodically as per the configuration set in the profile and added into the DLP incidents table.

**Parent Topic:**[Create a new incident profile for Microsoft DLP integration](create-profile-microsoft-dlp-integration.md)

