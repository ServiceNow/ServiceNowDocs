---
title: Create a schedule for ArcSight ESM event ingestion ingestion
description: You can define the polling or pull schedule for new correlated events. During this step, you can verify the existing settings for correlation event retrieval or modify the scheduling as needed. This step also permits you to retrieve historical correlation events using a date range.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, Set up instance, ArcSight ESM Event Ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a schedule for ArcSight ESM event ingestion ingestion

You can define the polling or pull schedule for new correlated events. During this step, you can verify the existing settings for correlation event retrieval or modify the scheduling as needed. This step also permits you to retrieve historical correlation events using a date range.

## Before you begin

Role required: sn\_si.admin.

## About this task

You can choose whether you want to ingest any historical correlation events during the Scheduling step. You also choose how often you will poll for future new correlation events that match the profile configuration.

As a user with the sn\_si.admin role, you configure these polling intervals on a per-profile basis. The performance of the ArcSight ESM correlation event ingestion integration may be impacted by the different polling intervals. When scheduling, you may prefer to balance reducing polling overhead on the ArcSight ESM server against a desire to be notified as soon as possible when an event is created or updated. A five-minute default value is set for any profile, but you may prefer to modify this setting to as low as one minute if required.

**Pulling new and updated correlation events**

## Procedure

1.  If the Scheduling page on the progress bar is not displayed, select **Scheduling**.

2.  Choose one to schedule how and when correlation events are pulled from the &lt;ArcSight&gt; console.

<table id="choicetable_phd_qqc_jfb"><thead><tr><th align="left" id="d183747e97">

Option

</th><th align="left" id="d183747e100">

Description

</th></tr></thead><tbody><tr><td id="d183747e106">

**-   Ongoing Event Ingestion field selected
-   One-Time Retrieval field cleared
**

</td><td>

On-going EventBased on the default setting, the ServiceNow AI Platform instance pulls from the ArcSight ESM server for new correlation events every five minutes. Security incidents are created if correlation events are found and incident generation filtering criteria are matched. To balance ingestion polling overhead desire to get the most current data, five minutes is the default setting. However, this value can be modified to as low as one minute if needed.

</td></tr><tr><td id="d183747e133">

**-   Ongoing Event Ingestion field cleared
-   One-Time Retrieval field selected
**

</td><td>

One-Time RetrievalUse this configuration if you want a one-time pull to ingest historical correlation events.

 When this setting is configured, a profile is used once to retrieve correlation events from historical events that are based on a date range. To the right of the Since date field, click the calendar icon. In the calendar that is displayed, select the date that you want to start pulling alerts. Starting with the Since date value, correlation events are retrieved up through the current date.

 Note that you can retrieve events as far back as seven days from the current date. This functionality is not intended to retrieve significant amounts of historical events for archival reasons but rather a minimal amount of in-flight events that are being actively worked at the time of profile activation.

After the correlation events are pulled, this setting will not retrieve more correlation events for this profile going forward from the current date. This setting populates the security incident with all the correlation events that are found for the range you enter.

</td></tr></tbody>
</table>    ![ArcSight ESM: Create Profile: Schedule](../image/sir-arcsight-esm-profile-schedule.png)

    As an example for scheduling an initial correlation event ingestion time, if you have a daily ArcSight ESM security check that runs once a day at 4 AM local time, you can set up the corresponding correlation event profile in your ServiceNow AI Platform instance to run at 4:05 AM local time to capture the security failure event right away and create a security incident. Enter `04 05 00` in the Initial event ingestion field. In the Increment \(Minutes\) field, enter `1440` \(24 hours\) to schedule the next event ingestion for 24 hours from the initial event ingestion. Both the initial event ingestion time and next event ingestion time are displayed in the fields.

3.  To configure the settings for this example, follow these steps.

    1.  With the Scheduling page displayed, select the **Ongoing event ingestion** check box to enable this option.

    2.  In the Increment \(Minutes\) field, enter `1440` \(24 hours\).

    3.  Click the **Set initial correlated event ingestion time** check box to enable editing for the Initial event ingestion and Next event ingestion fields.

    4.  In the Initial event ingestion time field, enter `04 05 00`.

        In the Next event ingestion time \(estimated\) field, the time of the next event ingestion is displayed.

4.  Click **Continue** to navigate to the Additional Options page.

    **Note:** The default number of security incidents that can be created and aggregated in a day, and the flow time period are defined in the ArcSight ESM Integration Settings. You can modify these settings if required. See [ArcSight ESM Integration Settings for event ingestion integration](../concept/arcsight-esm-settings.md) for details.


