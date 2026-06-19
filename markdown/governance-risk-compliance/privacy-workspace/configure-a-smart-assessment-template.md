---
title: Configure smart assessment templates for screening assessments
description: Create a privacy assessment template using the Smart Assessment Engine as a base for sending screening assessments and use it to detect the privacy risks and mitigate those risks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/privacy-workspace/configure-a-smart-assessment-template.html
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Privacy Management, Governance, Risk, and Compliance]
---

# Configure smart assessment templates for screening assessments

Create a privacy assessment template using the Smart Assessment Engine as a base for sending screening assessments and use it to detect the privacy risks and mitigate those risks.

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
Select **Initial Assessment**.

</td></tr><tr><td>

Description

</td><td>

Description of the assessment. This description is displayed to the responder during the assessment.

</td></tr><tr><td>

All information object categories

</td><td>

Option to display either all the information object categories or a subset of the information object categories during the assessment.**Note:** This option is applicable if you add the **Data elements** subsection that is not part of the screening assessment.

</td></tr><tr><td>

State model

</td><td>

State model of the assessment. This field is automatically set to **Privacy assessment task model**.

</td></tr><tr><td>

Information object categories

</td><td>

Information object categories to display during the assessment. **Note:** This field only appears when the **All information object categories** option is not selected. This field is applicable if you add the **Data elements** subsection that is not part of the screening assessment.

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

    A new tab titled Sections appears that contains the questionnaire that is fetched from the Smart Assessment Engine.


## What to do next

Publish a new version of the template to revise a published template without disrupting in-progress assessments.

The Smart Assessment Engine uses one published version of a template at a time. When you publish a new version, the prior version is retired and no new assessments can be sent against it.

**Note:** Assessments already in Draft, Assigned, or Work in progress state continue against the version they were created with.

To create a version of an existing template, see [Create a version of a privacy assessment template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/create-new-smart-asmt-version.md).

**Parent Topic:**[Configuring Privacy Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/configure-privacy-mgmt.md)

