---
title: Article quality index for knowledge management
description: Assess the quality of knowledge articles with the article quality index \(AQI\). The AQI helps maintain consistent quality of knowledge articles attached to a knowledge base where articles are written by various authors.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exploring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Article quality index for knowledge management

Assess the quality of knowledge articles with the article quality index \(AQI\). The AQI helps maintain consistent quality of knowledge articles attached to a knowledge base where articles are written by various authors.

Using AQI feature, a knowledge administrator \(a user with knowledge\_admin role\) creates a checklist and adds a set of true or false questions to the checklist to assess the quality of knowledge articles. For each question, the knowledge\_administrator assigns a weight based on its importance to the quality measurement and then attaches the checklist to a knowledge base.

A knowledge reviewer \(a user with knowledge\_coach and knowledge\_domain\_expert role\) performs AQI review on knowledge articles attached to the knowledge base by answering the true or false questions in the checklist. The article quality is then scored based on the cumulative weight of all answers set to true in the checklist.

The average AQI scoring is displayed on the Content Quality tab of the Knowledge Management dashboard \(see [Knowledge Management dashboard](../../../use/dashboards/application-content-packs/knowledge-management-dashboard.md)\).

## Activating article quality index

The article quality index feature is activated with the Knowledge Management Advanced \(com.snc.knowledge\_advanced\) plugin. For details see, [Activate the Knowledge Management Advanced plugin](../task/activate-knowledge-advanced-plugin.md).

**Parent Topic:**[Knowledge Management](knowledge-management.md)

**Related topics**  


[Use Article Quality Index](use-article-quality-index.md)

