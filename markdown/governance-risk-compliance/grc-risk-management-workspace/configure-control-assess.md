---
title: Configure a control effectiveness assessment
description: Configure and publish a control effectiveness assessment to assess the effectiveness of controls in mitigating risks.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Perform Advanced Risk Assessment, Use, Risk Management, Governance, Risk, and Compliance]
---

# Configure a control effectiveness assessment

Configure and publish a control effectiveness assessment to assess the effectiveness of controls in mitigating risks.

## Before you begin

Role required: sn\_risk.admin

## About this task

Configure the control assessment criteria with details such as factors, the scoring logic, and the rating criteria. You can also specify if you would like to assess the complete control environment or if you would like to assess controls individually. These details are the aspects on which the risk assessment is performed. You can also enable the options to add existing controls or new controls during an assessment. This exercise ensures that each risk assessment methodology \(RAM\) has its own control assessment criteria.

## Procedure

1.  Navigate to the RAM form that has inherent risk as an assessment type.

2.  Under the Assessment Types related list, select **Control Assessment**.

3.  On the form, fill in the fields.

    For a description of the field values on the control assessment form, see [Control Assessment form](../reference/control-assessment-form.md).

4.  Select the Factors section and select **Edit**.

    The Factors related list appears only when **Control environment assessment** is selected from the **Calculate based on** field.

5.  Add the necessary factors from the Collection list to the Factors list, and select **Save**.

6.  Select the Qualitative Rating Criteria related list and select **New**.

7.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Lower rating interval|Range for qualitative risk ratings. For example, for a range of 0–10, you can enter 0 as the lower range. And for a range of 11– 20, the value can be 11 as the lower range.|
    |Risk rating|Severity of the risk. You can enter ratings such as high, medium, or low. For example, assume that the lower rating interval for the Low rating is 0, and that the lower rating interval for the Medium rating is 11. If the risk score is 15, then the rating criterion is Medium because 15 is in the range of 11–20.|
    |Overridden score|Score that the risk assessor can use to override the computed score.|
    |Risk color style|Color code style for the background color on the risk rating value and for the text color on the risk assessment instance. For example, for a high risk, you can select the Red color style with the background color as red and the text as black.|

    **Note:** Don’t enter negative values in the Qualitative Rating Criteria form.

8.  To define the assessment result mapping for the applicable record types, do the following actions:

    These steps apply when conducting the control assessment on an object.

    1.  Select the Assessment Result Mapping related list.

        The Assessment Result Mapping related list appears only when the **Update assessment results to source record** option is selected in the RAM.

    2.  Select the record type.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Risk assessment methodology|Name of the RAM. This field is automatically set based on the selected RAM.|
        |Record Type|Name of the applicable record type. This field is automatically set based on the selected record type.|
        |Control effectiveness|Column where the control effectiveness rating value is stored in the source record. After the assessment, the control effectiveness result is copied to the column selected in this field.|

        **Note:** If the same record type is used in another risk assessment methodology, the source record will update based on the field defined in the RAM of the latest advanced risk assessment.

    4.  Select **Update**.

9.  Select **Submit**.

10. Select **Publish**.


## Result

The control assessment type is published.

-   **[Control Assessment form](../reference/control-assessment-form.md)**  
Use the Control Assessment form in the Advanced Risk application to assess the effectiveness of controls in mitigating risks.

**Parent Topic:**[Perform Advanced Risk Assessment](../concept/use-advanced-risk-assessment.md)

