---
title: Impact Rating record form
description: Use the Impact Rating record form to assess an impact category such as low, moderate, high, or critical by using BCM UIB Workspace.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure impact ratings, General administration setup for BCM, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Impact Rating record form

Use the Impact Rating record form to assess an impact category such as low, moderate, high, or critical by using BCM UIB Workspace.

## Impact Rating record form

For description of the field values, see the table.

<table id="table_tnn_1b4_nnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the impact rating.

</td></tr><tr><td>

Value

</td><td>

Numerical value for the impact rating. You can associate a unique numerical value to each impact rating. You cannot use the same value for any other impact rating in the BCM application.

 For example, you can assign value **1** to the **01-Low** impact category as shown below. After you do so, you cannot assign value **1** to any other impact rating in your BCM application instance.

 ![Impact Rating form showing the name, value description, and question text](../image/question-text.png)

</td></tr><tr><td>

Impact Category

</td><td>

Category of the impact. For example, Workforce impact, Regulatory impact, Revenue impact, and so on.

</td></tr><tr><td>

Impact analysis question

</td><td>

List of available impact analysis questions. This field is displayed if the impact category of the business disruption contributes to RPO.

</td></tr><tr><td>

Tolerable

</td><td>

Option for enabling the RTO impact as tolerable. This check box is displayed only if the impact category contributes to RTO.

</td></tr><tr><td>

Description

</td><td>

Short description about the impact rating.

</td></tr><tr><td>

Question text

</td><td>

Field to revise the question text. For the recovery time objective of an impact category, you can revise the question that is displayed in the RTO assessment questionnaire. You can navigate to the Impact Rating record as shown in the example:![Navigating to the Impact Rating record for an impact category.](../image/updating-question-text-field.png)Update the question text for the RTO assessment as shown in the example:

![Revising the question text.](../image/question-text.png)The revised question is then displayed in the RTO assessment of the business impact analysis record.

</td></tr></tbody>
</table>**Parent Topic:**[Configure impact ratings](../task/configure-impact-rating-uib-ws.md)

