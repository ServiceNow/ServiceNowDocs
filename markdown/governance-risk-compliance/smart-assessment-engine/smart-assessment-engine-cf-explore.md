---
title: Exploring Smart Assessment Engine
description: The ServiceNowSmart Assessment Engine \(SAE\) helps you reduce the manual burden and costs of your assessment processes through automation.
locale: en-US
release: zurich
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Exploring Smart Assessment Engine

The ServiceNow®Smart Assessment Engine \(SAE\) helps you reduce the manual burden and costs of your assessment processes through automation.

## Smart Assessment Engine

In Governance, Risk, and Compliance \(GRC\) workflows such as compliance management, vendor risk management, privacy management, audit management, business continuity, and operational risk management, organizations face challenges in gathering input from employees and making informed decisions. Manual processes can be inefficient, time-consuming, and prone to errors, leading to increased operational costs and compliance risks.

SAE is designed to automate and optimize assessment processes, reducing manual efforts and costs. It provides an intuitive, configurable, and access-controlled assessment experience, enabling organizations to design and execute assessments seamlessly while ensuring compliance and efficiency. SAE is a versatile and business-friendly assessment engine that simplifies data collection, risk analysis, and compliance management. It supports a drag-and-drop template designer for effortless assessment creation and includes predefined roles to align with standard user personas. SAE ensures end-to-end workflow automation, post-assessment actions, and seamless collaboration.

By implementing SAE, organizations can streamline assessments, enhance accountability, and ensure regulatory compliance while optimizing overall efficiency. It enables organizations to track risks, maintain compliance, and improve decision-making through standardized evaluation processes.

## Smart Assessment Engine benefits

The following table shows the benefits of the Smart Assessment Engine application.

<table id="table_gsk_1b5_dyb"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Users

</th></tr></thead><tbody><tr><td>

See an overview of all your assessment template-related information. You can review the published and unpublished assessment templates and access the template designer.

</td><td>

[Accessing templates in the Assessment Workspace](sae-asmnt-workspace.md)

</td><td>

Template reader \[sn\_smart\_asmt.template\_reader\], Template manager \[sn\_smart\_asmt.template\_manager\], or Assessment admin \[sn\_smart\_asmt.assessment\_admin\]

</td></tr><tr><td>

Use the template designer for the following tasks:

 -   Create and customize the assessment templates that support a range of types including Control Attestation and Risk Identification.
-   Set the assessment parameters such as the question types, justifications, and conditional visibility.
-   Add the instructions, questions, and reference information by using the template designer.

</td><td>

[Using the template designer](sae-template-designer.md)

 [Create an assessment template](../task/sae-asmnt-template-create.md)

 [Add instructions and questions to an assessment template](../task/sae-asmnt-template-populate.md)

 [Add reference information to an assessment template](../task/sae-asmnt-add-reference.md)

</td><td>

Template manager \[sn\_smart\_asmt.template\_manager\] or Assessment admin \[sn\_smart\_asmt.assessment\_admin\]

</td></tr><tr><td>

Trigger assessments by using the Workflow Studio or scripts in Workflow Studio.

</td><td>

[Triggering assessments](sae-asmnt-triggering.md)

</td><td>

Flow designer \[flow\_designer\]

</td></tr><tr><td>

Respond to the assessments and collect the responses from within your workspace. As an assessor, your work is automatically saved, which eliminates the need for manual saving and helps to prevent data loss. You can also reassign the in-progress assessments to another user or cancel the assessments that are no longer needed.

</td><td>

[Responding to assessments](sae-respond-to-asmnt.md)

</td><td>

Assessment actor \[sn\_smart\_asmt.actor\]

</td></tr><tr><td>

Combine multiple assigned assessments into a single, streamlined view. You can manage, submit, or reassign these combined assessments at one time. Use Bulk Submit or Bulk Reassign assessments to handle all the assessments in one action.

</td><td>

[Submit combined assessments](../task/sae-asmnt-combine.md)

</td><td>

Assessment actor \[sn\_smart\_asmt.actor\]

</td></tr><tr><td>

Migrate the metric types to the SAE assessment templates to use the assessment designs that you already created.

</td><td>

[Migrate a legacy metric type to an assessment template](../task/sae-asmnt-tmplt-migrate-metrics-to.md)

</td><td>

Assessment admin \[sn\_smart\_asmt.assessment\_admin\]

</td></tr><tr><td>

Set up scoring for your assessment responses to calculate meaningful scores at the assessment, section, or subsection level.

</td><td>

[Scoring assessments](scoring-in-assessments.md)

</td><td>

sn\_smart\_asmt.template\_manager and sn\_smart\_asmt.assessment\_admin

</td></tr><tr><td>

Automate actions based on assessment responses. These actions use the responses from an assessment to automate tasks

</td><td>

[Post-assessment automations](impact-automation.md)

</td><td>

sn\_smart\_asmt.assessment\_admin or sn\_smart\_asmt.template\_manager and sn\_smart\_imp\_auto.automation\_creator

</td></tr></tbody>
</table>## Roles of SAE users

-   **Assessment actor**

    A user with the assessment actor \[sn\_smart\_asmt.actor\] role can respond to the assessments that are assigned to them. They can also reassign these assessments.

-   **Assessment reader**

    A user with the assessment reader \[sn\_smart\_asmt.assessment\_reader\] role can read the assessments within the categories that they’re assigned to. Additionally, they can read and comment on the assessments they created, and view and comment on the assessments that are generated from those templates.

    **Note:** The Assessment reader role field in the template determines the minimum user role that is required to view and comment on assessments. Only users with the specified role and the Assessment reader \[sn\_smart\_asmt.assessment\_reader\] role can access the assessments that are generated from this template.

-   **Assessment Admin**

    A user with the assessment admin \[sn\_smart\_asmt.assessment\_admin\] role can create, view, update, and delete both template categories and assessment templates. Additionally, the user with this role can view all the assessments, modify their states, reassign the assessments, and migrate the existing metric types to new assessment templates.

-   **Template reader**

    A user with the template reader \[sn\_smart\_asmt.template\_reader\] role can read specific assessment templates that are based on the categories mapped to the templates.

    **Note:** Each template must be mapped to one or more template category. A template reader must have this role to view the templates that are mapped with that category. A template reader must be able to access a template category to view the template.

-   **Template Manager**

    A user with the template manager \[sn\_smart\_asmt.template\_manager\] role can read, write, or create specific assessment templates that are based on the categories that are mapped to these templates. Their access to the template categories during the creation process is governed by the same rules that apply to the template readers.

-   **Template Developer**

    A user with the template admin or template manager role and template \[sn\_smart\_asmt.developer\] role can read, write, and create the script for response automation in assessment questions.


For more information, see [Roles in Smart Assessment Engine](../reference/sae-roles-defined.md).

