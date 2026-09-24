---
title: Monitoring third-party elements
description: Monitor third-party elements using scalable scoring models, relationship analysis, and due diligence workflow integration in the Third-party Risk Management application to conduct more informed risk assessments as part of your third-party risk program.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm-monitor-tp-elements.html
release: brazil
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 9
breadcrumb: [Monitor third-party risk, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Monitoring third-party elements

Monitor third-party elements using scalable scoring models, relationship analysis, and due diligence workflow integration in the Third-party Risk Management application to conduct more informed risk assessments as part of your third-party risk program.

## Third-party elements overview

Third-party elements \(TP elements\) are the external organizations or entities that an engagement relies on to provide goods, services, or support. TP elements can include the suppliers, contractors, facilities, individuals, or any other external organization that can access the engagement's systems, data, or facilities.

Examples of TP element classes and associated risks:

-   **Datacenter**

    A facility or location where an engagement or third party outsources the storage, processing, and management of their data and IT infrastructure. A datacenter could potentially experience a data breach, downtime, or compliance violation that exposes their engagements to unexpected risk. This example would be classified as a Facility TP element.

-   **Manufacturing facility**

    A facility or location where an engagement or third party outsources the production or assembly of their products. A manufacturing facility could potentially experience a supply chain disruption, a counterfeit part, or a regulatory compliance issue that exposes their engagements to unexpected risk. This example would be classified as a Facility TP element.

-   **Beneficial owner**

    An individual who owns or controls an organization that is involved in a business relationship or transaction. These individuals may not be the registered or legal owners of the organization, but have significant influence or control over its operations, decision-making, or financial affairs. This example would be classified as a Principal TP element.

-   **AI use case**

    An AI system or application that a third party or engagement uses as part of its operations. AI use case elements capture information that domain experts need to review as part of your due diligence process.

-   **AI model**

    An AI model that an AI use case relies on. Select **Global AI model** to make it available for linking to AI use case elements across multiple third parties. Leave it cleared to make it available only within the third party where it was created.


For more information on TP elements and examples of their associated controls and potential risks, see [Terminology](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-terminology.md).

## Collecting and reviewing third-party elements

Collecting TP elements is optional. You can add elements directly, or assign the work through a task to the due diligence requester or a third-party or engagement contact.

**Note:** The ability to create TP elements by reviewing collection questionnaire responses was removed in the Brazil release. TP elements are created directly, either in the Elements grid or through a task.

To collect TP elements:

1.  If AI assets are involved in the engagement, the due diligence requester selects **AI assets involved** when creating the due diligence request. The requester also identifies the internal user who responds to the Inherent Risk Questionnaire \(IRQ\).

2.  The due diligence request owner selects **Start onboarding**. An internal assessment is created for the IRQ process. If the requester selected **AI assets involved**, an internal task is also created, assigning the due diligence requester to add AI use case elements.

3.  The IRQ responder completes the internal assessment. If an internal task for AI use cases was created, the due diligence requester completes the task by adding AI use case elements directly in the Elements grid. For more information, see [Create a task for an internal user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-internal-tasks.md), [Manage a task for a third party or engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-ws-task-manage.md), [Manage elements in the grid](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-elements-grid-manage.md), and [Complete an element collection task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-elements-task-manage.md).

4.  After the internal assessment and, if applicable, the internal task for AI use cases are complete, the due diligence request owner can select **Start collection** or **Start due diligence**.

5.  To collect more elements from the third party or engagement, the due diligence request owner selects **Start collection**. The system creates a task and assigns it to a third-party or engagement contact.

6.  The third-party or engagement contact completes the task by selecting **Manage elements** on the task to open the Elements grid, adding or editing elements, and then selecting **Resolve Task**. For more information, see [Complete an element collection task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-elements-task-manage.md).

7.  When ready to begin element-level assessments, the due diligence request owner selects **Start due diligence**. An assessment is created only for elements marked as **Assessment required**.


The process for assessing elements is the same as assessing any other third-party risk area. For more information on assessments, see [Assessing your third-party risk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-assessing-tpr.md).

## Adding third-party elements to engagements

You can create a TP element from either of the following locations:

-   From an engagement's **Elements** tab. An element created this way is linked to that engagement automatically.
-   From the third party's Elements grid. An element created this way isn't linked to any engagement by default.

If you create an element at the third-party level, the element isn't available for assessment until you link it to an engagement. In the engagement's **Elements** tab, select **Add** to link an existing TP element to that engagement. For more information, see [Add a third-party element record to an engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-tp-element-engagement.md) and [Manage elements in the grid](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-elements-grid-manage.md). After you link the elements to an engagement, you can start the due diligence process for those elements.

## Element-scoped assessments, issues, and tasks

Assessments, issues, and tasks can be scoped to a TP element instead of an engagement. When a record is scoped to an element, the **Element** field is visible and required. This scope is available only when the third party uses the Smart Assessment Engine \(SAE\). When SAE isn't in use, the element option isn't available for external assessments, issues, or tasks. Element evidence is captured against the third party and element. The record's contribution to a specific engagement is calculated from the element-engagement relationship, not tied to the engagement directly. Existing behavior for assessments, issues, and tasks scoped to a third party or to an engagement is unchanged.

Third-party and engagement contacts can respond to element-scoped assessments in the third-party portal in the same way they respond to engagement-scoped assessments.

When a questionnaire template is sent to an element more than once, the system checks whether the previous respondent is still a primary contact. If so, the questionnaire is assigned to that contact again. If they're no longer a primary contact, the questionnaire is assigned to the current primary contact instead.

## Third-party element scoring

You can categorize each TP element into one of the following types: Facility, Product, Principal, or Other. This classification helps you organize the assessment criteria and subsequent scoring. Scoring on a TP element is determined by averaging the risk ratings from its associated third-party risk assessments. If you conduct multiple assessments for the same TP element, the system scores only the latest assessment for each questionnaire template, based on assessment close date. Duplicate assessments are excluded. This approach maintains a current risk rating for the TP element. For example, if a TP element has assessments with risk ratings of Very High and Very Low, the average leads to an overall risk rating of Moderate.

TP element assessment scores roll up to the third-party level through relationship scores calculated from questionnaire-level evidence. An assessment sent on a TP element calculates a risk rating using the third party's scoring rule. This rating is informational only and doesn't roll up on its own. When a TP element is linked to an engagement, the engagement's risk rating for that element-engagement relationship is calculated dynamically using the engagement's scoring rule. The system collects every assessment sent on the TP element and keeps only the latest assessment for each questionnaire template, based on assessment close date. It then applies the engagement's risk-area criteria to that set. When more than one TP element shares the same classification for an engagement \(for example, multiple TP elements classified as Product\), component criteria are applied at the classification level. The resulting component score contributes to the engagement's overall risk score. Engagement and third-party risk-area calculations also include assessments sent on linked TP elements and assessments sent directly on the engagement or third party. If you link a TP element that already has assessment evidence to a new engagement, the relationship score is calculated automatically using the existing evidence. A new assessment on the TP element isn't required for each engagement it's linked to. Linking or unlinking a TP element and closing a TP element assessment each recalculate the affected engagement and third-party ratings in real time. Reassigning a third party's scoring rule triggers a full recalculation of that third party's score tree, including its engagements and elements.

**Note:** The relationship score uses the target engagement's scoring rule and business service criticality, not the third party's scoring rule in the relationship score calculation. This means the same element can produce different risk ratings for different engagements. The calculation uses raw questionnaire and document request ratings from closed, valid element assessments \(not assessment-level risk ratings\). When multiple assessments use the same questionnaire template, only the latest assessment \(by close date\) is used; different templates in the same risk area both contribute. If no valid evidence exists for a relationship, the risk rating is cleared. The relationship score is stored in `sn_tprm_dd_m2m_engagement_element.risk_rating`.

You can create your own TP element classifications to meet your specific risk program requirements. For more information on creating classifications and assigning weights for scoring, see [Third-party element form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-tpe-form.md) and [Define component criteria](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-component-criteria-define.md).

