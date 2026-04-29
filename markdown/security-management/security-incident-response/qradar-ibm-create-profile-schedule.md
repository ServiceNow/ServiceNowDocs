---
title: Define schedule
description: You can define the schedule for the offense ingestion. During this step, you can verify the default settings for the offense retrieval or modify the scheduling as needed. This step also permits you to retrieve historical offenses using a date range.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Setup IBM QRadar profile, Set up instance, IBM QRadar Offense Ingestion Integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Define schedule

You can define the schedule for the offense ingestion. During this step, you can verify the default settings for the offense retrieval or modify the scheduling as needed. This step also permits you to retrieve historical offenses using a date range.

## Before you begin

Role required: sn\_si.admin

## About this task

You can choose whether you want to ingest any historical offenses during the Scheduling step. You also choose how often you will poll for future new offenses and updated offenses that match the profile configuration.

As a user with the sn\_si.admin role, you configure these polling intervals on a per-profile basis. The performance of the IBM QRadar offense ingestion integration may be impacted by the different polling intervals. When scheduling, you may prefer to balance reducing polling overhead on the IBM QRadar server against a desire to be notified as soon as possible when an offense is created or updated. A five-minute default value is set for any profile, but you may prefer to modify this setting to as low as one minute if required.

**Pulling new and updated offenses**

When the polling schedule is set, the scheduled job pulls both new and updated offenses that were pulled previously but did not meet the incident filtering criteria. This provides you with the flexibility to create incidents based on criteria that may not be present when a offense is first created but becomes available after an update occurs, for example, during the investigation phase. Once an incident is created for a specific offense, its subsequent updates are ignored since it is expected that the offense is now being treated as an active ServiceNow security incident. However, all other offenses that have been previously ingested but failed to meet the incident generation criteria, will continue to be pulled and checked against the incident generation criteria until they become part of an active incident.

## Procedure

1.  If the Scheduling page on the progress bar is not displayed, select **Scheduling**.

2.  Choose one to schedule how and when offenses are pulled from the IBM QRadar console.

<table id="choicetable_phd_qqc_jfb"><thead><tr><th align="left" id="d439412e91">

Option

</th><th align="left" id="d439412e94">

Description

</th></tr></thead><tbody><tr><td id="d439412e100">

**__Ongoing offense ingestion field selected__**

</td><td>

On-going OffenseBased on the default setting, the ServiceNow AI Platform instance pulls from the IBM QRadar server for new and updated offenses every five minutes. Security incidents are created if offenses are found and incident generation filtering criteria are matched. To balance ingestion polling overhead desire to get the most current data, five minutes is the default setting. However, this value can be modified to as low as one minute if needed.

</td></tr><tr><td id="d439412e121">

**-   Ongoing offense ingestion selected
-   Set initial offense ingestion time
**

</td><td>

Initial ingestion timeIf you want to schedule the initial ingestion at a specific time, follow these steps:

-   Select the Ongoing offense ingestion and Set initial offense ingestion time fields.
-   Specify the time in the Input initial offense ingestion time field.
 The initial ingestion will take place at the time specified here. Subsequent ingestions will be based on the schedule defined in the Polling increment \(minutes\) field.

 As an example for scheduling an initial offense ingestion time, if you have a daily IBM QRadar security check that runs once a day at 4 AM local time, you can set up the corresponding offense profile in your ServiceNow AI Platform instance to run at 4:05 AM local time to capture the security failure right away and create a security incident.

 Enter `<date> 04 05 00` in the Initial offense ingestion field. In the Polling increment \(Minutes\) field, enter `<date> 1440` \(24 hours\) to schedule the next offense ingestion for 24 hours from the initial offense ingestion. Both the initial offense ingestion time and next offense ingestion time are displayed in the fields.

 The initial ingestion will take place at 4:05 am. The subsequent ingestions will be based on the polling interval. In this case, since the Polling increment is 24 hours, the next ingestion will take place on the next day at 4:05 am.

</td></tr><tr><td id="d439412e174">

**One Time Retrieval field selected**

</td><td>

One-Time RetrievalUse this configuration if you want a one-time pull to ingest historical offenses.

 When this setting is configured, a profile is used once to retrieve offenses from historical events that are based on a date range. To the right of the Since date field, click the calendar icon. In the calendar that is displayed, select the date that you want to start pulling offenses. Starting with the Since date value, offenses are retrieved up through the current date. Note that you can pull as far back as seven days from the current date. This functionality is not intended to retrieve significant amounts of historical offenses from IBM QRadar for archival reasons but rather a minimal amount of in-flight offenses that are being actively worked at the time of profile activation.

After the offenses are pulled, this setting will not retrieve more offenses for this profile going forward from the current date. This setting populates the security incident with all the offenses that are found for the range you enter.

</td></tr></tbody>
</table>    ![IBM QRadar: Create Profile: Schedule](../image/ibm-qradar-profile-schedule.png)

3.  Click **Continue** to navigate to the Additional Options page.


