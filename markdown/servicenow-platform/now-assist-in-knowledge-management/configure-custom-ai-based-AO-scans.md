---
title: Configure custom AI-based Article Optimization scans
description: The Out-of-Box \(OOB\) Knowledge Center settings provide default configurations for article optimization scans. However, you can customize scans for article optimization.
locale: en-US
release: zurich
product: Now Assist in Knowledge Management
classification: now-assist-in-knowledge-management
topic_type: task
last_updated: "2025-12-04"
reading_time_minutes: 2
breadcrumb: [Configure Now Assist in Knowledge Management, Now Assist in Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure custom AI-based Article Optimization scans

The Out-of-Box \(OOB\) Knowledge Center settings provide default configurations for article optimization scans. However, you can customize scans for article optimization.

## Before you begin

Role required: admin

## About this task

Configure Article Optimization scans for articles in the Knowledge Center. Two types of Article Optimization scans are available in the Knowledge Center. One is a script-based scan and the other is a AI-based scan. If you are subscribed to Now Assist, you can configure and run both the scan types. If you are not subscribed to Now Assist, you can configure only the script-based scans, and Article Optimization runs only the script-based scans.

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Knowledge Center** &gt; **Lists** &gt; **Article Optimization** &gt; **Scans**.

    ![Article Optimization scans definition table.](../image/navigate-to-scan-definition-table.jpeg)

2.  Select **New**.

    1.  If you want to clone and modify an existing scan, go to the **kb\_assist\_scan\_definition** table.

    2.  Open a record and select **Insert and stay** to copy the scan.

    3.  **Rename** the copied scan.

    ![Modify a scan.](../image/Modify-scan.jpeg)

3.  Fill out the record form as follows:

    1.  Set the **Run type** field to:

        -   **On change:** If you want the scan to run each time an article is saved.

            **Note:** the scan must still be associated with a job in order to run but the job schedule will not control when this scan runs.

        -   **Always:**If you want the scan to run based on the schedule set up in the associated job.
    2.  Set the **Execution type** to **Now Assist skill**.

    3.  Select the **Look-up** icon and open the **List filter**.

    4.  Set the condition to **Name** and enter part of your prompt name.

    5.  Select **Run** to view filtered results.

        **Note:** The list can show multiple results if the same prompt name is used in multiple skills or if there are multiple versions of a prompt due to modifications. In this case, select one of the prompts and use **Preview** to make sure that it’s the prompt you want to select \(the **Active** flag is a good indicator\).

4.  Add scripts to the **Process Inputs** and **Process Outputs** fields.

    **Note:**

    -   Using a copy of an existing scan can come in handy as this specific format has to be used for sending data to the Now LLM Service and processing the results.
    -   The last part of the **Process Outputs** script is used to define the finding record and what appears on the **Article Optimization** cards in the editor UI.
5.  **Save** the record.


## Result

The Article Optimization scan is custom configured.

## What to do next

To run the scan, you must add the configured scan to a job. For more information see, [Configuring Article Optimization jobs](configuring-article-optimization-jobs.md).

**Parent Topic:**[Configuring Now Assist in Knowledge Management](../../knowledge-management/concept/configuring-now-assist-km.md)

**Related topics**  


[Configuring custom script based Article Optimization scans](configure-custom-script-based-AO-scan.md)

[Configuring Article Optimization skill and prompts](configure-kc-AO-skill.md)

[Activate Article Optimization skill](activate-kc-AO-skill.md)

