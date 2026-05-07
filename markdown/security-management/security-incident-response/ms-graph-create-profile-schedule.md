---
title: Define schedule for Microsoft Graph Security API integration
description: Verify the default settings for alert retrieval or modify the scheduling as needed. This step permits you to filter your alert retrieval based on a date range.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create a profile, Microsoft Graph Security API alert ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Define schedule for Microsoft Graph Security API integration

Verify the default settings for alert retrieval or modify the scheduling as needed. This step permits you to filter your alert retrieval based on a date range.

## Before you begin

Role required: sn\_si.admin

## About this task

You also choose how often you will poll for future alerts that match the alert profile configuration. For automated alert ingestion profiles, before the profile is activated, you verify and modify the scheduling and alert retrieval. This step is needed for scheduled alert profiles.

As a user with the sn\_si.admin role, you configure these polling intervals on a per-profile basis. The performance of the Microsoft Graph Security API alert ingestion integration is impacted by the different polling intervals. When scheduling, you may prefer to balance system load against incident urgency. A five-minute default value is set for any profile, but you may prefer to modify this setting based on the urgency of the incident and the anticipated load on your system.

## Procedure

1.  If the Scheduling page on the progress bar is not displayed, select **Scheduling**.

2.  Choose one to schedule how and when alerts are pulled from the Microsoft Azure tenant.

<table id="choicetable_phd_qqc_jfb"><thead><tr><th align="left" id="d292245e84">

Option

</th><th align="left" id="d292245e87">

Description

</th></tr></thead><tbody><tr><td id="d292245e93">

**__Ongoing Alert Ingestion selected__**

</td><td>

Based on the default setting, the ServiceNow AI Platform instance pulls from the Microsoft Azure tenant for new alerts every five minutes. Security incidents are created if triggered alerts are found and incident generation filtering criteria are matched. To balance alert ingestion against server load, and to pull the most current data, five minutes is the setting you may prefer. However, this value can be modified as needed.

</td></tr><tr><td id="d292245e111">

**-   Ongoing Alert Ingestion selected
-   Set initial alert ingestion time
**

</td><td>

Initial ingestion timeIf you want to schedule the initial ingestion at a specific time, follow these steps:

-   Select the Ongoing Alert Ingestion and Set initial alert ingestion time fields.
-   Specify the time in the Input initial alert ingestion time field.
 The initial ingestion will take place at the time specified here. Subsequent ingestions will be based on the schedule defined in the Polling increment \(minutes\) field.

 As an example for scheduling, if you have a daily alert job that runs once a day at 4 AM local time, you can set up the corresponding alert profile in your ServiceNow AI Platform instance to run at 4:05 AM local time to capture the alert right away and create a security incident.

 Enter 04 05 00 in the Initial alert ingestion field. In the Increment \(Minutes\) field, enter 1440 \(24 hours\) to schedule the next alert ingestion for 24 hours from the initial alert ingestion. Both the initial alert ingestion time and next alert ingestion time are displayed in the fields.

 To configure the settings in this example, follow these steps:

-   Select the **Ongoing Alert Ingestion** option.
-   In the Polling Increment \(minutes\) field, enter 1440 \(24 hours\).
-   Click the **Set Initial alert ingestion time** option to enable editing for the Initial alert ingestion time and Next alert ingestion \(estimated\) time fields.
-   In the Initial alert ingestion time field, enter 04 05 00. In the Next alert ingestion \(estimated\) time field, the time of the next alert ingestion is displayed.


</td></tr><tr><td id="d292245e175">

**__One Time Retrieval field selected__**

</td><td>

One-Time RetrievalUse this configuration if you want a one-time pull to ingest historical alerts.

 When this setting is configured, a profile is used once to retrieve alerts from historical events that are based on a date range. To the right of the Since date field, click the calendar icon. In the calendar that is displayed, select the date that you want to start pulling alerts. Starting with the Since date value, alerts are retrieved up through the current date. Note that you can pull as far back as seven days from the current date. This functionality is not intended to retrieve significant amounts of historical alerts but rather a minimal amount of in-flight alerts that are being actively worked at the time of profile activation.

After the alerts are pulled, this setting will not retrieve more alerts for this profile going forward from the current date. This setting populates the security incident with all the alerts that are found for the range you enter.

</td></tr></tbody>
</table>3.  Click **Continue** to navigate to the Additional Options page.


