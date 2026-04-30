---
title: Update dashboard overview
description: When you activate the problem state model, you need to update the overview dashboard to use the new states.
locale: en-US
release: yokohama
product: Problem Management
classification: problem-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Activities to clean up after migration, Migration Utility, Configuring Problem Management, Problem Management, IT Service Management]
---

# Update dashboard overview

When you activate the problem state model, you need to update the overview dashboard to use the new states.

## Before you begin

Role required: admin

## About this task

In the problem overview dashboard, refer to the closed problems by setting Active = false instead of state = 4.

**Note:** If you have added your own custom dashboards or charts, you may need to manually update them as you have migrated to the problem state model.

## Procedure

1.  If you are prompted with the message `To edit this record click here`, then click **here**.

2.  Click the configuration icon \(![Configuration icon](../image/configuration-icon.png)\).

3.  Hover your mouse on **Problems Closed per Week** chart to view and select the Edit Content menu.

4.  Select the filter to open the condition builder and update the condition from **Problem state** is **4** to **Active** is **false**.

5.  Click **Run**.

6.  Click **Save**.

7.  Click **Back** to return to the dashboard.


