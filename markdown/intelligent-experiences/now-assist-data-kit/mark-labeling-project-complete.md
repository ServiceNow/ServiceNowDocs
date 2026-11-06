---
title: Mark a labeling project complete
description: Mark a labeling project complete to save its ground truth values in a new dataset and data collection that you can use for evaluation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/now-assist-data-kit/mark-labeling-project-complete.html
release: australia
product: Now Assist Data Kit
classification: now-assist-data-kit
topic_type: task
last_updated: "2026-10-16"
reading_time_minutes: 1
keywords: [ground truth, labeling project, Now Assist Data Kit]
breadcrumb: [Add a ground truth to each dataset record, Using AI Data Kit, AI Data Kit, Managing data for AI, Enable AI Experiences]
---

# Mark a labeling project complete

Mark a labeling project complete to save its ground truth values in a new dataset and data collection that you can use for evaluation.

## Before you begin

Role required: sn\_data\_kit.admin

## About this task

When you mark a project complete, every task is published, including tasks that labelers haven't finished. The results are added to a new dataset and a new data collection, and the collection is published so that it's ready for evaluation. After you mark a project complete, you can't change it.

**Important:**

Mark the project complete only after labelers finish their tasks. Unfinished tasks are added to the new data collection without ground truth values.

## Procedure

1.  Navigate to **All** &gt; **AI Data Kit** &gt; **Home**.

2.  In the Data labeling section, on the **Projects** tab, select the project.

3.  Check the task counts to confirm that labeling is finished.

    The **Published tasks** count shows how many tasks labelers have submitted.

4.  Select **Mark complete**.

5.  In the Mark project as complete dialog box, enter a **Dataset name** and a **Data collection name**.

    Optionally, enter a **Description**.

6.  Select **Mark as complete**.

    The project's tasks are closed. The new dataset appears on the **Datasets** tab, and the new data collection appears on the **Data collections** tab. Refresh the list if the dataset doesn't show as Published yet.


## Result

The new dataset contains the record columns and a column for each component in the project layout, including the ground truth.

## What to do next

To evaluate a skill with the ground truth, select the new data collection in AI Skill Kit.

