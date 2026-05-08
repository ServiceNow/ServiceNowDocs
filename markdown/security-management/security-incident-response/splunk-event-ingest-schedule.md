---
title: Schedule and retrieve alerts for the Splunk Enterprise Event Ingestion integration
description: For automated alert ingestion profiles, this step is final step of the event profile configuration. During this step, you can verify the default settings for alert retrieval or modify the scheduling as needed. This step permits you to filter your alert retrieval based on a date range.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Create an event profile, Splunk Enterprise Event Ingestion integration for Security Operations by ServiceNow, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Schedule and retrieve alerts for the Splunk Enterprise Event Ingestion integration

For automated alert ingestion profiles, this step is final step of the event profile configuration. During this step, you can verify the default settings for alert retrieval or modify the scheduling as needed. This step permits you to filter your alert retrieval based on a date range.

## Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## About this task

After you have completed all the steps in the progress bar for the profile configuration as shown in the following figure, you have completed the configuration for profiles for manual event forwarding. There is no scheduling available for events forwarded manually from your Splunk Enterprise console. For profiles for automated alert ingestion, you choose whether you want to ingest any historical alerts during the Scheduling step. You also choose how often you will poll for future alerts that match the alert profile configuration.

![Progress bar.](../image/progress-bar.png "Progress bar")

For automated alert ingestion profiles, before the profile is activated, you verify and modify the scheduling and alert retrieval. This step is the final step of the event profile configuration process for scheduled alert profiles.

Configure these polling intervals on a per-profile basis. The performance of the Splunk event ingestion integration is impacted by the different polling intervals. When scheduling, you may prefer to balance system load against incident urgency. A five-minute default value is set for any profile, but you may prefer to modify this setting based on the urgency of the incident and the anticipated load on your system.

In the Splunk Enterprise console, you set an alert to trigger that is based on increments or on a specific time. Use this setting to help you configure the scheduling in your ServiceNow AI Platform instance so the time increments in your Splunk Enterprise console synchronize with the scheduling that you set up in your ServiceNow AI Platform instance.

## Procedure

1.  If the Scheduling page on the progress bar is not displayed, select **Scheduling**.

2.  Choose one to schedule how and when alerts are pulled from the Splunk Enterprise console.

<table id="choicetable_phd_qqc_jfb"><thead><tr><th align="left" id="d194402e130">

Option

</th><th align="left" id="d194402e133">

Description

</th></tr></thead><tbody><tr><td id="d194402e139">

**-   On-going Alert field selected
-   One-Time Retrieval field cleared
**

</td><td>

On-going AlertBased on the default setting, the ServiceNow AI Platform instance pulls from the Splunk Enterprise server for new alerts every five minutes. Security incidents are created if triggered alerts are found and filtering criteria are matched. To balance alert ingestion against server load, and to pull the most current data, five minutes is the setting you may prefer. However, this value can be modified as needed.

</td></tr><tr><td id="d194402e166">

**-   On-going alert field cleared
-   One-Time Retrieval field selected
**

</td><td>

One-time retrievalUse this configuration if you want a one-time pull to ingest alerts based on historic events.

 When configured, a profile is used once to retrieve triggered alerts including alerts from historical events that are based on a date range. To the right of the **Since date** field, click the calendar icon. In the calendar that is displayed, select the date that you want to start pulling alerts. Starting with the **Since date** value, triggered alerts are retrieved up through the current date.

After the alerts are pulled, this setting will not retrieve triggered alerts for this profile going forward from the current date. This setting populates the security incident with all the alerts that are found for the range you enter.

</td></tr></tbody>
</table>    ![Scheduling page with calendar displayed.](../image/214SplunkProfileSchedulingTab.png)

    As an example for scheduling, if you have a daily Splunk alert that runs once a day at 4 AM local time, you can set up the corresponding alert profile in your ServiceNow AI Platform instance to run at 4:05 AM local time to capture the alert right away and create a security incident. Enter `04 05 00` in the **Initial alert ingestion** field. In the **Increment \(Minutes\)** field, enter `1440` \(24 hours\) to schedule the next alert ingestion for 24 hours from the initial alert ingestion. Both the initial alert ingestion time and next alert ingestion time are displayed in the fields.

3.  To configure the settings for this example, follow these steps.

    1.  With the Scheduling page displayed, select the **Ongoing alert** check box to enable this option.

    2.  In the **Increment \(minutes\)** field, enter `1440` \(24 hours\).

    3.  Click the **Select Initial alert ingestion** check box to enable editing for the Initial alert ingestion and Next alert ingestion fields.

    4.  In the Initial alert ingestion field, enter `04 05 00`.

        In the **The Next alert ingestion \(estimated\)** field, the time of the next alert ingestion is displayed.

4.  Click **Finish** to complete the configuration.

    A confirmation dialog is displayed. You have successfully completed the setup and configuration for the integration. This profile is activated, and it pulls alerts from the Splunk Enterprise console based on your scheduling. There is a limit of 1,000 security incidents that can be created in a 24-hour period. Up to 100 events are per fired alert. Subsequent events will be ignored after the limits are reached.


**Parent Topic:**[Create and name an event profile](splunk-event-ingest-create-profile.md)

