---
title: Workflow of risk identification for business applications
description: When assessing an application for risks, the application goes through various stages of risk identification and assessment. You can define the identification and assessment workflow based on your requirements.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Application risk assessment using Advanced Risk Assessment, Integrate, Risk Management, Governance, Risk, and Compliance]
---

# Workflow of risk identification for business applications

When assessing an application for risks, the application goes through various stages of risk identification and assessment. You can define the identification and assessment workflow based on your requirements.

Before the risks of an application are assessed, the application must be created in the Business application table and brought to GRC. After the application comes to GRC, a risk identification record is created. The application owner provides information about the application to the IT Risk Manager. The IT Risk Manager then maps the recommended risks, citations, and policies.

Consider the following example to understand the workflow of risk identification and assessment for a business application. A new business application is introduced into your organization. This new application is a part of the Business Application table. The new application has two owners:

-   IT application owner
-   Business owner: This user must have the sn\_grc.business\_user role.

**Note:** Your organization can use different roles.

At this point, the application is not a part of GRC. It must be brought to GRC as an entity before its risks can be assessed. The new application must also have information objects associated with it.

The workflow and approvers of the application risk assessment are determined by the settings in the Risk Identification Configuration form. Refer to [Set up risk identification integration](../task/configure-risk-identification-form.md) to understand the process of defining the workflow. To reinitiate risk identification, a flow designer action is provided.

When assessing a new business application, the workflow of the risk identification is as follows:

1.  A business application is created either automatically or by an application owner in the business application table.
2.  GRC detects the new business application. A GRC entity is created for the new application. The detection is handled by the GRC Profile Generation scheduled job that runs in the background.
3.  A new risk identification record is created for the application.

    **Note:** The Risk Manager can modify the configuration record and determine the workflow of the assessment. After a risk identification configuration is published, the risk manager can modify only some fields in the configuration record.

4.  A questionnaire is initiated and sent to the application owner to collect details about the application.
5.  The application owner responds to the questionnaire.
6.  The IT Risk Manager reviews the responses. If the responses are unsatisfactory, the manager sends the questionnaire back to the application owner.

    **Note:** If the questionnaire is sent back, then the new responses are reverted to their original form.

7.  Based on the configuration, after the IT Risk Manager is satisfied with the responses, the system initiates the inherent assessment.
8.  GRC maps the risks and compliance objects based on the entity types.
9.  The IT Risk Manager reviews the information object mapping.
10. The system executes the recommendation engine based on the algorithm selected in the configuration.
11. The IT Risk Manager reviews and maps the recommended risks, policies, and citations based on the associated information objects.
12. The IT Risk Manager maps the recommended controls based on associated citations, policies, and risks.
13. The application owner manages the control life cycle and attests the controls.

The following figure represents the workflow of the solution.

![Integration of APM and Advanced Risk Assessment](../image/updated-apm-and-risk-workflow.png "Solution workflow of the GRC and APM integration")

## States of the risk identification record

After the risk identification configuration moves to the Published state, a risk identification record gets created for the related entity.

The risk identification record moves through the following states:

-   New: A new record is created
-   Information Gathering: The information about the application is collected.
-   Review: The Risk Manager reviews the information.
-   Inherent Assessment: The Risk Manager performs inherent risk assessment.
-   Risk Mapping: The Risk Manager maps the necessary risks, citations, and policies.
-   Monitor: The risks are monitored.
-   Retired: The risks are retired as necessary.

After the risk identification configuration moves to the Retired state, the configuration becomes invalid and risk identification records are not created for related entities.

In terms of its life cycle, a risk identification record goes through the following states:

1.  New
2.  Information Gathering
3.  Review
4.  Inherent Assessment
5.  Risk Mapping
6.  Monitor
7.  Retired

**Parent Topic:**[Application risk assessment using Advanced Risk Assessment](risk-and-apm-better-together.md)

