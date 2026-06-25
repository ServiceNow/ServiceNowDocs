---
title: Integrating Third-party Risk Management with GRC: Policy and Compliance Management
description: The GRC: Policy and Compliance Management integration updates the compliance status of controls and control objectives based on the questionnaire responses from a third party or engagement. Compliance managers \[sn\_compliance.manager\] can associate controls and control objectives with specific questions, third parties, and engagements used in Third-party Risk Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/pc-assessment-integration.html
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Integrate, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Integrating Third-party Risk Management with GRC: Policy and Compliance Management

The GRC: Policy and Compliance Management integration updates the compliance status of controls and control objectives based on the questionnaire responses from a third party or engagement. Compliance managers \[sn\_compliance.manager\] can associate controls and control objectives with specific questions, third parties, and engagements used in Third-party Risk Management.

If you have the Policy and Compliance Management application installed, users with the Compliance Manager role can perform several key tasks that help manage and assess Third-party compliance.

-   You can associate third parties and engagements to specific control objectives. This association results in controls being applied to the third party or engagement

    For more information, see [Manually add a control to a third party or engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-add-controls-tp.md).

-   You can individually link the question to multiple control objectives for each question in a questionnaire template. This enables for a granular and detailed assessment of compliance.

    For more information, see [Manually add a control objective to a question](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-add-controls-q.md).

-   When third parties and engagements respond to questionnaires, the system automatically updates the compliance status of the linked controls. If they provide an incorrect answer, the associated controls are marked as non-compliant. Conversely, correct answers keep the controls compliant.

**Note:** Although it is not possible to directly map control objectives to questions in SAE questionnaires, SAE provides the capability to flag controls as compliant or non-compliant through post-assessment actions.

All third parties are automatically categorized into an entity type called Vendors. This helps ensure that each third party and engagement is represented as an entity.

When an entity, such as a third party or engagement, is associated with a control objective a corresponding control is created for that entity. This association links the third party or engagement with the control, which can influence the compliance status of the control.

In the context of Third-party Risk Management, each question in a questionnaire template can be individually linked to multiple control objectives through a related list. When a questionnaire is sent to a third party and the third party responds with an incorrect answer, the controls associated with the linked control objectives are marked as non-compliant. Conversely, if the third party provides the correct answer, the controls remain compliant.

This feature helps ensure that the compliance status of controls is dynamically updated based on the third party or engagements responses, providing a real-time and accurate assessment of their compliance. Both Policy and Compliance Management users and Third-party risk assessors \[sn\_vdr\_risk\_asmt.vendor\_assessor\] can monitor the status of a control.

**Note:**

Third-party Risk Management consumes compliance objects in a read-only capacity. Controls and control objectives are authored and managed in GRC: Policy and Compliance Management.

For more information on implementing Policy and Compliance Management, see [Implementing Policy and Compliance Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/policy-and-compliance-management/policy-compliance-impl-overview.md).

-   **[Manually add a control to a third party or engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-add-controls-tp.md)**  
If you’re using both Policy and Compliance Management and Third-party Risk Management, you can associate controls with third parties and engagements. Controls can be marked as compliant or non-compliant.
-   **[Manually add a control objective to a question](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-add-controls-q.md)**  
If you’re using both Policy and Compliance Management and Third-party Risk Management, you can associate control objectives and controls with questions. Controls can be marked as compliant or non-compliant based on the response to the question.

**Parent Topic:**[Integrating TPRM with other applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/integrating-with-tprm.md)

**Related topics**  


[Manually add a control to a third party or engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-add-controls-tp.md)

[Manually add a control objective to a question](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-add-controls-q.md)

[Assessing your third-party risk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-assessing-tpr.md)

[Implementing Policy and Compliance Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/policy-and-compliance-management/policy-compliance-impl-overview.md)

