---
title: Draft close notes for a risk signal using Now Assist for Telecommunications, Media and Technology \(TMT\)
description: Automatically generate closure notes and close eligible risk signals at the end of each day based on the status of their associated risk solutions.
locale: en-US
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use generative AI skills, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Draft close notes for a risk signal using Now Assist for Telecommunications, Media and Technology \(TMT\)

Automatically generate closure notes and close eligible risk signals at the end of each day based on the status of their associated risk solutions.

## Before you begin

Role required: sn\_acct\_lc.customer\_success\_agent

## About this task

A scheduled job runs everyday and automatically drafts closure notes for all risk signals eligible to be closed that meet the following criteria:

-   All associated risk solutions are in a closed or inactive state.
-   No new risk occurrences have been created after the last runtime of the scheduled job.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Now Assist Skills**.

2.  Select **Activate** in the **Draft close notes** card.

3.  Select the user role that can use this skill and select **Save** to activate the skill.

    The daily scheduled job identifies all eligible risk signals, reviews the activity data for each eligible risk signal from the associated risk solutions and generates closure notes. The Closure notes and the State are updated on the risk signal record and are visible in the Activity stream.

    ![Closure notes](../image/draft-risk-close-notes.jpg)

    The activity contexts used to generate the closure notes are predefined and available with the base system. If you want to use additional fields or tables when generating closure notes, you must add additional activity contexts using the Customer Central guided setup. Navigate to **All** &gt; **Customer Central** &gt; **Activity Contexts** and select **Risk signal**, create an activity context group and map it to the additional table you want to use.

    ![Activity context group](../image/activity-context.jpg)

    For more details on creating the activity context group, see [Configure activity groups for the Customer History view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-activity-groups-ca.md).


**Parent Topic:**[Using Now Assist for Telecommunications, Media and Technology \(TMT\)](../concept/now-assist-spm-using.md)

