---
title: Define schedule for the Secureworks CTP Ticket ingestion
description: Verify the default settings for ticket retrieval or modify the scheduling as needed. This step permits you to filter your ticket retrieval based on a date range and a polling interval.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create a profile for Secureworks CTP ticket ingestion integration, Secureworks CTP Ticket Ingestion Integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Define schedule for the Secureworks CTP Ticket ingestion

Verify the default settings for ticket retrieval or modify the scheduling as needed. This step permits you to filter your ticket retrieval based on a date range and a polling interval.

## Before you begin

Role required: sn\_si.admin

## About this task

You also choose how often you will poll for future tickets that match the ticket profile configuration. Configure these polling intervals on a per-profile basis. When scheduling, you may prefer to balance system load against incident urgency. A one-minute default value is set for any profile, but you may prefer to modify this setting based on the urgency of the incident and the anticipated load on your system.

## Procedure

1.  If the Scheduling page on the progress bar is not displayed, select **Scheduling**.

2.  Choose one to schedule how and when tickets are pulled from the Secureworks CTP portal.

<table id="choicetable_phd_qqc_jfb"><thead><tr><th align="left" id="d434848e75">

Option

</th><th align="left" id="d434848e78">

Description

</th></tr></thead><tbody><tr><td id="d434848e84">

**Ongoing ticket ingestion selected**

</td><td>

Based on the default setting, the ServiceNow AI Platform instance pulls from the Secureworks CTP portal for new tickets every five minutes. Security incidents are created if tickets are found and incident generation filtering criteria are matched. To balance ticket ingestion against server load, and to pull the most current data, five minutes is the setting you may prefer. However, this value can be modified as needed.

</td></tr><tr><td id="d434848e102">

**-   Ongoing ticket ingestion selected
-   Set initial ticket ingestion time
**

</td><td>

Initial ingestion timeIf you want to schedule the initial ingestion at a specific time, follow these steps:

-   Select the Ongoing ticket ingestion and Set initial ticket ingestion time fields.
-   Specify the time in the Input initial ticket ingestion time field.
 The initial ingestion will take place at the time specified here. Subsequent ingestions will be based on the schedule defined in the Polling increment \(minutes\) field.

 As an example for scheduling, if you have a daily ticket job that runs once a day at 4 AM local time, you can set up the corresponding ticket profile in your ServiceNow AI Platform instance to run at 4:05 AM local time to capture the ticket right away and create a security incident.

 Enter 04 05 00 in the Initial ticket ingestion field. In the Polling increment \(minutes\) field, enter 1440 \(24 hours\) to schedule the next ticket ingestion for 24 hours from the initial ticket ingestion. Both the initial ticket ingestion time and next ticket ingestion time are displayed in the fields.

 To configure the settings in this example, follow these steps:

-   Select the **Ongoing ticket ingestion** option.
-   In the Polling Increment \(minutes\) field, enter 1440 \(24 hours\).
-   Select the **Set initial ticket ingestion time** option.
-   In the Input initial ticket ingestion time field, enter 04 05 00. The time of the next ticket ingestion is displayed in the Next ticket ingestion time \(estimated\) field.


</td></tr></tbody>
</table>    ![Secureworks CTP: Create Profile: Schedule](../image/secureworks-create-profile-schedule.gif)

3.  Click **Continue** to navigate to the Additional Options page.


