---
title: Activate a tracking profile
description: Activate one of the out-of-the-box tracking profiles to start collecting portal and campaign metrics.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Content Analytics, Setup continuous improvement features, Configure, Employee Center, Employee Service Management]
---

# Activate a tracking profile

Activate one of the out-of-the-box tracking profiles to start collecting portal and campaign metrics.

## Before you begin

Role required: sn\_cda.analytics\_admin

## About this task

Content Analytics contains two out-of-the-box profiles \(Content Experiences and Content Publishing\) that track metrics for the demo portal associated with the product.

You can use either tracking profile to track metrics for the Employee Center by setting it as the default profile.

## Procedure

1.  Navigate to **All** &gt; **Content Analytics** &gt; **Setup**.

2.  Activate one of the profiles: Double-click in the **Active** column, select **True**, then click the **Save** icon.

3.  Set a default profile: Double-click in the **Default** column, select **True**, then click the **Save** icon.

    **Note:** The two profiles act as repositories for data collection. The different repository of data provides options to display data sets separately in the analytics dashboard.


## Result

The out-of-the-box tracking profiles each have a scheduled job to collect data. You can modify or manually execute the script associated with the scheduled job by doing these steps:

1.  Click the link in the Trigger column.

    **Note:** If the Trigger column doesn't appear in the Tracking profiles list, click the **Update Personalized List** icon and add the Trigger column to the selected list.

    The Profile trigger form opens, where you can modify the import run time \(how often the script runs\) or set a condition.

2.  To manually execute the script, click **Execute Now**.

