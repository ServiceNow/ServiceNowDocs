---
title: Assess the impact of a regulatory alert
description: Evaluate the risk of a regulatory alert by initiating either a risk assessment or a regulatory assessment.
locale: en-US
release: yokohama
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage regulatory tasks, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Assess the impact of a regulatory alert

Evaluate the risk of a regulatory alert by initiating either a risk assessment or a regulatory assessment.

## Before you begin

Role required: sn\_grc\_reg\_change.user

## About this task

You can initiate one of the following assessments:

-   Regulatory assessment: Uses the Smart Assessment Engine. A regulatory assessment is used to assess the potential effects of new or updated regulations before the regulations are finalized or implemented.
-   Risk assessment: Uses the classic risk assessment. A risk-based approach is used to identify and address both direct and indirect impacts.

## Procedure

1.  Navigate to **All** &gt; **Regulatory Change Management** &gt; **Compliance Workspace** &gt; **Lists** &gt; **Regulatory Alerts**.

2.  Select the regulatory alert that you want to assess.

3.  Select **Assess impact**.

4.  Select either **Regulatory assessment** or **Risk assessment** based on your requirement.

5.  If you select, Regulatory assessment, do the following in the Evaluate regulatory impact dialog box.

    1.  In the **Assessment template** field, specify the template to use for the assessment.

    2.  In the **Select a group** field, select the group responsible to perform the assessment.

    3.  In the **Assessors** field, specify individual assessors of the group.

        Ensure that the assessors have the sn\_grc\_reg\_change.user or sn\_grc.business\_user roles granted.

    4.  In the **Due date** field, specify the due date for the assessment completion.

    5.  Select **Send**.

    In the Regulatory assessments related list in the regulatory alert record, the new regulatory assessments are listed.

6.  If you select, Risk assessment, from the Entities list, select the entities that require an impact assessment.

    1.  Select **Send**.

        Ensure that the entity owners who are the risk assessors have the sn\_risk\_advanced.ara\_assessor role.

        In the Risk assessments related list in the regulatory alert record, the new impact assessments are listed.


