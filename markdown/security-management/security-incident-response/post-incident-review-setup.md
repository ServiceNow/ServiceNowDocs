---
title: Configure an assessment trigger condition
description: Define rule conditions and generate required and optional assessments for specific security incidents.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage post incident activities, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure an assessment trigger condition

Define rule conditions and generate required and optional assessments for specific security incidents.

## Before you begin

Role required: sn\_si.admin

**Note:** To use the Post Incident Review Assessment Trigger Conditions feature, you must upgrade to Security Incident Response 11.0. Before upgrading, you must revert any customizations done to the Post Incident Review Metric type and trigger conditions. In addition, you may also have to revert the customizations done to the business rules specific to the post incident review.

-   Require assessments to be complete
-   Store assignee

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Administration** &gt; **Post Incident Review - Assessments Setup**.

2.  In the **Assessment Trigger Conditions Configure** section, select **Configure**.

    **Note:** On the Assessment Configurations form, and within the Assessments Configurations section, the **Generate assessments** check box is selected by default.

    -   When you select the check box, an optional assessment is created for every security incident.
    -   When you deselect the check box, the assessments are not generated. The assessment rules are not displayed and you cannot configure conditions for the security incidents.
3.  On the Assessment Configurations form, in the Conditions section, specify the required information.

    1.  In the **Name** field, specify the rule name.

    2.  In the **Fulfilment** field, specify the fulfilment type.

    3.  To configure a condition, select the rule record and define conditions in the **Condition** field.

        **Note:**

        -   If you create a rule without defining a condition in the **Condition** field, then the condition is evaluated as true and the rule is applicable for all security incidents.
        -   You can define a specific rule to make the assessments either mandatory or optional, and the assessments are not generated for the remaining security incidents, which don't match the defined rules.

