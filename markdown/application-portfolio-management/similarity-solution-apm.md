---
title: Train the similarity solution for Enterprise Architecture to categorize applications while registering
description: Train the business application similarity definition included within the Predictive Intelligence for Enterprise Architecture to suggest a category for a business application when it is being registered or on-boarded.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Train the similarity solution for Enterprise Architecture to categorize applications while registering

Train the business application similarity definition included within the Predictive Intelligence for Enterprise Architecture to suggest a category for a business application when it is being registered or on-boarded.

## Before you begin

Ensure that the Enterprise Architecture – Predictive Intelligence plugin \(com.snc.apm.predictive\_intelligence\) is activated.

The Business Application Similarity solution uses textual similarity to compare business application records. It analyzes the Name and Description fields of existing business applications and compares them with new or updated records. During training, the system builds a model using words and phrases from existing application records. When a new business application is registered or on‑boarded, the system compares its text against previously trained records to identify applications with similar terminology and context. If the new application closely matches existing applications, the system suggests the most common category used by those similar applications.

Role required: ml\_admin

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Similarity** &gt; **Solution Definitions**.

2.  In the Similarity Definitions \[ML view\], click the Business Application Similarity \(ml\_sn\_sn\_apm\_ml\_global\_ba\_similarity\) label.

3.  On the Similarity Definition Business Application Similarity \[ML view\] form, verify the default values for business application similarity.

    For more information on the Similarity Definition form fields, see [Create and train a similarity solution](https://www.servicenow.com/docs/access?context=create-similarity-solution&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

    **Note:** Set the application scope to Enterprise Architecture – Predictive Intelligence to edit the form. Click the word here at the end of the warning message that appears.

<table id="table_ak1_zww_4lb"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Unique name for your similarity definition.

</td></tr><tr><td>

Word Corpus

</td><td>

Collection of words and phrases related to the name and description of the business application that functions as the vocabulary the system uses to compare your instance records based on their textual similarity.

</td></tr><tr><td>

Processing Language

</td><td>

Dominant language of the dataset that you are training on the solution definition. If the dataset language is Italian, choose Italian.**Note:** English processing is applied to all datasets by default.

</td></tr><tr><td>

Stopwords

</td><td>

Existing word corpus that is relevant to your solution. You can also add stopwords to the list, for example, words like Application.

</td></tr><tr><td>

Training Frequency

</td><td>

Option to retrain from once daily or every 30 days in three months increments up to 180 days.

</td></tr><tr><td>

Update Frequency

</td><td>

Frequency at which you want to refresh the data you use to retrieve your similarity results.

</td></tr></tbody>
</table>4.  Click **Update &amp; Retrain**.


## What to do next

You can create a similarity solution with words and phrases related to the name and description of the business application that triggers a prediction. You can also set a training frequency for your machine-learning solution to collect and compare existing records with new records for a similarity definition.

Use the similarity solution to categorize an application while it is on-boarded.

**Parent Topic:**[Configuring Enterprise Architecture \(formerly Application Portfolio Management\)](../concept/configure-apm.md)

