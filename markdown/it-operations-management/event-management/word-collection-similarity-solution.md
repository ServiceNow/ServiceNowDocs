---
title: Similarity solutions
description: Similarity solutions enable you to use Machine Learning \(ML\) to compare the text in a resolved alert record to an open alert record to reuse its resolution approach.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Alert similarity, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Similarity solutions

Similarity solutions enable you to use Machine Learning \(ML\) to compare the text in a resolved alert record to an open alert record to reuse its resolution approach.

## Training a similarity solution

To train a similarity solution, you collect words to compile a collection that Machine Learning \(ML\) can use to compare text in the **Short Description**, **Description**, **Source**, **Type**, **Resource**, and **Metric Name** fields in a resolved alert to see whether the words in the set match words in an open alert. The resolved alert, which is similar to an open alert, provides an example to show how the open alert can be resolved.

To train a solution, the filter must return at least one record. If your filter returns no records, update it.

**Note:** The preferred number of records for training a solution is between 30,000 records and 300,000. If you submit more than 300,000 records, the most recent 300,000 records are used to train the solution. Use only authentic records from the database.

-   Ensure that the records you train are not too old and that they are relevant to your business needs. Keep the words in the collection current.
-   Do not use hard-coded dates as filters because these filters are not updated when you retrain solutions unless you update them manually before every retraining. Instead, use relative date filters, for example, the last 3 months, last 6 months, or last 12 months.
-   Perform training as needed until it provides an acceptable similarity solution. This practice provides you time to review and update your solution definition.

## Fields to include in the solution

Record the fields that are likely to contain words and phrases that help the system identify similar records for your solution.

The similarity fields that you select should be a subset of your input field selections. For example, if you select fields from incident records that are in Open state, do not select **Close note** as a similarity field. Because open records do not include **Close note** fields, the text cannot be similar.

The similarity fields are available to users when they create records.

## About the similarity score

The similarity score is a measure from 0-100 of the degree of similarity between two alert records. Alert records that have a similarity score higher than the threshold that you specify is returned by the solution.

Review similarity examples and their scores using the **Show training progress** feature to determine whether to either increase or decrease the solution threshold. You can change the threshold value in the **Threshold for Similarity Score** field.

## View training solution progress

Training times vary based on the number of records and classes within the training set. The more records and classes you use, the longer the training can take. For example, a data set containing 100,000 records and several hundred classes can take around five hours to complete.

To show the training solution progress, the ML solution automatically performs the following activities when you select **Show training progress** on the Solutions page. For more information, see [View solution training progress](https://www.servicenow.com/docs/access?context=view-training-progress&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

|Activity|Description|
|--------|-----------|
|Fetching files for training.|The system downloads the training records and sends them to the nearest training service.|
|Preparing the data.|The system removes duplicate records from the training set.|
|Training the solution.|The training service trains the solution.|
|Uploading the trained solution.|The training service uploads the solution as attachment records.|

**Parent Topic:**[Alert similarity](alert-similarity.md)

