---
title: Define third-party risk scoring rules
description: Define criteria, based on risk scores, that determine which third parties require assessments. Third-party risk scoring rules apply to subsidiaries and engagements and to third-party risk areas.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Classic assessments, Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Define third-party risk scoring rules

Define criteria, based on risk scores, that determine which third parties require assessments. Third-party risk scoring rules apply to subsidiaries and engagements and to third-party risk areas.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager

## Procedure

1.  Navigate to **All** &gt; **Third-party Risk Management** &gt; **Scoring Setup** &gt; **Third-party Risk Scoring Rules**.

2.  Select **New**, fill in the form, and then select **Submit**.

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

Description of the scoring rule that will help other users understand its intent.

</td></tr><tr><td>

Number

</td><td>

For each third-party risk scoring rule, the system auto-assigns a unique ID number that starts with the text VRS.The unique ID is used in all references to the item. You can use the ID to search or filter for the item that you want to work on.

</td></tr><tr><td>

Third-party risk area criteria

</td><td>

The risk area criteria that applies to this engagement risk scoring rule.

 A third-party risk area criteria is a group of risk domains \(sometimes called risk areas in other platform features\) that applies to a particular type of third party. See [Define third-party risk area criteria](tprm-risk-domain-criteria-df.md) for details on how the criteria are defined.

</td></tr><tr><td>

Third-party risk component criteria

</td><td>

Criteria for third-party risk assessments, engagements, and subsidiaries that applies to this risk scoring rule.

 Components are the entities for which you can assess risk \(for example, subsidiaries or engagements\). A component criteria is a group of components that should apply to a particular type of third party or engagement.

 See [Define component criteria](tprm-component-criteria-define.md).

</td></tr><tr><td>

Active

</td><td>

Option to activate the rule. Only active rules are applied.

</td></tr><tr><td>

Order

</td><td>

Select the order to indicate the rule's precedence. If multiple rules apply to the same third-party risk area, engagement, or subsidiary, the one with the higher-order value is applied.

</td></tr><tr><td>

Vendor filter

</td><td>

Use the [condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) to define the rules for selecting third parties. For example, you can filter on third parties with whom you do considerable business \(Size is $1,000,000\) or third parties within a specific category \(Category is software\).

</td></tr></tbody>
</table>    ![New third-party risk scoring rule.](../image/new-vendor-risk-scoring-rule.png)


