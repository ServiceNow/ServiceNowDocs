---
title: Train the similarity solution definition to find similar existing major cases
description: To enable finding related major cases in a cluster, you must first update and train the similarity solution definition.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure trending case topics, Trending case topics, Machine learning solutions, Implement Intelligence, Configure, Customer Service Management]
---

# Train the similarity solution definition to find similar existing major cases

To enable finding related major cases in a cluster, you must first update and train the similarity solution definition.

## Before you begin

Role required: admin

Activate the Predictive Intelligence for Customer Service Management plugin \(com.snc.csm\_ml\).

## About this task

By default, a similarity solution definition for finding similar existing major cases in a cluster is already available. A similarity solution definition collects and compares your existing records to new similar records.

You can modify the fields, filters, update frequency, and training frequency.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Similarity** &gt; **Solution Definitions**.

2.  In the Similarity Definitions list, search for and select the Major Issue Detector solution definition \(ml\_sn\_global\_major\_issue\_detector\).

3.  On the Similarity Definition form, verify the default field values.

    For more information about the Similarity Definition form fields, see [Create and train a similarity solution](https://www.servicenow.com/docs/access?context=create-similarity-solution&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

4.  Change the fields and filters, as required.

5.  To change the frequency with which the model for similarity solution definition must be rebuilt, edit the **Update Frequency** field.

6.  To change the frequency with which to include new records in the model for the similarity solution definition, edit the **Training Frequency** field.

7.  In the Training Request Schedule related list, view the schedule for training the Major Issue Detector solution definition.

8.  Click **Update &amp; Retrain**.

9.  Open the Major Issue Detector solution definition.

10. In the ML Solutions related list, view the training solution progress in the **Progress** column.

    **Note:** Alternatively, you can click the link for the solution in the **Active** column. On the ML Solution form, click the **Show training progress** related link to check the training solution progress.


