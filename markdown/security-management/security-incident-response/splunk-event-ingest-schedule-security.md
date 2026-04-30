---
title: Schedule and retrieve notable events
description: For automated notable event ingestion profiles, this step is required in the event profile configuration. During this step, you can verify the default settings for notable event retrieval or modify the scheduling as needed. This step also permits you to retrieve historical notable events using a date range.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Set up a profile for scheduled notable event ingestion, Create an event profile, Splunk Enterprise Security event ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Schedule and retrieve notable events

For automated notable event ingestion profiles, this step is required in the event profile configuration. During this step, you can verify the default settings for notable event retrieval or modify the scheduling as needed. This step also permits you to retrieve historical notable events using a date range.

## Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## About this task

For profiles for automated notable event ingestion, you choose whether you want to ingest any historical notable events during the Scheduling step. You also choose how often you will poll for future new notable events and updated notable events that match the alert profile configuration.

For automated notable event ingestion profiles, before the profile is activated, you verify and modify the scheduling and alert retrieval. This is a required step for all event profile configuration process for scheduled alert profiles.

You configure these polling intervals on a per-profile basis. The performance of the Splunk event ingestion integration may be impacted by the different polling intervals. When scheduling, you may prefer to balance reducing polling overhead on the Splunk Enterprise Security server against a desire to be notified as soon as possible when a notable event is created or updated. A five-minute default value is set for any profile, but you may prefer to modify this setting to as low as one minute if required.

Pulling new and updated notable events

When the polling schedule is set, the scheduled job pulls both new and updated notable events that were pulled previously but did not meet the incident filtering criteria. This provides you with the flexibility to create incidents based on criteria that may not be present when a notable event is first created but becomes available after an update occurs, for example, during the investigation phase. Once an incident is created for a specific notable event, its subsequent updates are ignored since it is expected that the notable is now being treated as an active ServiceNow® security incident. However, all other notables that have been previously ingested but failed to meet the incident generation criteria, will continue to be pulled and checked against the incident generation criteria until they become part of an active incident.

## Procedure

1.  If the Scheduling page on the progress bar is not displayed, select **Scheduling**.

2.  Choose one to schedule how and when notable events are pulled from the Splunk Enterprise Security console.

<table id="choicetable_phd_qqc_jfb"><thead><tr><th align="left" id="d471802e107">

Option

</th><th align="left" id="d471802e110">

Description

</th></tr></thead><tbody><tr><td id="d471802e116">

**-   On-going Event Ingestion field selected
-   One-Time Retrieval field cleared
**

</td><td>

On-going EventBased on the default setting, the ServiceNow AI Platform instance pulls from the Splunk Enterprise Security server for new and updated notable events every five minutes. Security incidents are created if notable events are found and incident generation filtering criteria are matched. To balance ingestion polling overhead desire to get the most current data, five minutes is the default setting. However, this value can be modified to as low as one minute if needed.

</td></tr><tr><td id="d471802e143">

**-   On-going Notable Event field cleared
-   One-Time Retrieval field selected
**

</td><td>

One-Time RetrievalUse this configuration if you want a one-time pull to ingest historical notable events.

 When this setting configured, a profile is used once to retrieve notable events from historical events that are based on a date range. To the right of the Since date field, click the calendar icon. In the calendar that is displayed, select the date that you want to start pulling alerts. Starting with the Since date value, notable events are retrieved up through the current date. Note that you can pull as far back as seven days from the current date. This functionality is not intended to retrieve significant amounts of historical events from Splunk Enterprise Security for archival reasons but rather a minimal amount of in-flight events that are being actively worked at the time of profile activation.

After the notable events are pulled, this setting will not retrieve more notable events for this profile going forward from the current date. This setting populates the security incident with all the notable events that are found for the range you enter.

</td></tr></tbody>
</table>    ![Scheduling page with calendar displayed.](../image/splunk_es_scheduling_security.png)

    As an example for scheduling an initial notable event ingestion time, if you have a daily Splunk security check that runs once a day at 4 AM local time, you can set up the corresponding notable event profile in your ServiceNow AI Platform instance to run at 4:05 AM local time to capture the security failure event right away and create a security incident. Enter `04 05 00` in the Initial event ingestion field. In the Increment \(Minutes\) field, enter `1440` \(24 hours\) to schedule the next event ingestion for 24 hours from the initial event ingestion. Both the initial event ingestion time and next event ingestion time are displayed in the fields.

3.  To configure the settings for this example, follow these steps.

    1.  With the Scheduling page displayed, select the **Ongoing event ingestion** check box to enable this option.

    2.  In the Increment \(minutes\) field, enter `1440` \(24 hours\).

    3.  Click the **Select Initial event ingestion** check box to enable editing for the Initial event ingestion and Next event ingestion fields.

    4.  In the Initial event ingestion field, enter `04 05 00`.

        In the The Next event ingestion \(estimated\) field, the time of the next event ingestion is displayed.

4.  Click one of the following to continue with the profile configuration.

    |Option|Description|
    |------|-----------|
    |**Continue**|The Additional Options form is displayed. **Additional Options** is selected on the progress bar. The next step is to update the notable events when the SIR incident is created and/or closed.|
    |**Update**|Your data is saved and the Splunk Event Security Profiles list is displayed.|
    |**Previous**|The Scheduling form is displayed.|
    |**Delete**|Delete this event profile and the Splunk Enterprise Security Event Profiles list is displayed.|


