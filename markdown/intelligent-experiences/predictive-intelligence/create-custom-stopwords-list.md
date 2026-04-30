---
title: Create a custom stopwords list
description: Exclude common words you want the system to ignore during training and prediction.
locale: en-US
release: yokohama
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure Predictive Intelligence, Predictive Intelligence, Enable AI experiences]
---

# Create a custom stopwords list

Exclude common words you want the system to ignore during training and prediction.

## Before you begin

Role required: admin or ml\_admin

## About this task

Stopwords lists enable the system to exclude extraneous words that can impede search and the overall natural language processing of your data.

Predictive Intelligence provides you with default stopwords lists for each language the system supports. Examples of stopwords include words such as in, the, and the names of people and companies. You can also define your own stopwords list that's comprised of words specific to your organization and industry.

The custom list you provide works alongside those that the system already uses by default. For example, if incident records are used in a classification solution, and a company name is used in those records, consider adding that name to your list, as it's unlikely to provide any relevant information for the solution you're building.

In this example scenario, you create a custom stopwords list for the Brazilian Portugese language.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Stopwords**.

2.  On the Stopwords list, click **New**.

    ![This image shows the list of default stopword lists for the various processing languages supported in this release.](../images/stopword-list-default.png)

3.  In the Stopwords form, configure these fields.

    |Field|Value|
    |-----|-----|
    |Name|Enter a unique name for the list, such as the name of your company and the processing language. For example, `Blitzo Brazilian Portuguese Stopwords`.|
    |Stopwords Language|Select **Brazilian Portuguese**|
    |Stopwords List|Manually enter the stopwords using a comma-separated format. For more examples of stopwords, see the image in Step 2 of this procedure.|

    ![This image shows an example list of Brazilian Portuguese stopwords for your custom stopwords list.](../images/stopword-list-custom1.png)

4.  Click **Submit**.

    Your custom stopwords list appears in the Stopwords list view.

    ![When you submit your stopwords list, it appears in the Stopwords list view.](../images/stopword-list-custom2.png)

5.  If you need to update your stopwords list, just click its Name, add or remove words from the list, and click **Update**.

    ![This image shows you how to update your stopwords list, if needed.](../images/stopword-list-custom3.png)


## What to do next

Assign a custom or default stopwords list to a classification, similarity, clustering, or regression solution definition.

