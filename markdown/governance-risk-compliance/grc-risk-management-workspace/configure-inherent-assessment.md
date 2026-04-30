---
title: Configure an inherent assessment
description: Configure and publish an inherent assessment in the Advanced Risk application to assess the inherent risks in your organization.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Perform Advanced Risk Assessment, Use, Risk Management, Governance, Risk, and Compliance]
---

# Configure an inherent assessment

Configure and publish an inherent assessment in the Advanced Risk application to assess the inherent risks in your organization.

## Before you begin

Role required: sn\_risk.admin

## About this task

Configure the criteria for an inherent risk assessment by adding the factors, scoring logic, and rating criteria to the Inherent Assessment form. Each risk assessment methodology \(RAM\) has its own inherent assessment criteria. For example, you can assess the inherent risk for such factors as the financial impact, regulatory impact, and client impact. To get the inherent assessment score, the impact of these factors is multiplied by the likelihood that a risk would occur.

## Procedure

1.  Navigate to the RAM form that has the inherent risk as an assessment type.

2.  In the Assessment Types related list, select **Inherent Assessment**.

3.  On the form, fill in the fields.

    For a description of the field values on the inherent assessment form, see [Inherent Assessment form](../reference/inherent-assessment-form.md).

4.  To add factors, select the Factors related list.

    This related list is available only when **Factor responses** is selected from the **Calculate based on** field.

5.  Select **Edit** and add the factors.

6.  Select **Save**.

7.  Select the Qualitative Rating Criteria related list and select **New**.

8.  On the form, fill in the fields.

<table id="table_m42_blm_kkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Lower rating interval

</td><td>

Range for qualitative risk ratings. For example, for a range of 0–10, you can enter 0 as the lower range. For a range of 11– 20, the value can be 11 as the lower range.

</td></tr><tr><td>

Rating

</td><td>

Severity of the risk. You can enter ratings such as high, medium, or low. For example, assume that the lower rating interval for the Low rating is 0, and that the lower rating interval for the Medium rating is 11. If the risk score is 15, then the rating criterion is Medium because 15 is in the range of 11-20.

</td></tr><tr><td>

Overridden score

</td><td>

Score that is used when the assessor overrides the risk rating.

</td></tr><tr><td>

Risk color style

</td><td>

Color code style for the background color on the risk rating value and for the text color on the risk assessment instance. For example, for a high risk, you can select the Red color style with the background color as red and the text as black.

</td></tr><tr><td>

Risk appetite scale

</td><td>

Risk appetite scale for the risk rating criteria. The appetite scales must be mapped to the qualitative risk rating criteria in the risk assessment methodology. You can compute the qualitative appetite status that is based on the latest assessment or aggregated rating to provide the qualitative appetite status. For example, you can select a risk appetite scale of **Hungry** for the risk rating of **Very High**. This field appears only when the risk appetite feature is configured in the advanced risk assessment properties. **Important:** In a qualitative risk assessment, map the risk appetite scale to the risk rating criteria for the final assessment type. For example, if you have both residual and inherent assessments, map the risk appetite scale to the risk rating criteria in the residual assessment.

</td></tr></tbody>
</table>    **Note:** Don’t enter negative values in the Qualitative Rating Criteria form.

9.  If you select the **Enable heatmap** option, then do the following actions:

    1.  Select the Heatmap Colors related list.

    2.  In the Risk color style column, specify the risk color style.

10. To define the assessment result mapping for the applicable record types, do the following actions:

    These steps apply when conducting the inherent assessment on an object.

    1.  Select the Assessment Result Mapping related list.

        The Assessment Result Mapping related list appears only when the **Update assessment results to source record** option is selected in the RAM.

    2.  Select the record type.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Risk assessment methodology|Name of the RAM. This field is automatically set based on the selected RAM.|
        |Record Type|Name of the applicable record type. This field is automatically set based on the selected record type.|
        |Inherent risk rating|Column where the inherent risk rating value is stored in the source record. After the assessment, the inherent risk rating result is copied to the column that is selected in this field. This field appears only when the **Assessment contribution** field has **Qualitative** or **Both**.|
        |Inherent ALE|Column where the inherent annual loss expectancy \(ALE\) value is stored in the source record. After the assessment, the inherent ALE result is copied to the column that is selected in this field. This field appears only when the **Assessment contribution** field is set to is **Quantitative** or **Both**.|

        **Note:** If the same record type is used in another risk assessment methodology, the source record will update based on the field defined in the RAM of the latest advanced risk assessment.

    4.  Select **Update**.

11. Select **Submit**.

12. Select **Publish**.


## Result

The assessment type is published.

-   **[Inherent Assessment form](../reference/inherent-assessment-form.md)**  
Use the Inherent Assessment form in the Advanced Risk application to assess the inherent risks in your organization.

**Parent Topic:**[Perform Advanced Risk Assessment](../concept/use-advanced-risk-assessment.md)

