---
title: Vulnerability Type form
description: On the Vulnerability Type form, fill in the fields for Operational vulnerability.
locale: en-US
release: zurich
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up the Operational vulnerability type, Setting up the Operational vulnerability module, Completing general administrative tasks, Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Vulnerability Type form

On the Vulnerability Type form, fill in the fields for Operational vulnerability.

<table id="table_uj1_q5x_nvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Label for the vulnerability type record.

</td></tr><tr><td>

Name

</td><td>

Name of the vulnerability type. For example, vulnerability\_type.

</td></tr><tr><td>

Category

</td><td>

Category of the vulnerability type. For example, Operational vulnerability \[sn\_oper\_res\_vulnerability\].

</td></tr><tr><td>

Description

</td><td>

Description of the vulnerability type.

</td></tr><tr><td>

Active

</td><td>

Option to activate the vulnerability type.

</td></tr><tr><td class="sub-head" colspan="2">

State Model

</td></tr><tr><td>

State Model

</td><td>

Vulnerability state model. The state model and action task state model specify the workflow states and transition conditions for a record type and an action task, respectively.

</td></tr><tr><td>

Action task state Model

</td><td>

Action task model. A record type and an action task follow the workflow states configured in their respective state models.

</td></tr><tr><td class="sub-head" colspan="2">

Assessment Configuration

</td></tr><tr><td>

Assessment templates

</td><td>

Pre-defined formats to request responses from assessors or reviewers that help to evaluate the record. You can use one or multiple assessment templates and use them in the action tasks. Use the Smart Assessment template that has been added to the vulnerability type.

</td></tr><tr><td class="sub-head" colspan="2">

Template Configuration

</td></tr><tr><td>

Document templates

</td><td>

Pre-defined formats to generate the PDF of the vulnerability record.

</td></tr><tr><td class="sub-head" colspan="2">

Related lists

</td></tr><tr><td>

Subtypes

</td><td>

Sub-type of vulnerability type record. For example, **Documentation Loss**.

</td></tr><tr><td>

View Rules

</td><td>

Rules to define the form view of the vulnerabilities in the Operational Resilience Workspace. Specifying the rules helps you to define the view you want to use for the vulnerabilities and control how the vulnerability form appears. For example, Default view or Workspace view.

![View rules.](../image/view-rules.png)

</td></tr><tr><td>

Assignment Rules

</td><td>

Rules to assign the tasks to users and groups by default.

**Note:** Assignment rules apply only when the operational vulnerability is created from the Employee Center. Otherwise, they do not apply.

In the Applies to related list, you can select a table and specify the conditions that must be met before the task is assigned to the user or group. The rule is applied only if the task is not already assigned to another user or group. In the Script related list, you can use a script to further customize the assignment rule.

![Assignment rule.](../image/assignment-rules.png)

</td></tr><tr><td>

Jurisdiction

</td><td>

Jurisdictions for the impacted regions.**Note:** Jurisdictions are not currently supported in Operational vulnerability.

</td></tr></tbody>
</table>