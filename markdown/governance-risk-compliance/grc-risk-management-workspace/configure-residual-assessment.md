---
title: Configure a residual assessment
description: Configure and publish a residual assessment in the Advanced Risk application to assess the residual risks in your organization.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Perform Advanced Risk Assessment, Use, Risk Management, Governance, Risk, and Compliance]
---

# Configure a residual assessment

Configure and publish a residual assessment in the Advanced Risk application to assess the residual risks in your organization.

## Before you begin

Role required: sn\_risk.admin

## About this task

Use a residual assessment to identify and assess the risks that exist after any controls are implemented. If no controls are identified, then the residual risk is the same as an inherent risk. If the factors for an inherent assessment are used a residual assessment, then you can copy the assessment contribution, qualitative scoring logic, factors, and qualitative rating criteria from the inherent assessment. You can also choose how you want to derive the score of the residual assessment.

## Procedure

1.  Navigate to the risk assessment methodology \(RAM\) form that has the residual risk as an assessment type.

2.  In the Assessment Types related list, select **Residual Assessment**.

3.  On the form, fill in the fields.

    For a description of the field values on the residual assessment form, see [Residual Assessment form](../reference/residual-assessment-form.md).

4.  If you selected **Factor responses** in the **Calculate based on** field, then select the Factors related list so that you can add factors to the residual assessment.

5.  Select **Edit**, add the necessary factors, and then select **Save**.

6.  If the **Calculate based on** field has **Inherent risk and control effectiveness** and if the **Qualitative scoring logic** field has **Lookup matrix between inherent assessment and control effectiveness**, then do the following actions:

    1.  Select the Matrix related list.

    2.  In the respective columns, enter the score, risk rating, risk color style, and overridden score.

7.  Select the Qualitative Rating Criteria related list and select **New**.

8.  On the form, fill in the fields.

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

Score that the risk assessor can use to override the computed score.

</td></tr><tr><td>

Risk color style

</td><td>

Color code style for the background color on the risk rating value and for the text color on the risk assessment instance. For example, for a high risk, you can select the Red color style with the background color as red and the text as black.

</td></tr><tr><td>

Risk appetite scale

</td><td>

Risk appetite scale for the risk rating criteria. Appetite scales must be mapped to the qualitative risk rating criteria in the risk assessment methodology. Compute the qualitative appetite status that is based on the latest assessment or aggregated rating to provide the qualitative appetite status. For example, you can select a risk appetite scale of **Hungry** for the risk rating of **Very High**. This field appears only when the risk appetite feature is configured in the advanced risk assessment properties. **Important:** In a qualitative risk assessment, map the risk appetite scale to the risk rating criteria for the final assessment type. For example, if you have both residual and inherent assessments, map the risk appetite scale to the risk rating criteria in the residual assessment.

</td></tr></tbody>
</table>    **Note:** Don’t enter negative values in the Qualitative Rating Criteria form.

9.  Select the Heatmap Colors related list.

    This related list appears only when all of the following are true:

    -   The **Enable heatmap** option is selected.
    -   The **Calculate based on** field has **Factor responses**.
    -   The residual assessment is based on a matrix between the inherent assessment and control effectiveness.
10. In the Risk color style column, select the background color and text color combination.

11. To define the assessment result mapping for the applicable record types, do the following actions:

    These steps apply when conducting the residual assessment on an object.

    1.  Select the Assessment Result Mapping related list.

        The Assessment Result Mapping related list appears only when the **Update assessment results to source record** option is selected in the RAM.

    2.  Select the record type.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Risk assessment methodology|Name of the RAM. This field is automatically set based on the selected RAM.|
        |Record Type|Name of the applicable record type. This field is automatically set based on the selected record type.|
        |Residual risk rating|Column where the residual risk rating value is stored in the source record. After the assessment, the residual risk rating result is copied to the column that is selected in this field. This field appears only when the **Assessment contribution** field has **Qualitative** or **Both**.|
        |Residual ALE|Column where the residual annual loss expectancy \(ALE\) value is stored in the source record. After the assessment, the residual ALE result is copied to the column that is selected in this field. This field appears only when the **Assessment contribution** field is set to is **Quantitative** or **Both**.|

        **Note:** If the same record type is used in another risk assessment methodology, the source record will update based on the field defined in the RAM of the latest advanced risk assessment.

    4.  Select **Update**.

12. Select **Submit** and then select **Publish**.


## Result

The assessment type is published.

-   **[Residual Assessment form](../reference/residual-assessment-form.md)**  
Use the Residual Assessment form in the Advanced Risk application to assess the residual risks in your organization.

**Parent Topic:**[Perform Advanced Risk Assessment](../concept/use-advanced-risk-assessment.md)

