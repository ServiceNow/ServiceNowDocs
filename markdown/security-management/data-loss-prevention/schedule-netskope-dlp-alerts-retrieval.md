---
title: Schedule the Netskope DLP incidents retrieval
description: Set a schedule to retrieve Netskope DLP incidents that match the criteria in the profile.
locale: en-US
release: zurich
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a Profile for Netskope DLP integration, Data Loss Prevention Incident Response Integration with Netskope, Integrate, Data Loss Prevention Incident Response, Security Operations]
---

# Schedule the Netskope DLP incidents retrieval

Set a schedule to retrieve Netskope DLP incidents that match the criteria in the profile.

## Before you begin

Role required: sn\_dlir.admin

## About this task

You can plan how often you will poll for net new Netskope incidents that match the incident profile configuration. To enable automated incident ingestion, you must configure the scheduling and incident retrieval before you activate the profile. The profile can be configured to do one-time retrieval using the **One-Time Retrieval** check box. The historical date can be up to one month from the past.

## Procedure

1.  Configure the schedule to define how and when you pull incidents from Netskope.

2.  On the form, fill in the fields.

<table id="table_lc5_dd2_ltb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Ongoing Incident Ingestion

</td><td>

Ongoing incident ingestion that your ServiceNow AI Platform instance pulls from  Netskope for new incidents. If there are triggered incidents found, which match with the incident filtering criteria, then DLP incidents are created.

</td></tr><tr><td>

Polling increment \(minutes\)

</td><td>

Polling frequency that is defined in minutes. This default value is set to **5**.

</td></tr><tr><td>

Set Initial Incident Ingestion Time

</td><td>

Option to set initial incident ingestion based on the configured date and time.

 You can use this option to define a specific date and time for the initial ingestion. Subsequent ingestions are based on the polling interval period.

</td></tr><tr><td>

Input Initial Incident Ingestion Time

</td><td>

Date and time that you specify for the incident ingestion.

</td></tr><tr><td>

Initial Incident Ingestion Time

</td><td>

The first time when data is ingested.**Note:** The value is visible only if the **Set Initial Incident Ingestion Time** option is selected.

</td></tr><tr><td>

Next Incident Ingestion Time \(estimated\)

</td><td>

The next estimated incident ingestion time.

</td></tr><tr><td>

One-Time Retrieval

</td><td>

Option to enable one-time historical data pull.**Note:** If selected, then historical data will be pulled from Netskope DLP according to the date added in **Since Date**.

</td></tr><tr><td>

Since Date

</td><td>

Date from when data is fetched from Netskope.**Note:** At most the last 30 days of data can be fetched from Netskope.

</td></tr></tbody>
</table>3.  Click **Finish**.

4.  On the pop-up, save the created profile configuration by clicking **Finish**.

5.  Activate the profile.

    1.  Open the created profile.

    2.  Set **Active** to **true**.

    3.  Click **Update**.


## Result

After the successful creation activation of the profile, incidents will be fetched periodically as per the configuration set in the profile. The incidents will be added into the DLP incidents table.

**Parent Topic:**[Create a Profile for Netskope DLP integration](create-profile-netskope-dlp-integration.md)

