---
title: Load Digital Experience Score​ demo data
description: Load the demo data for Digital Experience Score​ after installing the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/dexscr-load-demo-data.html
release: brazil
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configuring DEX Score, Configure, Digital End-User Experience, IT Service Management]
---

# Load Digital Experience Score​ demo data

Load the demo data for Digital Experience Score​ after installing the application.

## Before you begin

Role required: admin

## About this task

Besides loading demo data, the **CreateDemoDataForDEXScoreJob** scheduled job does the following:

-   Creates demo data for agents
-   Creates DEX score records
-   Inserts data for the last 90 days into the respective tables for the following information:
    -   Application and device health
    -   Surveys
    -   Service level agreements

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Find and open the **CreateDemoDataForDEXScoreJob** scheduled job.

3.  Select **Execute Now**.

    The job runs in the background and takes a few minutes to complete.


## Result

After the scheduled job runs successfully, the demo data is loaded into the instance.

