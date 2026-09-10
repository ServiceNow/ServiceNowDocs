---
title: Assess the impact of a regulatory alert
description: Evaluate the risk of a regulatory alert by initiating either a risk assessment or a regulatory assessment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/regulatory-change-management-service-portal/impact-assessment-tasks.html
release: australia
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: task
last_updated: "2026-08-16"
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

1.  Navigate to **Workspaces** &gt; **Compliance Workspace**.

2.  Select the List icon \[Omitted image "ListsIcon.jpg"\] Alt text:.

3.  In the Lists tab, navigate to **Regulatory alerts** &gt; **All assigned alerts**.

4.  Select the regulatory alert that you want to assess.

5.  Select **Assess impact**.

6.  For **Regulatory assessment**, perform the following in the Evaluate regulatory impact dialog box.

    1.  In the **Assessment template** field, specify the template to use for the assessment.

    2.  In the **Select a group** field, select the group responsible to perform the assessment.

    3.  In the **Assessors** field, specify individual assessors of the group.

        Ensure that the assessors have the sn\_grc\_reg\_change.user or sn\_grc.business\_user roles granted.

    4.  In the **Due date** field, specify the due date for the assessment completion.

    5.  Select **Send**.

    In the Regulatory assessments related list in the regulatory alert record, the new regulatory assessments are listed.

7.  For **Risk assessment**, filter and select the entities to assess in the Evaluate risk impact dialog box.

    1.  In the **Filter by** dropdown, select one of the following options:

        -   **Entities by Impacted Areas**: Displays entities derived from impacted areas, including citations, control objectives, controls, policies, risk statements, and risks. These correspond to the records on the Impacted areas tab of the alert.
        -   **Entities by Recommendations**: Displays entities derived from AI-recommended impacted areas, including citations, control objectives, controls, and policies. These correspond to the records on the Recommendations tab of the alert.
    2.  Select the entities, and then, select **Send**.

        Ensure that the entity owners who are the risk assessors have the sn\_grc.business\_user and sn\_risk\_advanced.ara\_assessor roles.

        In the Risk assessments tab in the regulatory alert record, the new risk assessments are listed.


**Related topics**  


[Update a regulatory assessment template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/regulatory-change-management-service-portal/update-reg-assessment-template.md)

