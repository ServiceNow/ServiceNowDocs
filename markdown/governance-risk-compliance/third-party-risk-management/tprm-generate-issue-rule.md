---
title: Create an issue generation rule
description: Create an issue generation rule that will automatically create an issue based on question responses to external assessments. Issues help ensure that your concerns about a third party or engagement are remediated.
locale: en-US
release: xanadu
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Classic assessments, Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Create an issue generation rule

Create an issue generation rule that will automatically create an issue based on question responses to external assessments. Issues help ensure that your concerns about a third party or engagement are remediated.

## Before you begin

Role required: admin or sn\_vdr\_risk\_asmt.vendor\_risk\_admin

## About this task

In an iterative process, before the TPR manager closes an assessment, the TPR manager can generate non-compliance issues and tasks. The TPR manager communicates with the TP contacts and engagement contacts by using comments to close the issues and tasks. The TPR manager can also assign different contacts as needed.

## Procedure

1.  Navigate to **All** &gt; **Third-party Risk Management** &gt; **Issues** &gt; **Issue Generation Rules** or **Workspaces** &gt; **Vendor Management Workspace**, select the list icon ![](../../grc-workspace-vrm/image/ws-list-icon.png), and then navigate to **Assessment setup** &gt; **Issue Generation Rules**.

2.  Create an issue generation rule by selecting **New** and fill in the form.

<table id="table_krg_p53_2yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name or short description of the rule.

</td></tr><tr><td>

Issue template

</td><td>

Issue template that is used when generating the issue.

</td></tr><tr><td>

Task template

</td><td>

Task template that is used after generating the issue.

</td></tr><tr><td>

Active

</td><td>

Option that activates the issue generation rule for assessments and questions.

</td></tr><tr><td>

Supports smart assessment

</td><td>

Option that indicates that the Issue generation rule can be used with the Smart Assessment Engine.**Note:** For existing rules, this option isn’t set when there are classic questionnaire and document request templates that haven’t been migrated and published. This option is set automatically when an SAE questionnaire or document request template has been added manually.

When you create a new rule template and have the Smart Assessment Engine property enabled, this field is selected by default after saving the template.

</td></tr><tr><td class="sub-head" colspan="2">

**Questions**

</td></tr><tr><td>

Questionnaire template

</td><td>

Questionnaire template that the rule applies to.

</td></tr><tr><td>

Questions

</td><td>

Questions that generate issues based on their responses.

</td></tr><tr><td class="sub-head" colspan="2">

**SAE Questions**

</td></tr><tr><td>

Questionnaire template

</td><td>

Questionnaire template that the rule applies to.

</td></tr><tr><td>

Questions

</td><td>

Questions that generate issues based on their responses.

</td></tr></tbody>
</table>3.  Select **Submit**.


## Result

After the TPR assessor moves the state of the assessment to the Generating Observations state, issues will generate based on these rules.

The TPR assessor can navigate to the Issues tab of the External assessment in the Vendor Management Workspace to view generated issues.

**Related topics**  


[Assessing your third-party risk](../concept/tprm-assessing-tpr.md)

[Create an issue for a third party or engagement](tprm-ws-issue-create.md)

