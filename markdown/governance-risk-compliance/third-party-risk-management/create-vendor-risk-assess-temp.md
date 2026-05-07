---
title: Create an external assessment template
description: When defining an assessment template, the third-party risk manager provides scheduling information for the third-party risk assessment.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 3
breadcrumb: [Classic assessments, Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Create an external assessment template

When defining an assessment template, the third-party risk manager provides scheduling information for the third-party risk assessment.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager

## About this task

As part of an assessment, the TPR manager can send multiple questionnaires and document requests by using assessment templates. The TPR admin first defines the required questionnaire templates and document request templates and then the TPR managers groups them into an assessment template. The TPR manager can use the resulting assessment template to send the appropriate questionnaires, document requests, or both in future assessments.

**Note:**

When you create a new assessment template and have the Smart Assessment Engine property enabled, the Supports smart assessment option is selected by default after saving the template.

For existing assessments, the Supports smart assessment option is set automatically when all Classic engine templates have been removed. You can add associated questionnaire and document request templates that have been migrated to and published in the Smart Assessment Engine.

## Procedure

1.  Navigate to one of the following locations:

    -   **All** &gt; **Third-party Risk Management** &gt; **Assessment setup** &gt; **External Assessment Templates**.
    -   **Workspaces** &gt; **Vendor Management Workspace**, select the list icon ![](../../grc-cam-workspace/image/ws-list-icon.png) and then navigate to **Assessment setup** &gt; **External assessment templates**.
2.  Select **New**.

3.  On the form, fill in the fields.

    For more information about the field descriptions, see [Create new external assessment template form](../reference/create-assess-template-form.md).

4.  Select **Submit**.

5.  Add a questionnaire or document request template to the assessment template using one of the following methods.

<table id="choicetable_rkc_13z_hcc"><thead><tr><th align="left" id="d102897e161">

Option

</th><th align="left" id="d102897e164">

Description

</th></tr></thead><tbody><tr><td id="d102897e170">

**Add Questionnaire templates**

</td><td>

1.  In the Classic UI, navigate to the Questionnaire templates related list, select **Edit**, and add the questionnaire template you want.

In the Vendor Management Workspace, navigate to the Questionnaire templates related list and select **Add** to add the questionnaire template you want.

2.  Select **Save**.


</td></tr><tr><td id="d102897e206">

**Add Document request templates**

</td><td>

1.  In the Classic UI, navigate to the Document request templates related list, select **Edit**, and add the document request template you want.

In the Vendor Management Workspace, navigate to the Document request templates related list, and select **Add** to add the document request template you want.

2.  Select **Save**.


</td></tr><tr><td id="d102897e242">

**Add SAE Questionnaire templates**

</td><td>

1.  In the Classic UI, navigate to the SAE Questionnaire templates related list, select **Edit**, and add the SAE questionnaire template you want.

In the Vendor Management Workspace, navigate to the SAE Questionnaire templates related list, and select **Add** to add the SAE questionnaire template you want.

2.  Select **Save**.


</td></tr><tr><td id="d102897e290">

**Add SAE Document templates**

</td><td>

1.  In the Classic UI, navigate to the SAE Document request templates related list, select **Edit**, and add the SAE Document request template you want.

In the Vendor Management Workspace, navigate to the SAE Document request templates related list, and select **Add** to add the SAE Document request template you want.

2.  Select **Save**.


</td></tr></tbody>
</table>    The assessment template is ready to be used.


**Related topics**  


[Create a questionnaire or document request template](create-questionnaire-template.md)

[Create a questionnaire or document request template using the Designer](create-question-template.md)

[Create a TPRM SAE questionnaire or document request template](create-sae-q-template.md)

