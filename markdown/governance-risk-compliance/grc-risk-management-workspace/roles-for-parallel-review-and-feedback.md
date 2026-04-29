---
title: Roles for Parallel Review and Feedback
description: When you integrate Parallel Review and Feedback with other applications, users must have the necessary roles to review records, capture feedback, and track the closure of feedback.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Parallel Review and Feedback in Advanced Risk, Use Risk Workspace, Risk Management, Governance, Risk, and Compliance]
---

# Roles for Parallel Review and Feedback

When you integrate Parallel Review and Feedback with other applications, users must have the necessary roles to review records, capture feedback, and track the closure of feedback.

The following roles have been introduced to enable users of other applications to use the Parallel Review and Feedback:

<table id="table_nvh_f2q_k1c"><thead><tr><th>

Role title \[name\]

</th><th>

Contained under

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_rvw\_feedback.admin

</td><td>

sn\_risk.admin

</td><td>

Users with this role can configure a feedback integration setup to define the table on which you want to use parallel review and feedback.

</td></tr><tr><td>

sn\_rvw\_feedback.reviewer

</td><td>

sn\_risk\_workspace.IT\_risk\_manager

 sn\_risk\_workspace.operational\_risk\_manager

</td><td>

Users with this role can create feedback on a record they're reviewing, suggesting overall improvements, or changes to specific fields in the record.

</td></tr><tr><td>

sn\_rvw\_feedback.respondent

</td><td>

sn\_risk\_workspace.business\_op\_risk\_manager

</td><td>

Users with this role can take necessary actions and provide comments or explanations regarding the submitted feedback.

</td></tr><tr><td>

sn\_rvw\_feedback.reader

</td><td>

sn\_risk.reader

</td><td>

Users with this role have read-access to feedback.

</td></tr></tbody>
</table>**Parent Topic:**[Parallel Review and Feedback in Advanced Risk](../concept/integrate-advanced-risk-with-parallel-review-feedback.md)

