---
title: Activate Event Management solution version
description: The system activates the most recent version of the solution, but you can activate any previously trained Event Management solution version if it is more appropriate.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Alert similarity, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Activate Event Management solution version

The system activates the most recent version of the solution, but you can activate any previously trained Event Management solution version if it is more appropriate.

## Before you begin

Because you might have created more than one solution, you can choose to activate the solution that is most appropriate.

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Similarity** &gt; **Solutions**.

2.  In the ML Solutions list, click the Reference icon \(![Reference icon](../image/info.png)\) for the trained solution that you want to activate.

3.  Click **Open Record**.

    You can assign a title to the solution using the `evt_mgmt_similarity_solution_title` property. The default value is `ml_x_global_alert_similarity`. This property changes the value in the **Solution Name** field.

4.  In the solution record, click **Activate**.

    The system activates this solution version and deactivates any other solution version.


**Parent Topic:**[Alert similarity](../concept/alert-similarity.md)

