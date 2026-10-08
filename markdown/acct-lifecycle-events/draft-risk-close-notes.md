---
title: Draft close notes for a risk signal using ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\)
description: Automatically generate closure notes and close eligible risk signals at the end of each day based on the status of their associated risk solutions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/draft-risk-close-notes.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Associate risk signals, Risk portfolio dashboard, Dashboards, Customer success, Use, Customer Success Management]
---

# Draft close notes for a risk signal using ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\)

Automatically generate closure notes and close eligible risk signals at the end of each day based on the status of their associated risk solutions.

## Before you begin

Role required: `sn_acct_lc.customer_success_agent`

## About this task

A scheduled job runs every day and automatically drafts closure notes for all risk signals eligible to be closed that meet the following criteria:

-   All associated risk solutions are in a closed or inactive state.
-   No new risk occurrences have been created after the last runtime of the scheduled job.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **AI Skills**.

2.  Select **Activate** in the **Draft close notes** card.

3.  Select the user role that can use this skill and select **Save** to activate the skill.

    The daily scheduled job identifies all eligible risk signals, reviews the activity data from associated risk solutions, and generates closure notes. The Closure notes and State fields are updated on the risk signal record and visible in the Activity stream.

4.  To use additional fields or tables when generating closure notes, add an activity context using the Customer Central guided setup.

    Navigate to **All** &gt; **Customer Central** &gt; **Activity Contexts**, select **Risk signal**, create an activity context group, and map it to the additional table you want to use. See [Configure activity groups for the Customer History view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/configure-activity-groups-ca.md) for details.


**Parent Topic:**[Associate risk signals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-risk_signal_solution.md)

