---
title: Feedback integration configuration form
description: Use the Feedback integration configuration form to define a setup for the Parallel Review and Feedback.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure a feedback integration, Parallel Review and Feedback in Advanced Risk, Use Risk Workspace, Risk Management, Governance, Risk, and Compliance]
---

# Feedback integration configuration form

Use the Feedback integration configuration form to define a setup for the Parallel Review and Feedback.

See the following table for a description of the field values.

<table id="table_l35_zwl_kkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Name of the table to integrate review and feedback. For example, if you want to provide feedback on the risk event records, you must select the sn\_risk\_advanced\_event table.

</td></tr><tr><td>

Reviewer group

</td><td>

Reviewer group who can provide feedback on the selected table records.

</td></tr><tr><td>

Active

</td><td>

State of the feedback integration configuration. Only active configurations can be considered to provide feedback on the selected table records.

</td></tr><tr><td>

Workspace URL path

</td><td>

Workspace URL path to send feedback-related notifications to a particular workspace. For example, to use it on the Risk Workspace, select `risk/risk`.

</td></tr><tr><td class="sub-head" colspan="2">

Respondent

</td></tr><tr><td>

Respondent type

</td><td>

Respondent who can respond to the raised feedback on the selected table records. The options are as follows:-   **User on target record**: Individual who can respond to the feedback.
-   **Group on target record**: Group of users who can respond to the feedback.
-   **Specific group**: Specific group who can respond to the feedback when the target record doesn't have a user or group. You can see only those groups that are assigned with the sn\_rvw\_feedback.respondent role.

</td></tr><tr><td>

Respondent field

</td><td>

User or group field on the target record. For example, if you want the record owner to respond to the raised feedback, select `Owner` in this field.

</td></tr></tbody>
</table>**Parent Topic:**[Configure a feedback integration](../task/configure-feedback-integration.md)

