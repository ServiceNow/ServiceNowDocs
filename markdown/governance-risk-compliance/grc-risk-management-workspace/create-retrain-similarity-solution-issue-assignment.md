---
title: Train and use the similarity solution definition for issue assignment prediction
description: Train and use the machine learning solution by activating the Governance, Risk, and Compliance Predictive Intelligence plugin. The solution enables the system to automatically suggest correct assignees to route issues. These suggestions reduce the time spent on deciding who should own the issue.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Issue assignment using the Governance, Risk, and Compliance Predictive Intelligence plugin, Manually create GRC issues, Use, Risk Management, Governance, Risk, and Compliance]
---

# Train and use the similarity solution definition for issue assignment prediction

Train and use the machine learning solution by activating the Governance, Risk, and Compliance Predictive Intelligence plugin. The solution enables the system to automatically suggest correct assignees to route issues. These suggestions reduce the time spent on deciding who should own the issue.

## Before you begin

Make sure that the following plugins are activated.

-   The Policy and Compliance Management plugin
-   The Risk Management plugin
-   GRC Profiles plugin must be activated
-   The Predictive Intelligence plugin

Modify the following [Governance, Risk, and Compliance properties](../../grc-common/reference/grc-properties.md) with the sn\_grc.admin role.

-   **Issue assignee suggestion based on** property \(**Similarity Analysis**\).
-   **Machine Learning Solution for prediction of issue assignee** property \(**ml\_x\_snc\_sn\_grc\_pred\_intel\_global\_similarity\_solution\_definition\_for\_assigned\_to\_for\_issue**\).

Role required: ml\_admin

## Procedure

1.  Navigate to **Predictive Intelligence** &gt; **Similarity** &gt; **Solution Definitions**.

2.  Click the **Similarity Solution Definition for Assigned To for Issue** solution.

<table id="table_o1g_bfj_3fb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Unique name for the similarity solution.

</td></tr><tr><td>

Name

</td><td>

Name of the similarity solution. This field is automatically set to the system-assigned name that is the most similar to your value for the **Label** field.

</td></tr><tr><td>

Word Corpus

</td><td>

Existing word corpus that is relevant to your solution. For this use case, select the **Word Corpus for Issue Assignment** word corpus.**Note:** For word corpora in similarity solutions, the number of records per table is limited to 300,000.

</td></tr><tr><td>

Table

</td><td>

Table that contains the records that you want to train against and to predict for. When you assign a table value, a link appears in the form. The link shows the number of records that match your current conditions. For this use case, the field is automatically set to the Issue \[sn\_grc\_issue\] table. Do not modify this field for this solution definition.

</td></tr><tr><td>

Fields

</td><td>

Field types that are likely to help in identifying the owner. You can select the columns from the table in the **Table** field so that their data helps in predicting the issue more accurately. In this use case, the **Short description** and the **Description** fields are selected. These fields are the field types that contain the text of the issue records whose owner you're trying to identify.**Note:** You can modify the fields selected here if there are other non-empty important fields on the issue record in your database, such that these fields can help in finding out similar issues for predicting the issue owners.

</td></tr><tr><td>

Test Table

</td><td>

Table that contains the record that you want to predict for. For this use case, the field is automatically set to the Issue \[sn\_grc\_issue\] table.**Note:** The number of records which the Similarity window can retrieve is limited to 10. This field must not be modified for this solution definition.

</td></tr><tr><td>

Test Fields

</td><td>

Fields which are used as input during prediction. In this use case, select **Short description** and **Description**.**Note:** You can modify the fields selected here if there are other non-empty important fields on the issue record in your database, such that these fields can help in finding out similar issues for predicting the issue owners.

</td></tr><tr><td>

Filter

</td><td>

Filter that applies conditions to the field records that you're using as a base to retrieve your similarity results. For example in this use case, you can set an **Assigned to \[is\] \[not empty\]** condition because leaving the field empty will not provide a suggestion.

</td></tr><tr><td>

Processing Language

</td><td>

Dominant language of the dataset that you are training on the solution definition. If the dataset language is English, choose **English**. By default, English processing is applied to all datasets. For example, if you select **Italian**, the system processes the data in both English and Italian.

**Note:** The term processing indicates some of the language-specific steps that are used as part of training a solution. These steps include tokenizing words, removing stop words, and stemming.

</td></tr><tr><td>

Stopwords

</td><td>

List of stopwords. When you select your processing language, the system automatically adds a Stopwords list that uses the same language. For example, if your processing language is English, the **Default English Stopwords** option appears. The Default English Stopwords list also appears in your selection. You can add your own custom list of stopwords.

</td></tr><tr><td>

Training Frequency

</td><td>

Frequency of training. The retraining option can range from once a day to every 30 days in 3 month increments up to 180 days.

</td></tr><tr><td>

Update Frequency

</td><td>

Frequency of how often you want to refresh the data that you use to retrieve your similarity results. For example, new issues typically occur frequently throughout the day. If you have issue records that are open, you may want to select an update frequency of **Every 15 minutes**. This frequency can increase the likelihood that newly opened records are included in the refresh.

</td></tr></tbody>
</table>3.  Click the appropriate button for the solution definition.

    |Option|Description|
    |------|-----------|
    |**Save**|Save your solution definition record so that you can return to it later.|
    |**Update and Retrain**|Modify your solution definition and train it.|


**Parent Topic:**[Issue assignment using the Governance, Risk, and Compliance Predictive Intelligence plugin](../concept/issue-assignment-using-predictive-intelli.md)

