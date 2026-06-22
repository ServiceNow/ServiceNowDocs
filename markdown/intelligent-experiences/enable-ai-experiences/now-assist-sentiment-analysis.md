---
title: Sentiment Analysis
description: Apply Now Assist Sentiment Analysis to each customer interaction to assess user satisfaction and facilitate informed decision-making. The customer communications can be related to cases, records, or problems. Use this skill to prioritise this data based on the overall sentiment and reasoning, by providing generative AI analysis to the fulfillers and enabling them identify cases that require urgent attention.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/intelligent-experiences/enable-ai-experiences/now-assist-sentiment-analysis.html
release: xanadu
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: concept
last_updated: "2025-04-11"
reading_time_minutes: 2
breadcrumb: [Analysis skills, Now Assist skills, Exploring Now Assist, Now Assist, Enable AI experiences]
---

# Sentiment Analysis

Apply Now Assist Sentiment Analysis to each customer interaction to assess user satisfaction and facilitate informed decision-making. The customer communications can be related to cases, records, or problems. Use this skill to prioritise this data based on the overall sentiment and reasoning, by providing generative AI analysis to the fulfillers and enabling them identify cases that require urgent attention.

Now Assist Sentiment Analysis uses large language model \(LLM\) to produce sentiment evaluations for new or active case/problem records, and it also illustrates sentiment trends over time. Fulfillers are provided with a summary to comprehend the reasons behind the sentiments without reading all the notes and comments. This enables them to prioritize and focus on urgent cases and issues based on the severity of the sentiments, and improve the overall customer experience.

## Now Assist Sentiment Analysis refresh

The skill saves the analysis, trends and reasoning on the record and doesn't refresh with page refreshes. LLM calls are made for sentiment refresh when there is a relevant change on that specific record or updates to the input fields defined in the input prompt. The input fields are defined in Now Assist Admin, as parameters for analysing the customer interaction. Now Assist Sentiment Analysis will apply only to records that meet the filter conditions specified in the input templates, as well as those defined in the availability section of Now Assist Admin.

## Now Assist Sentiment Analysis in list view

The saved values for sentiment, sentiment trends and the underlying reasonings will also be available in the list view.

While you're in a list view, if any underlying records have been updated and a new LLM call is triggered, you will receive a notification prompting you to refresh the page. This helps you to stay informed and engaged with the latest information. Although the list can be long, the visual notification will focus only on the records currently visible on your page, which helps you maintain relevance as you work through the sentiment evaluations.

## Generating Now Assist Sentiment Analysis

You can generate sentiment analysis for the following products.

-   [Analyze sentiments in Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/customer-service-management/now-assist-for-csm/analyze-sentiments-in-now-assist-for-csm.md)
-   [Analyze sentiments in Now Assist for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/it-service-management/now-assist-for-it-service-management-itsm/sentiment-analysis-now-assist-itsm.md)

## Availability

This skill is available in the workflow and product listed below.

<table id="table_r25_vxc_dbcsssdf"><thead><tr><th>

Workflow

</th><th>

Product

</th></tr></thead><tbody><tr><td>

Technology

</td><td>

[Now Assist for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm.md)

</td></tr><tr><td>

Customer

</td><td>

[Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/customer-service-management/now-assist-for-csm/now-assist-csm.md)

</td></tr></tbody>
</table>