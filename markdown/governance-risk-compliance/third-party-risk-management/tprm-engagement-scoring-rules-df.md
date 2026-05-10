---
title: Define engagement risk scoring rules
description: An engagement risk-scoring rule specifies component criteria that determine which engagements are selected for assessment. For example, a rule could enable assessments for engagements that involve more than $40,000 annual business. Engagement scoring rules apply only to engagements.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Classic assessments, Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Define engagement risk scoring rules

An engagement risk-scoring rule specifies component criteria that determine which engagements are selected for assessment. For example, a rule could enable assessments for engagements that involve more than $40,000 annual business. Engagement scoring rules apply only to engagements.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager

## About this task

**Important:** Engagement risk scoring rules apply only to engagements and not to parent third parties. Engagement risk rating scores, therefore, apply only to risk assessments for the engagement.

## Procedure

1.  Navigate to **All** &gt; **Third-party Risk Management** &gt; **Scoring Setup** &gt; **Engagement Risk Scoring Rules**.

    ![List of engagement risk scoring rules.](../image/engagement-risk-scoring-rules.png)

2.  Select **New**, fill in the form, and then select **Submit**.

    ![Engagement Risk Scoring Rule — New.](../image/risk-engage-scoring-rule.png)

<table id="table_eng-scoring-rule"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the scoring rule.

</td></tr><tr><td>

Description

</td><td>

Description of the scoring rule.

</td></tr><tr><td>

Number

</td><td>

For each engagement risk scoring rule, the system auto-assigns a unique ID number that starts with the text ERS.The unique ID is used in all references to the item. You can use the ID to search or filter for the item that you want to work on.

</td></tr><tr><td>

Third-party risk area criteria

</td><td>

The third-party risk area criteria that applies to this engagement risk scoring rule.

 A third-party risk area criteria is a group of risk domains \(sometimes called risk areas in other platform features\) that applies to a particular type of third party. See [Define third-party risk area criteria](tprm-risk-domain-criteria-df.md) for details on how criteria are defined.

</td></tr><tr><td>

Engagement risk component criteria

</td><td>

The engagement risk component criteria that applies to this engagement risk scoring rule. Components are the entities for which you can assess risk \(for example, subsidiaries or engagements\). A component criteria is a group of components that should apply to a particular type of third party or engagement.

</td></tr><tr><td>

Active

</td><td>

Option to activate the rule. Only active rules are applied to engagements.

</td></tr><tr><td>

Order

</td><td>

Specify the order to indicate the rule's precedence. If multiple rules apply to the same engagement, the one with the higher-order value is applied.

</td></tr><tr><td>

Engagement Filter

</td><td>

Criteria for selecting engagements.

 Use the [condition builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_ConditionBuilder.md) to define the criteria.

 For example, you can perform assessments for third parties with whom you do considerable business: `Annual spend is greater than $40,000` or third parties within a particular category: `Category is software`.

</td></tr></tbody>
</table>
