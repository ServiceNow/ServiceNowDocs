---
title: Review Event Management similarity examples
description: Review the similarity examples and scores that the system provides during solution training to see how the selected alert record compares to existing alert records. For example, you can modify the similarity score threshold to increase the accuracy of your similarity recommendations.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Alert similarity, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Review Event Management similarity examples

Review the similarity examples and scores that the system provides during solution training to see how the selected alert record compares to existing alert records. For example, you can modify the similarity score threshold to increase the accuracy of your similarity recommendations.

## Before you begin

Train a similarity solution in a ServiceNow datacenter. For more information, see [Create an Event Management similarity solution](create-solution-similarity.md).

Role required: evt\_mgmt\_admin

## About this task

Adjust the current threshold to provide useful results. For example, a low similarity score has more coverage but less precision.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Similarity** &gt; **Solutions**.

2.  In the ML Solutions list, locate your solution and click the Information icon \(![Information icon](../image/info.png)\).

3.  Click **Open Record**.

4.  Click the **Similarity Examples** related link.

    ![Similarity example](../image/similarity-example.png)

5.  Review the similarity examples and their threshold scores to determine the accuracy and coverage levels you want applied to your solution similarity results.

    The higher the similarity score, the more precise it is and the less coverage it offers. The lower the similarity score, the more coverage it has and the less precision it offers.

6.  Based on your review, determine whether to increase or decrease the similarity score threshold value for your similarity solution

    The solution returns only similarity results that have a score that is higher than the threshold. If the current threshold is not providing useful results, adjust the threshold value.

7.  Navigate to **Predictive Intelligence** &gt; **Similarity** &gt; **Solutions**.

8.  In the ML Solutions list, locate your solution and click the Reference icon \(![Reference icon](../image/reference-icon.png)\).

9.  Click **Open Record**.

10. In the Solution Statistics tab, enter a new value in the **Similarity Score Threshold** field.

    For example, suppose that the current score is 80. Based on your similarity example review, you might want to update the field by entering a higher score of 90, which will return fewer results but ones that are more similar to the alert record under review. A lower similarity score has more coverage but less precision.

11. Right-click in the form header and click **Save**.

    Your solution uses the new similarity threshold value. In the example, the solution returns similar results that have a score higher than 90.


**Parent Topic:**[Alert similarity](../concept/alert-similarity.md)

