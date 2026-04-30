---
title: Configuring custom script based Article Optimization scans
description: The Out-of-Box \(OOB\) Knowledge Center settings provide default configurations for article optimization scans. However, users can configure new scans for article optimization.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-11-21"
reading_time_minutes: 2
breadcrumb: [Configuring Knowledge Center, Knowledge Center, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configuring custom script based Article Optimization scans

The Out-of-Box \(OOB\) Knowledge Center settings provide default configurations for article optimization scans. However, users can configure new scans for article optimization.

## Before you begin

Role required: admin

## About this task

Configure Article Optimization scans for articles in the Knowledge Center. Two types of Article Optimization scans are available in the Knowledge Center. One is a script-based scan and the other is a AI-based scan. If you are subscribed to Now Assist, you can configure both the scan types. If you are not subscribed to Now Assist, you can configure only the script-based scans, and Article Optimization runs only the script-based scans.

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Knowledge Center** &gt; **Lists** &gt; **Article Optimization** &gt; **Scans**.

    ![Article Optimization scans definition table.](../image/navigate-to-scan-definition-table.jpeg)

2.  Select **New**.

    1.  If you want to clone and modify an existing scan, go to the **kb\_assist\_scan\_definition** table.

    2.  Open a record and select **Insert and stay** to copy the scan.

    3.  **Rename** the copied scan.

3.  Fill out the record form as follows:

    1.  Set the **Run type** field to:

        -   **On change:** If you want the scan to run each time an article is saved.

            **Note:** the scan must still be associated with a job in order to run but the job schedule will not control when this scan runs.

        -   **Always:**If you want the scan to run based on the schedule set up in the associated job.
    2.  Set the **Execution type** to **Script Based**.

4.  Type the script code in the **Script** field.

    **Note:** Using a copy of an existing scan can come in handy as this specific format has to be used for processing the results.

5.  **Save** the record.


## Result

The Article Optimization scan is custom configured.

## What to do next

To run the scan, you must add the configured scan to a job. For more information see, [Configuring Article Optimization jobs](configuring-article-optimization-jobs.md)

**Related topics**  


[Configure custom AI-based Article Optimization scans](configure-custom-ai-based-AO-scans.md)

[Configuring Article Optimization skill and prompts](configure-kc-AO-skill.md)

[Activate Article Optimization skill](activate-kc-AO-skill.md)

