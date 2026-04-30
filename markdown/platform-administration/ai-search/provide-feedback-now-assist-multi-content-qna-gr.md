---
title: Provide feedback on Now Assist Multi-Content Response Genius Result answers
description: Provide positive or negative feedback on Now Assist Multi-Content Response Genius Result answers.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-09-08"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Now Assist in AI Search, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Provide feedback on Now Assist Multi-Content Response Genius Result answers

Provide positive or negative feedback on Now Assist Multi-Content Response Genius Result answers.

## Before you begin

You can perform this task when viewing a Now Assist Multi-Content Response Genius Result answer in a search portal that uses the faceted search widget.

Role required: none

## About this task

Use the thumb-up and thumb-down icons in a Now Assist Multi-Content Response Genius Result answer to submit positive or negative feedback on the answer. Positive feedback indicates that the answer provided you with the information you were looking for. Negative feedback indicates that the answer didn't help you with your question.

**Note:** You can only submit feedback once per Now Assist Multi-Content Response Genius Result answer.

Feedback for Now Assist Multi-Content Response Genius Result answers is stored in the Generative AI Log \[sys\_generative\_ai\_log\] and Genius Result Event Actions \[sys\_search\_genius\_result\_event\_action\] tables. Users with the admin role can view answer feedback metadata in the Gen AI Log Metadata \[sys\_gen\_ai\_log\_metadata\] table.

## Procedure

1.  In the Now Assist Multi-Content Response Genius Result answer, select the thumb icon that matches your desired feedback type.

    -   If the answer provided the information you wanted, provide positive feedback by selecting the thumb-up icon ![](../image/now-assist-mc-qna-gr-thumb-up.png).
    -   If the answer did not address your question, provide negative feedback by selecting the thumb-down icon ![](../image/now-assist-mc-qna-gr-thumb-down.png).
2.  If you chose negative feedback, select the option that best explains why the answer didn't help you.

    If none of the predefined options explains why the answer didn't help you, select **Other**, then enter your own explanation into the text field.

3.  Select **Submit feedback**.


## Result

Your feedback is submitted for the Genius Result answer. The thumb-up and thumb-down icons for the answer become inactive, indicating that you've already submitted feedback for the answer.

