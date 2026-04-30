---
title: Train the clustering solution definition to automatically group similar cases into topics
description: To enable clustering of similar cases into topics, you must first update and train the clustering solution definition.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure trending case topics, Trending case topics, Machine learning solutions, Implement Intelligence, Configure, Customer Service Management]
---

# Train the clustering solution definition to automatically group similar cases into topics

To enable clustering of similar cases into topics, you must first update and train the clustering solution definition.

## Before you begin

Role required: admin

Activate the Predictive Intelligence for Customer Service Management plugin \(com.snc.csm\_ml\).

## About this task

By default, a clustering solution definition for clustering groups of cases into topics is already available. A clustering solution definition groups similar records into clusters so you can address them collectively or identify patterns.

You can modify the fields, filters, update frequency, and training frequency.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Clustering** &gt; **Solution Definitions**.

2.  In the Clustering Definitions list, search for and select the Grouping of Cases into Topics solution definition \(ml\_sn\_sn\_csm\_ml\_global\_grouping\_of\_cases\_into\_topics\).

3.  On the Clustering Definition form, verify the default field values.

4.  Change the fields and filters, as required.

5.  To change the frequency with which the model for clustering solution definition must be rebuilt, edit the **Update Frequency** field.

6.  To change the frequency with which to include new records in the model for the clustering solution definition, edit the **Training Frequency** field.

7.  In the Training Request Schedule related list, view the schedule for training the Grouping of Cases into Topics solution definition.

8.  Click **Update &amp; Retrain**.

9.  Open the Grouping of Cases into Topics solution definition.

10. In the ML Solutions related list, view the training solution progress in the **Progress** column.

    **Note:** Alternatively, you can click the link for the solution in the **Active** column. On the ML Solution form, click the **Show training progress** related link to check the training solution progress.

11. Click the **Cluster Visualization** tab.

    The clusters that were formed for the given solution are displayed in a tree map in descending order of size from top left to bottom right. Each node is colored from red to green depending on the cluster quality.


