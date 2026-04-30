---
title: Create a questionnaire or document request template
description: You can reuse questionnaire templates and document-request templates to speed up the creation of new questionnaires and document requests.
locale: en-US
release: yokohama
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Classic assessments, Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Create a questionnaire or document request template

You can reuse questionnaire templates and document-request templates to speed up the creation of new questionnaires and document requests.

## Before you begin

Role required: admin or sn\_vdr\_risk\_asmt.vendor\_risk\_admin

## About this task

When defining a template, you specify whether questionnaires or document requests should require electronic signatures for the third party, the reviewer, or both as mandated by your organization's rules or federal regulations. See the following optional steps for information about copying existing questionnaire templates.

<table id="id_bxz_wwv_szb"><thead><tr><th>

Term

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Metric or Assessment metric

</td><td>

A single question within a questionnaire template.

</td></tr><tr><td>

Metric type or Assessment metric type

</td><td>

A questionnaire template.

</td></tr><tr><td>

Category or Assessment category

</td><td>

A set of related questions within a questionnaire template.**Note:** There can be multiple categories within a metric type.

</td></tr></tbody>
</table>**Note:** A questionnaire template must have at least one category. Each category must contain at least one question.

## Procedure

1.  Navigate to one of the following locations:

    -   **All** &gt; **Third-party Risk Management** &gt; **Assessment setup** &gt; **Questionnaire Templates** or **Third-party Risk Management** &gt; **Assessment Setup** &gt; **Document Request Templates**.
    -   **Workspaces** &gt; **Vendor Management Workspace**, select the list icon ![](../../grc-workspace-vrm/image/ws-list-icon.png) and then navigate to **Assessment setup** &gt; **Questionnaire Templates**.
2.  Complete one of the following options to create a new template or copy an existing template.

<table id="choicetable_ctx_vmr_g2c"><thead><tr><th align="left" id="d252389e205">

Option

</th><th align="left" id="d252389e208">

Description

</th></tr></thead><tbody><tr><td id="d252389e214">

**Create a new template**

</td><td>

1.  Select **New** and then fill in the form.

For descriptions of all these fields, see [Assessment metric type form](../reference/tprm-create-q-template-form.md).

2.  Select **Submit**

Any other templates associated with this template are shown as related links or tabs.

**Note:** After saving your questionnaire or document request template, you can select the Edit in Designer related link to make additional edits using the designer.

.

</td></tr><tr><td id="d252389e254">

**Copy and customize an existing template**

</td><td>

1.  Open an existing questionnaire template by selecting the one you want from the Assessment Metric Types table.
2.  Select **Copy** and make any necessary updates.

A copy of the questionnaire template has been created and is shown in the Assessment Metric Types table.

</td></tr></tbody>
</table>
**Related topics**  


[Create an external assessment](tprm-create-assessment.md)

[Assessing your third-party risk](../concept/tprm-assessing-tpr.md)

[Create an issue generation rule](tprm-generate-issue-rule.md)

