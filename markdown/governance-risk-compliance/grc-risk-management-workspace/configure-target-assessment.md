---
title: Configure a target assessment
description: Configure and publish a target assessment in the Advanced Risk application to assess your desired future risk level. By configuring a target assessment, you enable the assessors and approvers to perform a target risk assessment in the Next Experience.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Perform Advanced Risk Assessment, Use, Risk Management, Governance, Risk, and Compliance]
---

# Configure a target assessment

Configure and publish a target assessment in the Advanced Risk application to assess your desired future risk level. By configuring a target assessment, you enable the assessors and approvers to perform a target risk assessment in the Next Experience.

## Before you begin

Role required: sn\_risk.admin

## About this task

Configure a target assessment to assess the future risks levels. Similar to inherent and residual assessments, you can define the criteria for conducting target assessments. Configuration includes specifying factors, scoring logic, rating criteria, and heatmap configuration.

## Procedure

1.  Navigate to the Risk assessment methodology \(RAM\) form that has the target risk as an assessment type.

2.  In the Assessment Types related list, select **Target Assessment**.

3.  On the form, fill in the fields.

    For a description of the field values on the Target assessment form, see [Target assessment form](../reference/target-assessment-form.md).

4.  **Note:** If you selected **Factor responses** in the **Calculate based on** field, then you have to add factors to the assessment manually.

    To add factors, select the Factors related list and then do the following steps:

    1.  Select **Edit**.

    2.  Select the factors and add them to the Factors List.

    3.  Select **Save**.

5.  To add qualitative rating criteria, select the Qualitative Rating Criteria related list and select **New**.

6.  On the form, fill in the fields.

<table id="table_m42_blm_kkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Lower rating interval

</td><td>

Range for the qualitative risk ratings. For example, for a range of 0–10, you can enter 0 as the lower range. For a range of 11– 20, the value can be 11 as the lower range.

</td></tr><tr><td>

Risk rating

</td><td>

Severity of the risk. You can enter ratings such as high, medium, or low. For example, assume that the lower rating interval for the Low rating is 0, and that the lower rating interval for the Medium rating is 11. If the risk score is 15, then the rating criterion is Medium because 15 is in the range of 11–20.

</td></tr><tr><td>

Overridden score

</td><td>

Score that the risk assessor can use to override the computed score. This score is associated with the risk when the rating is overridden.

</td></tr><tr><td>

Risk color style

</td><td>

Color code style for the background color on the risk rating value and for the text color on the risk assessment instance. For example, for a high risk, you can select the Red color style with the background color as red and the text as black.

</td></tr><tr><td>

Risk appetite scale

</td><td>

Risk appetite scale for the risk rating criteria. Appetite scales must be separately mapped to the qualitative risk rating criteria for Target Assessment in the RAM form. For example, you can select a risk appetite scale of **Hungry** for the risk rating of **Very High**. This field appears only when the risk appetite feature is configured in the advanced risk assessment properties. Future appetite status is calculated based on the defined risk appetite and the target risk profile.**Note:** The future appetite status can’t be aggregated or rolled up to any specific entities, risk statements, or individual risks.

</td></tr></tbody>
</table>    **Note:** Avoid entering negative values in the Qualitative Rating Criteria form.

7.  Select **Submit**.

8.  If you select the **Enable heatmap** option, you can do the following actions:

    1.  To specify the risk color style, select the Heatmap Colors related list.

    2.  In the Risk color style column, specify the risk color style.

    3.  Select **Submit**.

9.  To define the assessment result mapping for the applicable record types, do the following actions:

    These steps apply when conducting the target assessment on an object.

    1.  Select the Assessment Result Mapping related list.

        The Assessment Result Mapping related list appears only when the **Update assessment results to source record** option is selected in the RAM.

    2.  Select the record type.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Risk assessment methodology|Name of the RAM. This field is automatically set based on the selected RAM.|
        |Record Type|Name of the applicable record type. This field is automatically set based on the selected record type.|
        |Target risk rating|Column where the target risk rating value is stored in the source record. After the assessment, the target risk rating result is copied to the column that is selected in this field. This field appears only when the **Assessment contribution** field has **Qualitative** or **Both**.|
        |Target ALE|Column where the target annual loss expectancy \(ALE\) value is stored in the source record. After the assessment, the target ALE result is copied to the column that is selected in this field. This field appears only when the **Assessment contribution** field is set to is **Quantitative** or **Both**.|

        **Note:** If the same record type is used in another risk assessment methodology, the source record will update based on the field defined in the RAM of the latest advanced risk assessment.

    4.  Select **Update**.

10. Select **Publish.**


-   **[Target assessment form](../reference/target-assessment-form.md)**  
Use the Target Assessment form in the Advanced Risk application to assess the desired future risk level in your organization.

**Parent Topic:**[Perform Advanced Risk Assessment](../concept/use-advanced-risk-assessment.md)

