---
title: Check candidate recommendations in ERP Semantic Mining
description: Check the actions that ERP Semantic Mining suggests for improving the ease of replatforming an ERP \(Enterprise Resource Planning\) candidate.
locale: en-US
release: zurich
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, ERP Semantic Mining overview, Workflow Data Fabric]
---

# Check candidate recommendations in ERP Semantic Mining

Check the actions that ERP Semantic Mining suggests for improving the ease of replatforming an ERP \(Enterprise Resource Planning\) candidate.

## Before you begin

Role required: sn\_erp\_mining.erp\_user

**Important:** Starting with the Zurich release, ERP Semantic Mining is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

## About this task

When you view a candidate, ERP Semantic Mining displays the number of recommended actions or next steps to take.

For example, you may have to create a workflow in Workflow Studio for one candidate, update an integration spoke for another, and read an extraction table for a third candidate.

## Procedure

1.  Navigate to **All** &gt; **ERP Foundation** &gt; **ERP Semantic Mining**.

2.  In the side panel, select the candidates icon ![](../image/erpcm-candidates-icon.png).

    Alternatively, you can select a candidate directly on the ERP Semantic Mining home page. For more information, see [Browse an overview of candidates in ERP Semantic Mining](erpcm-view-home-page-overview.md).

3.  Select the candidate that you want to view the recommended next actions for.

4.  Select the **Recommendations** tab, which summarizes each suggested action.

    For a description of the field values, see [ERP Semantic Mining candidate recommendations field descriptions](../reference/erpcm-candidate-recommendations-field-descriptions.md).

5.  Select a **Recommended action URL** to open the relevant destination on the ServiceNow AI Platform in a new browser tab.

    For example, if the recommendation is to read an extraction table, select the **Recommended action** link to open the ERP model in Zero Copy Connector for ERP, where you can add the suggested table.


**Parent Topic:**[Finding and working with candidates to replatform](../concept/work-with-candidates.md)

