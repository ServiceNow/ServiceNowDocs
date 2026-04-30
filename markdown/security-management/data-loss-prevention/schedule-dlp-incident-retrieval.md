---
title: Schedule the Symantec DLP Incident Retrieval
description: Set a schedule to retrieve the incident data and ingest Symantec DLP incidents that match the criteria in the profile. Configure the schedule to define how and when you pull incidents from Symantec.
locale: en-US
release: yokohama
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create a profile for Symantec DLP integration, Symantec Integration for Data Loss Prevention Incident Response, DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Schedule the Symantec DLP Incident Retrieval

Set a schedule to retrieve the incident data and ingest Symantec DLP incidents that match the criteria in the profile. Configure the schedule to define how and when you pull incidents from Symantec.

## Before you begin

Role required: sn\_dlir.admin

## About this task

You can plan how often you will poll for future incidents that match the incident profile configuration. To enable automated incident ingestion, you must configure the scheduling and incident retrieval before you activate the profile. The profile can be configured to do one-time retrieval using the **One-Time Retrieval** check box. The historical date can be up to the last three months from the current date.

The polling interval is configured for each profile individually. The different polling intervals may impact the performance of the Symantec DLP incident integration. When scheduling, plan to balance the system load against the urgency of an incident.

## Procedure

1.  Set a schedule to retrieve data and ingest incidents that match the criteria in the profile.

2.  On the form, fill the fields.

<table id="table_jyk_kcz_2tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Ongoing Incident Ingestion

</td><td>

The ongoing incident ingestion that the ServiceNow AI Platform instance pulls from the  Symantec for new incidents. DLP incidents are created if triggered incidents are found and the incident generation filtering criteria matches.

</td></tr><tr><td>

Polling increment \(minutes\)

</td><td>

The polling frequency that is defined in minutes. This field is automatically set to 300 minutes.

</td></tr><tr><td>

Set Initial Incident Ingestion Time

</td><td>

Option to define a date and time for the initial ingestion. Subsequent ingestions are based on the polling interval period.

</td></tr><tr><td>

Input Initial Incident Ingestion Time

</td><td>

Date and time that you specify for the incident ingestion.

</td></tr><tr><td>

Initial Incident Ingestion Time

</td><td>

First time when the data is ingested.You can see the that values start showing up when the initial incident ingestion time is set.

</td></tr><tr><td>

Next Incident Ingestion Time \(estimated\)

</td><td>

Next period for an estimated incident ingestion.

</td></tr><tr><td>

One-Time Retrieval

</td><td>

Option to enable one-time historical data pull.If this field is selected, then historical data will be pulled from Symantec DLP according to the date added in the **Since Date** field.

</td></tr><tr><td>

Since Date

</td><td>

Date from when data is supposed to be retrieved from Symantec. This field can be set to at most three months.

</td></tr></tbody>
</table>    ![Schedule the Symantec Data Loss Prevention Incident Retrieval.](../../data-loss-prevention/image/dlp-symantec-scheduling.gif)

3.  To save the created profile configuration, click **Finish** on the pop-up window.

4.  To activate the profile, open the created profile.

5.  Enable **Active** option.

6.  Click **Update**.


## Result

After successful creation and activation of the profile, the incidents are retrieved periodically as per the configuration set in the profile and added into DLP incidents table.

**Parent Topic:**[Create a profile for Symantec DLP integration](create-profile-symantec-dlp.md)

