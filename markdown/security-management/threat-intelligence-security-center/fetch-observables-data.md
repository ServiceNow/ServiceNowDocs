---
title: Fetch Observables Data
description: Fetch the observables related records data.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Observables, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Fetch Observables Data

Fetch the observables related records data.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click on **Threat Intel Library** icon on the workspace.

3.  Go to **Observables**.

    The related observables associated with that selected object are displayed.

4.  Select any observable record.

    If the given observables has any CVEs associated with it then you can fetch its vulnerable related data automatically using the button provided, and these associated records are displayed in the Business Context section of the Vulnerabilities.

5.  Go to **Internal Intelligence** &gt; **Vulnerable entries**.

    The associated CVEs records for the observables are displayed.

6.  Select any CVE and click on **Fetch Vulnerability related data** button.

    **Note:**

    -   An information message displays that This specific vulnerability object doesn't have any vulnerable entries associated with it. You must associate the object\(s\) with the vulnerable entries to fetch the data. For more information see, [Fetch Vulnerability Data](fetch-vulnerability-data.md) on how to link the records and perform the scheduled job to fetch the data. and for more information on Scheduled jobs, see [Scheduled jobs](https://servicenow.com/docs/bundle/washingtondc-platform-administration/page/administer/reference-pages/concept/c_ScheduledJobs.html).
    -   This button will trigger a background scheduled job, and the job initiation and execution details are displayed in the Activity Stream section. For example, when the job is triggered the activity stream displays an activity that Started fetching associated data with the vulnerable entries. The background scheduled job will continuously check for any observables that has any vulnerable entry associated with the observable and run automatically and this scheduled job will run every one hour. in case if the records are not fetched then you can manually link the records and fetch the data.

**Parent Topic:**[Observables](../concept/observables.md)

