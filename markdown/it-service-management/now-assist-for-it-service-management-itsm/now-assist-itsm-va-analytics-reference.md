---
title: ITSM Virtual Agent Analytics reference
description: As an admin, you can refer to the indicators, schedule jobs, and scripts used in the ITSM Virtual Agent analytics.
locale: en-US
release: zurich
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: reference
last_updated: "2026-02-12"
reading_time_minutes: 1
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [Use ITSM Virtual Agent analytics dashboard, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# ITSM Virtual Agent Analytics reference

As an admin, you can refer to the indicators, schedule jobs, and scripts used in the ITSM Virtual Agent analytics.

## ITSM Virtual Agent indicators

<table id="table_hh1_cjc_g3c"><thead><tr><th>

Indicator

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Total chats count by unique users

</td><td>

Display total chat counts segmented by the following dimensions.-   By department
-   Assigned to
-   Incident caller company \(for e.g. when the caller company is an MSP\); Opened by Company
-   Opened by
-   Location
-   Aggregate by
    -   Unique users
    -   Maximum users

</td></tr><tr><td>

Interactions closed by all users

</td><td>

Display interactions closed by all users segmented by the following dimensions.-   By department
-   Assigned to
-   Incident caller company \(for example, when the caller company is an MSP\); Opened by Company
-   Opened by
-   Location
    -   Channels
    -   Handled by
-   Aggregate by
    -   Unique users
    -   Maximum users

</td></tr><tr><td>

Interactions closed by all users

</td><td>

Show interactions closed by all users with segmentations and aggregates.

</td></tr><tr><td>

Interactions closed by virtual agent

</td><td>

Display interactions closed by the ITSM virtual agent.-   By department
-   Assigned to
-   Incident caller company \(for e.g. when the caller company is an MSP\); Opened by Company
-   Opened by
-   Location

</td></tr><tr><td>

Ratio of chats closed by the virtual agent

</td><td>

This is calculated as \(interactions closed by VA / interactions closed by all users\) \* 100.

</td></tr><tr><td>

Interactions closed by virtual agent segmented by multiple dimensions

</td><td>

Evaluate virtual agent effectiveness by analyzing interactions closed by the virtual agent segmented by department, assigned to, incident caller company \(opened\_by\_company\), opened by, and location.

</td></tr><tr><td>

Aggregating user feedback

</td><td>

Use thumbs up/thumbs down on conversations.

</td></tr></tbody>
</table>## ITSM Virtual Agent data collection jobs

Run scheduled jobs to retrieve data.

To access the jobs, navigate to **All** &gt; **System Definition** &gt; **Scheduled jobs**.

-   The **\[Historical\] - ITSM Conversational Analytics** scheduled job runs on-demand. Run this job to retrieve historical data for the last six months.
-   The **\[Daily\] - ITSM Conversational Analytics** scheduled job retrieves daily data. This job automatically runs at midnight everyday.

## ITSM Virtual Agent analytics GAF clustering

To configure the Group Action Framework \(GAF\) to cluster topics and use chat summarization to create topic names, run the **Activate topic clustering for Now Assist ITSM dashboard** script. [Configure Group Action Framework](https://www.servicenow.com/docs/access?context=configure-gaf&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)![Now Assist for ITSM scheduled script execution](../image/now-assist-itsm-script-execution-va-dashboard.png)

