---
title: Recommendations and similar candidates in ERP-CM
description: The record for each candidate in ERP Semantic Mining \(ERP-CM\) displays information on suggested next steps and similar candidates to help you in replatforming an ERP \(Enterprise Resource Planning\) app.
locale: en-US
release: yokohama
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exploring ERP Semantic Mining, ERP Semantic Mining \(ERP-CM\), Building low-code applications, Developing your application, Building applications]
---

# Recommendations and similar candidates in ERP-CM

The record for each candidate in ERP Semantic Mining \(ERP-CM\) displays information on suggested next steps and similar candidates to help you in replatforming an ERP \(Enterprise Resource Planning\) app.

## Recommended actions for candidates

When you view a candidate, ERP-CM displays the number of recommended actions or next steps to take. The candidate details also have a **Recommendations** tab where you can view the suggested actions, and select them to open the associated app on the ServiceNow AI Platform.

For example, you may need to create a workflow in Workflow Studio for one candidate, update an integration spoke for another, and read an extraction table or remote table for a third candidate.

Each recommended action has an estimated effort, which is a numerical score that assesses how well the ServiceNow AI Platform has matching functionality. Green actions require little-to-no effort, while red actions are more difficult.

![ERP Semantic Mining candidates page with recommendations tab displayed.](../image/ecm-recommendations-tab.png)

For more information on recommended actions, see [Check candidate recommendations in ERP-CM](../task/erpcm-work-with-recommendations.md).

## Similar candidates in candidate details

For each candidate, ERP-CM displays a **Similar candidates** tab, which lists each similar candidate, a numerical score to represent how closely the two candidates are related, and a link to other similar candidates.

Similar candidates are helpful when planning how to best replatform a legacy app. When you replatform a custom app from the system of record, you don't have to replicate the old app exactly. Use the replatforming process to design a better app, perhaps one that addresses the needs of multiple similar candidates in a single, new app built using low-code tools on the ServiceNow AI Platform.

**Parent Topic:**[Exploring ERP Semantic Mining](exploring-ecm.md)

