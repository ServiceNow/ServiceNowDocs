---
title: Assess demands with smart assessments
description: Smart assessments automatically gather structured, weighted feedback from a demand's stakeholders and scores the demand. Demand managers can qualify demands offhand and track every assessment from a single place.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/strategic-planning/smart-assessments-overview.html
release: brazil
product: Strategic Planning
classification: strategic-planning
topic_type: concept
last_updated: "2026-09-24"
reading_time_minutes: 6
keywords: [smart assessments, demand assessment, demand workspace]
breadcrumb: [Use, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Assess demands with smart assessments

Smart assessments automatically gather structured, weighted feedback from a demand's stakeholders and scores the demand. Demand managers can qualify demands offhand and track every assessment from a single place.

Smart assessments replaces the manual assessment instances and assessment results workflow with an assessment workflow that runs automatically. Assessments are created, scored, and used to qualify the demand automatically, so demand managers no longer need to create an assessment or review its results manually.

When a demand moves from the Submitted to Screening state, an assessment is triggered for the demand's stakeholders who are added to the demand to be assessed.

If the demand does not require an assessment at all, it skips the assessments and moves directly to the Qualified state.

After every open assessment for the demand is completed or cancelled, the demand moves automatically to Qualified, and the individual section scores populate onto the demand. Apart from each assessment's own score, the demand's own **Score** field is calculated as the average of Risk, Size, and Value sections. Risk and size scores are inverted, so a lower risk or size score raises the demand's score. For more information, see [Demand assessment template questions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/strategic-planning/smart-assessments-overview.md). Strategic Alignment and Cost sections populate onto the demand but aren't part of this calculation.

## Benefits of smart assessments

-   Enhanced assessment experience with a cleaner, more intuitive assessment form for stakeholders.
-   Supports text-based questions for the assessments.
-   Supports viewing of assessment results after filling.
-   Supports a single view for all assessments assigned to you.

## Enabling smart assessments

Smart assessments is controlled by the **sn\_align\_ws.enable\_smart\_assessments** system property, which ships as inactive \(`false`\) by default. When the property is set to false, demands continue to use the classic assessments.

When an administrator sets the property to true:

-   Every newly created demand, and any demand currently in Draft or Submitted state, routes through smart assessments.
-   A demand that already has an assessment instance triggered under the old workflow continues and completes using that same workflow. This applies as long as the demand isn't reset to Draft. For more information, see [Deleting or resetting a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/strategic-planning/smart-assessments-overview.md).
-   After the property is set to true, continue using the smart assessments for a demand over the classic assessments.

## Smart assessment users

Smart assessment access works at three levels. The first is a top-level admin role that spans every template category. The second is a set of roles scoped to an individual template category. The third is template-level roles that control who can fill in or read an individual assessment. None of the category-level or top-level roles are assigned to any role automatically. You can decide who to assign them to, based on who should manage assessment templates in your instance.

|User|Description|
|----|-----------|
|Assessment admin \(sn\_smart\_asmt.assessment\_admin\)|Can access and edit templates in every template category. Not assigned to any role by default. You can assign it to whichever user you choose.|
|Template manager \(sn\_smart\_asmt.template\_manager\)|Can create and modify templates within a template category this user otherwise has access to. Not assigned to any role by default. You can assign it to whichever user you choose, such as an APW admin user.|
|Assessment actor \(sn\_smart\_asmt.actor\)|Stakeholders for the demand who fill in the smart assessments they're assigned. Separate assignment is required for each stakeholder by the admin.|
|Assessment reader \(sn\_smart\_asmt.assessment\_reader\)|Demand managers who read smart assessments and their results on demands they manage. Contained automatically with the demand manager role with no separate assignment needed.|
|Template reader \(sn\_smart\_asmt.template\_reader\)|Demand managers \[demand\_manager\] who read the demand assessment template category. Contained automatically with the demand manager role with no separate assignment needed.|

A user's access to an individual assessment determines whether they can fill it in or only view the responses. A user with the **sn\_smart\_asmt.actor** role who is assigned an open assessment can answer and save it. An admin user must individually assign this role to the stakeholders, including to demand managers if they are required to fill the assessments. For more information, see [Assign a role to a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_AssignARoleToAUser.md).

A user with only read access can view the responses without editing them. For the complete list of Smart Assessment Engine roles, including how template category roles combine with template manager, reader, and contributor roles, see [Roles installed in Smart Assessment Engine](https://www.servicenow.com/docs/r/governance-risk-compliance/smart-assessment-engine/sae-roles-defined.html).

## Viewing smart assessments for demands

View smart assessments from a single demand, or across all your demands. The Smart Assessments grid displays the assessment instance, assessment template, demand, state, users, and due date columns. For more information on how to fill the assessment, see [Fill out a smart assessment for a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/strategic-planning/fill-out-a-smart-assessment.md).

There are two ways to view Smart Assessments:

-   From an individual demand, to see only that demand's assessments.

    \[Omitted image "demand-smart-assessment-l2.png"\] Alt text: Smart assessments within a demand record.

-   From the main navigation menu, to see every smart assessment you have access to, across all demands.

    \[Omitted image "demand-smart-assessments-l1.png"\] Alt text: Smart assessments for all demands.


**Note:** A demand manager sees every smart assessment across their demands; a stakeholder sees only the smart assessments they're assigned to.

## Demand assessment template questions

The predefined Smart assessment template for demand scores a demand across five weighted sections. The purpose of the template is populated as Demand. It mirrors the metric categories used by the classic assessment workflow to compare demands.

\[Omitted image "demand-smart-assess-questions.png"\] Alt text: Predefined smart assessment questionnaire for a demand.

The Smart Assessment Engine calculates the value of each section per assessment instance using the question weights of the respective sections. For more information about how the Smart Assessment Engine uses section weights, see [Scoring forms](https://www.servicenow.com/docs/r/governance-risk-compliance/smart-assessment-engine/scoring-forms.html).

<table id="tbl_smart_asmt_template_questions"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Size

</td><td>

Size of the demand relative to the average size \(scale of 1–10\).

</td></tr><tr><td>

Strategic Alignment

</td><td>

Strategic alignment of the demand. Consists of the following attributes:-   Priority of the demand based on its urgency and importance
-   Relation to a corporate initiative
-   Increasing job efficiencies
-   Increasing process consistency and optimization
-   Competitive advantage gain

</td></tr><tr><td>

Risk

</td><td>

Risk associated with the demand based on delays, compliance and regulatory requirements, infrastructure and business expansion, and dependencies.

</td></tr><tr><td>

ROI

</td><td>

Impact of the demand based on its expected effect on the business and financial return of the demand based on the projected value.

</td></tr><tr><td>

Cost

</td><td>

Labor cost, capital cost, and operational cost of the demand.

</td></tr></tbody>
</table>The Size, ROI, and Cost questions are answered automatically from existing demand field values. The remaining questions are scored on a scale of 1–10 by the person completing the assessment.

The predefined demand assessment template is the only template the automatic screening state trigger, completion check, and score population use. The template is hardcoded. A user with the **sn\_smart\_asmt.template\_manager** role can create additional smart assessment templates in the Assessment Workspace. Using a different template for demands also requires customizing the **DemandSmartAssessmentUtils** script include to use it. For more information, see [Create an assessment template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/sae-asmnt-template-create.md) and [Use a custom smart assessment template for demands](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/strategic-planning/override-smart-assessment-template-dw.md).

## Deleting or resetting a demand

Deleting a demand, or resetting it to draft, automatically cancels any of its smart assessments that are still open. A warning message is displayed when you try to reset a demand to draft that has smart assessments triggered.

If a demand already has classic assessments on it and is reset to Draft, that reset is treated as a fresh assessment flow. It is not a continuation of the old one. Any open old assessments are cancelled. If smart assessments is enabled, a new smart assessment is triggered instead.

