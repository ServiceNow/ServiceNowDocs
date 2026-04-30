---
title: Check candidate recommendations in ERP-CM
description: Check the actions that ERP Customization Mining \(ERP-CM\) suggests to improve the ease of replatforming an ERP \(Enterprise Resource Planning\) candidate.
locale: en-US
release: xanadu
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Finding and working with candidates to replatform, ERP Customization Mining \(ERP-CM\), Building low-code applications, Developing your application, Building applications]
---

# Check candidate recommendations in ERP-CM

Check the actions that ERP Customization Mining \(ERP-CM\) suggests to improve the ease of replatforming an ERP \(Enterprise Resource Planning\) candidate.

## Before you begin

Role required: sn\_erp\_mining.erp\_user

## About this task

When you view a candidate, ERP-CM displays the number of recommended actions or next steps to take.

For example, you may need to create a workflow in Workflow Studio for one candidate, update an integration spoke for another, and read an extraction table or remote table for a third candidate.

## Procedure

1.  Navigate to **All** &gt; **ERP Foundation** &gt; **ERP Customization Mining**.

2.  In the side panel, select the candidates icon \(![Candidates icon](../image/erpcm-candidates-icon.png)\).

    Alternatively, you can select a candidate directly on the ERP-CM home page. For more information, see [Browse an overview of candidates in ERP-CM](erpcm-view-home-page-overview.md).

3.  Select the candidate that you want to view the recommended next actions for.

4.  Select the **Recommendations** tab, which summarizes each suggested action.

    For a description of the field values, see [ERP-CM candidate recommendations field descriptions](../reference/erpcm-candidate-recommendations-field-descriptions.md).

    ![Candidate recommendations](../image/erpcm-recommended-actions.png "Recommendations in ERP-CM")

    **Note:** The score improvement feature is available starting with Xanadu Store Release 2.

5.  Select a **Recommended action URL** to open the relevant destination on the ServiceNow AI Platform in a new browser tab.

    For example, if the recommendation is to read an extraction table, select the **Recommended action** link to open the ERP model in ERP Data Hub, where you can add the suggested table.


**Parent Topic:**[Finding and working with candidates to replatform](../concept/work-with-candidates.md)

