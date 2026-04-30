---
title: Load Digital Experience Score​ demo data
description: Load the demo data for Digital Experience Score​ after installing the application.
locale: en-US
release: yokohama
product: Digital Experience Score
classification: digital-experience-score
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Install Digital Experience Score​, Configuring Digital Experience Score​, Digital Experience Score​, Digital End-User Experience, IT Service Management]
---

# Load Digital Experience Score​ demo data

Load the demo data for Digital Experience Score​ after installing the application.

## Before you begin

[Install Digital Experience Score​](install-dex-score.md)

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

**Parent Topic:**[Install Digital Experience Score​](install-dex-score.md)

**Related topics**  


[Delete Digital Experience Score​ demo data](dexscr-delete-demo-data.md)

