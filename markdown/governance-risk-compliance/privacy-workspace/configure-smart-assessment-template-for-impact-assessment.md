---
title: Configure smart assessment templates for impact assessments
description: Create privacy assessment templates using the Smart Assessment Engine as a base for sending privacy impact assessments and using them to detect the privacy risks and mitigate those risks.
locale: en-US
release: yokohama
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Privacy Management, Governance, Risk, and Compliance]
---

# Configure smart assessment templates for impact assessments

Create privacy assessment templates using the Smart Assessment Engine as a base for sending privacy impact assessments and using them to detect the privacy risks and mitigate those risks.

## Before you begin

Role required: sn\_privacy.admin

## Procedure

1.  Navigate to **All** &gt; **Privacy Management** &gt; **Privacy Workspace** &gt; **Lists** &gt; **Configure privacy management** &gt; **Assessment template configuration**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_a3j_zhx_ydc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the configuration. For example, `Privacy Screening Assessment Configuration`.

</td></tr><tr><td>

Smart assessment template

</td><td>

Smart assessment template for which you're adding the configurations.**Note:** A template can be mapped to only one classification.

</td></tr><tr><td>

Classification

</td><td>

Logical grouping of the template. The choices are as follows.-   **Initial Assessment**
-   **Privacy Impact Assessment**
Select **Privacy Impact Assessment**.

</td></tr><tr><td>

Description

</td><td>

Description of the assessment. This description is displayed to the responder during the assessment.

</td></tr><tr><td>

All information object categories

</td><td>

Option to display either all the information object categories or a subset of the information object categories.**Note:** This option is useful only when you have configured the **Data elements** subsection under the **Personal data section**.

</td></tr><tr><td>

State model

</td><td>

State model of the assessment. This field is automatically set to **Privacy assessment task model**.

</td></tr><tr><td>

Information object categories

</td><td>

Information object categories to display during the assessment. **Note:** This field only appears when the **All information object categories** option is not selected.

</td></tr><tr><td>

Active

</td><td>

Option to indicate if the configuration is active.

</td></tr><tr><td>

Functional domain

</td><td>

Domain of the configuration. When accessed from the Privacy Workspace, this field is automatically set.

</td></tr></tbody>
</table>4.  Select **Save**.

    A new tab titled **Sections** appears that contains the questionnaire that is fetched from the Smart Assessment Engine.

5.  Select **Add**.

    1.  Select **Personal data**.

    2.  Select **Add**.

    The Sections tab now displays two sections: Personal data and Questionnaire. You can modify the label and the description of the personal data section and these will be visible to the responder on the assessment page.

6.  Select **Save**.

7.  To add subsections to a section, open the section for which you want to add subsections.

    1.  Select **Subsections**.

    2.  Select **Add**.

    3.  Select the subsections to add.

    4.  Select **Add**.

    For example, for the Personal data section, you can add Data elements, Data subject types, Hierarchy, and Legal basis. The details in the **Guidance** field of the subsections appear during the assessment to help the responder understand the questions in the assessment.


**Parent Topic:**[Configuring Privacy Management](../concept/configure-privacy-mgmt.md)

