---
title: Roles for performing advanced risk assessment
description: When you integrate advanced risk assessment with other applications, you must ensure the users have the necessary roles to perform and approve the assessments.
locale: en-US
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Components installed with Advanced Risk, Reference, Risk Management, Governance, Risk, and Compliance]
---

# Roles for performing advanced risk assessment

When you integrate advanced risk assessment with other applications, you must ensure the users have the necessary roles to perform and approve the assessments.

Starting with version 14.1.2, several new roles have been introduced to enable users of other applications to successfully use the advanced risk assessments feature. These independent roles have been created to provide the users the required ability to perform advanced risk assessment without requiring the Integrated Risk Management specific roles such as Risk Admin, GRC Business User.

**Note:** You must manually assign the advanced risk assessment roles to the sn\_grc.business\_user role. To understand how you can adjust granting of roles and groups, see the [How to adjust granting of roles and groups to use background jobs \[KB0963693\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0963693) article in the Now Support Knowledge Base. To understand more about the GRC business user role, see the [GRC Business User \[KB0864247\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0864247) article in the Now Support Knowledge Base article in the Now Support Knowledge Base. You must log in to Now Support to view the article.

<table id="table_gtf_wpk_qjb"><thead><tr><th>

Role title \[name\]

</th><th>

Contained under

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_risk\_advanced.ara\_admin

</td><td>

sn\_risk.admin

</td><td>

Users with this role can:-   Create risk assessment methodologies
-   Create and manage factors

</td><td>

-   sn\_risk\_advanced.ara\_creator
-   sn\_risk\_advanced.ara\_assessor
-   sn\_risk\_advanced.ara\_approver
-   sn\_risk\_advanced.ara\_reader

</td></tr><tr><td>

sn\_risk\_advanced.ara\_creator

</td><td>

sn\_risk.user

</td><td>

Users with this role can create object assessments.

</td><td>

sn\_risk\_advanced.ara\_reader

</td></tr><tr><td>

sn\_risk\_advanced.ara\_assessor

</td><td>

sn\_grc.business.user

</td><td>

Users with role can:-   Take assessments
-   Perform assessment related actions such as taking the assessment and responding to or reassigning the assessment

</td><td>

sn\_risk\_advanced.ara\_reader

</td></tr><tr><td>

sn\_risk\_advanced.ara\_approver

</td><td>

sn\_grc.business.user

</td><td>

Users with role can perform assessment related actions such as approving the assessment.

</td><td>

sn\_risk\_advanced.ara\_reader

</td></tr><tr><td>

sn\_risk\_advanced.ara\_reader

</td><td>

sn\_risk.reader

</td><td>

Users with role can read all the information on a risk assessment instance. Users with this role have read access to all tables within advanced risk assessment. If there are users who only need to have access to reports, they can use this role.

</td><td>

 

</td></tr><tr><td>

sn\_risk\_advanced.qualitative\_risk\_appetite\_reader

</td><td>

sn\_risk.user

 sn\_risk.reader

</td><td>

Users can view the qualitative risk appetite fields.

</td><td>

 

</td></tr><tr><td>

sn\_risk\_advanced.quantitative\_risk\_appetite\_reader

</td><td>

sn\_risk.user

</td><td>

Users can view the quantitative risk appetite fields.

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with Advanced Risk](components-risk-advanced.md)

