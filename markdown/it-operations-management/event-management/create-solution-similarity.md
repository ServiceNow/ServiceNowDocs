---
title: Create an Event Management similarity solution
description: Create and train a solution that applies machine learning to a collection of words to target and suggest similar alerts in your instance dataset. For example, you can compare the text in a resolved alert record to an open alert record to reuse its resolution approach.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Alert similarity, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Create an Event Management similarity solution

Create and train a solution that applies machine learning to a collection of words to target and suggest similar alerts in your instance dataset. For example, you can compare the text in a resolved alert record to an open alert record to reuse its resolution approach.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

The encryption scheme that you use can affect whether you can train solutions.

-   If your data is encrypted by Full Disc Encryption \(FDE\), you can train solutions.
-   If the field you are using for training is encrypted using Field Encryption, ensure that the shared service worker user has the correct encryption module role that has been used for encryption.
-   If you are using Edge Encryption, training is not supported.

**Note:** This feature supports only English language processing.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Similarity** &gt; **Solution Definitions**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_o1g_bfj_3fb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Solution Template

</td><td>

Use to define a word collection.

</td></tr><tr><td>

Label

</td><td>

Unique name for the similarity solution.

</td></tr><tr><td>

Name

</td><td>

Field that is auto-populated with a system-assigned name that is similar to the label name when the solution is created.

</td></tr><tr><td>

Table

</td><td>

Table that contains the records to use for the word collection, for example, the Incident table or the Asset table. When you assign a table value, a link appears that shows the number of records that match your current conditions.

</td></tr><tr><td>

Filter

</td><td>

Conditions that you want to apply to the training records. To train a solution, the filter must return at least one record. If your filter returns no records, update it.

</td></tr><tr><td>

Input Fields

</td><td>

Record the fields that contain the text and context that you want to include in your word collection.The field data type can be a string, reference, choice, or HTML, such as **Short description** and **Description**.

 **Note:** **Journal type** is not a supported data type.

 Good candidates for your input fields have text that is relevant to the solution. For example, if you are configuring a solution to find similar incident records, you can select the **Short Description**, **Description**, **Resolution notes**, and **Close notes** fields.

</td></tr><tr><td>

Training Frequency

</td><td>

Training is performed once by the system, by default. Because your data can age over time and degrade the accuracy of recommendations, consider invoking scheduled trainings once your solution definition is fairly stable.

</td></tr><tr><td>

Domain

</td><td>

On instances where domain separation is active, select the domain whose target records you want to use for your word collection. Create a separate similarity solution definition record for each domain whose field values you want to use for your word collection.

</td></tr><tr><td>

Similarity Fields

</td><td>

Record fields that are likely to contain words and phrases that help the system identify similar records for your solution.To change your **Similarity Field** choices, click the Lock icon \(![Lock icon](../image/lock-tag.png)\) to open the field and make your updates. Click the icon again to close the field and save your updates.

</td></tr><tr><td>

Similarity Window

</td><td>

The period in which you want to look for similar records. If you have a smaller number of total incoming records, a larger window might be best. However, if the window is too large, you may retrieve records that are not as useful. If the window is too small, you might not retrieve enough similar records. For example, if you are looking for similar incident records that are open, you can select **Last 1 day**. This selection targets the most recent records, many of which could still be open.

</td></tr><tr><td>

Similarity Window Filters

</td><td>

Filter conditions for your similarity window. These filters define the dataset conditions under which your similarity results are determined. For example, if you are looking for similar incident records that are open, you can filter your search by creating conditions such as: **\[Incident state\] \[is\] \[In progress\]**

 These filters are applied in addition to the **Input Field** filters.

</td></tr><tr><td>

Window Refresh Frequency

</td><td>

Frequency to refresh the similarity window. For example, if your window contains incident records that are open, you can select a refresh frequency value of **Every 15 minutes**. New incidents typically occur frequently throughout the day so this frequency increases the likelihood that newly opened records are included in the refresh. **Note:** If your similarity window is composed of records such as Knowledge article records, which are typically not created often, you can choose a larger refresh frequency such as **Every 1 day**.

</td></tr></tbody>
</table>4.  Click **Save** to save the solution definition record so you can return to it later, or click **Submit &amp; Train** to create the solution definition record and train it.

5.  If you submitted the solution for training, click **OK** on the **Training Activation** window to confirm.


## Result

The system schedules the solution for training with the nearest training service. You and other users subscribed to the Predictive Intelligence Notifications category receive a notification when the training completes, including any errors that might have occurred in the training. When training is complete, the system uploads the solution as an Attachment record.

## What to do next

Review the trained similarity solution examples in the **Similarity Examples** related link on your ML Solution Definition form.

**Parent Topic:**[Alert similarity](../concept/alert-similarity.md)

