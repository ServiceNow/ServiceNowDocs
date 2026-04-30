---
title: ERP-CM candidate recommendations field descriptions
description: On a candidate record in ERP Semantic Mining \(ERP-CM\) the Recommendations tab displays information about suggested next actions for replatforming ERP \(Enterprise Resource Planning\) candidates.
locale: en-US
release: yokohama
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ERP-CM field descriptions, ERP Semantic Mining reference, ERP Semantic Mining \(ERP-CM\), Building low-code applications, Developing your application, Building applications]
---

# ERP-CM candidate recommendations field descriptions

On a candidate record in ERP Semantic Mining \(ERP-CM\) the **Recommendations** tab displays information about suggested next actions for replatforming ERP \(Enterprise Resource Planning\) candidates.

For process details, see [Check candidate recommendations in ERP-CM](../task/erpcm-work-with-recommendations.md).

<table id="table_u5j_gnl_wyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Recommended action URL

</td><td>

Link to the recommended action.Select the recommendation link to open the relevant destination on the ServiceNow AI Platform. For example, the **Build a workflow** recommended URL would link to the flow in Workflow Studio.

</td></tr><tr><td>

Recommended action

</td><td>

Brief description of the action that ERP-CM suggests you take on a candidate when replatforming.

</td></tr><tr><td>

Effort estimation

</td><td>

Numerical score for how much effort the recommended action should require.Each recommended action has an estimated effort, which is a numerical score that assesses how well the ServiceNow AI Platform has matching functionality. Green actions require little-to-no effort, while red actions are more difficult.

</td></tr><tr><td>

Score improvement

</td><td>

The possible increase in the overall potential for a candidate if you implement the recommendation. Each time the AI/ML workflow is triggered, either automatically or manually, score improvements are calculated.

</td></tr><tr><td>

Table operation

</td><td>

The action you should take on the table, such as **Read** or **Update**.

</td></tr><tr><td>

Recommended technology

</td><td>

App or product on the ServiceNow AI Platform where you take the recommended action.

</td></tr><tr><td>

Max number of rows \(DB\)

</td><td>

The maximum number of database rows on the system of record that the recommended action allows.

</td></tr><tr><td>

Updated

</td><td>

Date and time the recommended action was most recently updated.

</td></tr></tbody>
</table>**Parent Topic:**[ERP-CM field descriptions](../concept/erpcm-field-description-reference-landing.md)

