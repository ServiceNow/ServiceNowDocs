---
title: Set up risk identification integration
description: Before assessing an application, specify the target application where the risk identification must be initiated.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Application risk assessment using Advanced Risk Assessment, Integrate, Risk Management, Governance, Risk, and Compliance]
---

# Set up risk identification integration

Before assessing an application, specify the target application where the risk identification must be initiated.

## Before you begin

Make sure you have the following applications:

-   Application Portfolio Management must be installed if you want the recommendation engine enabled and want to use the integration.
-   Application Portfolio Management integration with Risk Management \(com.snc.apm\_risk\_assessment\) must be installed. This application is required only if you want to use the integration.
-   Smart Assessment Engine and GRC Common Workspace Elements must be installed to use the smart assessment questionnaire during the risk identification. For more information, see [Configuring Smart Assessment Engine](../../assessment-engine/concept/smart-assessment-engine-cf-config.md).

Role required: sn\_risk.admin

## About this task

The Risk Identification Configuration form contains an entity type and a default identification record for the business application table. As a risk admin, you can either modify the default record or create your own configuration. The steps in this procedure are for creating a record. The Risk Identification Configuration form is used to do the following:

-   Gather information about the application by using a questionnaire.
-   Determine the criticality of the application.
-   Determine if an inherent assessment for the application is required.
-   Identify risks and map the relevant controls.
-   Choose to receive recommendations for risks and controls.

## Procedure

1.  Navigate to **All** &gt; **Advanced Risk Assessment** &gt; **Administration** &gt; **Risk Identification Configuration**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_djz_4wg_smb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the configuration. An example is `Risk Identification for Business Application`.

</td></tr><tr><td>

Configuration level

</td><td>

The level where the configuration is done. The choices are as follows:-   Entity class
-   Table


</td></tr><tr><td>

Target entity class

</td><td>

Entity class for which the risk identification questionnaire is initiated. For each entity of this entity class, a risk identification record is automatically created. This field appears only when **Entity class** is selected from **Configuration level**.

</td></tr><tr><td>

Target table

</td><td>

Table that contains the application record. For each entity of this table, a risk identification record is automatically created. This field appears only when **Table** is selected from **Configuration level**.

</td></tr><tr><td>

State

</td><td>

State of the configuration. This field is automatically set to **Draft**.

</td></tr><tr><td>

Risk manager group

</td><td>

Group which reviews the risk identification workflow. The users who belong to this group must have the sn\_risk.manager and sn\_compliance.manager roles.

</td></tr><tr><td>

Identification questionnaire

</td><td>

Option to initiate a questionnaire for gathering information about the application.

</td></tr><tr><td>

Inherent assessment

</td><td>

Option to perform inherent assessment or business impact analysis \(BIA\) assessment.

</td></tr><tr><td>

Recommendation engine

</td><td>

Option to recommend risks and controls. This option is available only when the **Target table** field has **Business Application**.

</td></tr><tr><td class="sub-head" colspan="2">

Identification Questionnaire

</td></tr><tr><td>

Use smart assessment

</td><td>

Option enables the use of smart assessment templates. You can select a smart assessment template in the **Questionnaire** field.For more information on how to create a smart assessment template, see [Create a smart assessment template for risk identification](create-smart-assessment-template-for-risk-identification.md).

</td></tr><tr><td>

Questionnaire

</td><td>

Questionnaire used for information gathering.**Note:** You can see a list of smart assessment templates only when you select the option **Use smart assessment**. Only published assessment templates with a Risk Identification category and the **Assessment target** field selected as `Entity` are available for selection.

</td></tr><tr><td>

Respondent type

</td><td>

Respondent of the questionnaire. The choices are as follows:-   Entity owner
-   User on target record


</td></tr><tr><td>

Questionnaire review required

</td><td>

Option to require that the questionnaire is reviewed by a reviewer.

</td></tr><tr><td>

Respondent field

</td><td>

Field on the target table that contains the respondent for the questionnaire. This field appears when the **Respondent type** field has **User on target record**.

</td></tr><tr><td class="sub-head" colspan="2">

Inherent Assessment

</td></tr><tr><td>

Review for inherent assessment required

</td><td>

Option to choose if the inherent assessment must be reviewed.

</td></tr><tr><td>

Risk assessment methodology

</td><td>

Option to select the risk assessment methodology \(RAM\) to perform inherent assessment. You can see the list of RAMs associated with the selected Target table.**Note:** Only published object-based RAMs with the inherent assessment option enabled are available for selection.

</td></tr><tr><td>

Approver type

</td><td>

Type of approver for the inherent assessment. The choices are as follows:-   User on target record
-   Group
**Note:** This field appears only when **Review for inherent assessment required** option is selected.

</td></tr><tr><td>

Approver

</td><td>

Approver for the inherent assessment. For a business application, the approver is the business owner of the application.**Note:** This field appears only when **User on target record** is selected from **Approver type**.

</td></tr><tr><td>

Approver group

</td><td>

Approver group for inherent assessment. This field appears only when the **Approver type** field has **Group**.**Note:** This field appears only when **Group** is selected from **Approver type**.

</td></tr><tr><td class="sub-head" colspan="2">

Recommendation Engine

</td></tr><tr><td colspan="2">

The Recommendation Engine section appears only when the **Target table** field has **Business Application**.

</td></tr><tr><td>

Recommendation engine algorithm

</td><td>

Specify the recommendation engine. The choices are as follows:-   None
-   Based on information object mapping
 For details on information objects, see [Information objects](../reference/information-objects.md).

</td></tr><tr><td class="sub-head" colspan="2">

Frequency

</td></tr><tr><td>

Frequency

</td><td>

Frequency of the reinitiation of the workflow. **Note:** The next run date of the reinitiation of the workflow is calculated based on the frequency defined in the risk integration configuration record. This frequency ensures continuous evaluation of the application.

</td></tr><tr><td>

Month

</td><td>

Month when the job must run.

</td></tr><tr><td>

Day of month

</td><td>

Day of the month when the job must run.

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  To define the RAM mapping for the risk identification configuration, do the following actions:

    1.  In the Risk Identification Configuration to RAM Mappings section, select **New**.

        The Risk Identification Configuration to RAM Mappings section appears only when **Entity class** is selected from **Configuration level**.

    2.  On the form, fill in the fields.

<table id="table_g54_k1n_21c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Risk identification configuration

</td><td>

Risk identification configuration for the RAM mapping. This field is automatically set to Risk identification configuration number.

</td></tr><tr><td>

Table

</td><td>

Table on which you want to define the RAM mapping.

</td></tr><tr><td>

Risk assessment methodology

</td><td>

Option to select the RAM to perform inherent assessment. You can see the list of RAMs associated with the selected table.**Note:** Only published object-based RAMs with the inherent assessment option enabled are available for selection.

</td></tr></tbody>
</table>    3.  Select **Submit**.

6.  Select **Publish** to publish the record.


**Parent Topic:**[Application risk assessment using Advanced Risk Assessment](../concept/risk-and-apm-better-together.md)

**Related topics**  


[Workflow of risk identification for business applications](../concept/workflow-risk-identification.md)

