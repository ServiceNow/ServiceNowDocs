---
title: Questionnaire ownership and contributor access
description: Each Smart Assessment Engine questionnaire request in the third-party portal has a single questionnaire owner and can include questionnaire contributors. Ownership determines who can submit the completed questionnaire and who can manage team access.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm-portal-questionnaire-ownership.html
release: brazil
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2026-06-03"
reading_time_minutes: 3
breadcrumb: [Third-party portal contact roles and permissions, Manage the third-party portal, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Questionnaire ownership and contributor access

Each Smart Assessment Engine questionnaire request in the third-party portal has a single questionnaire owner and can include questionnaire contributors. Ownership determines who can submit the completed questionnaire and who can manage team access.

**Important:**

This content applies to Third-Party Risk Management \(TPRM\) with Smart Assessment Engine \(SAE\) usage only. Questionnaire ownership and contributor behavior may differ in Classic TPRM environments.

## Questionnaire owner and questionnaire contributor

Every questionnaire request has exactly one questionnaire owner. The questionnaire owner is the primary responsible party for that questionnaire and is the only person who can submit the completed questionnaire to the customer, reassign ownership to another contact, or add and remove questionnaire contributors.

Questionnaire contributors are additional team members who can view and respond to questions, upload documents, and add comments. Multiple contributors can be assigned to a single questionnaire, but contributors cannot submit the questionnaire or manage other contributors.

The questionnaire owner is assigned based on the contact role type:

-   When there is one third-party or engagement primary contact for an organization, that contact is automatically designated as the questionnaire owner for questionnaire requests at their scope level.
-   When there are multiple third-party or engagement primary contacts, the system selects the questionnaire owner based on alphabetical order by last name. All other primary contacts are added as questionnaire contributors.
-   Third-party or engagement secondary contacts are initially added as questionnaire contributors when a questionnaire owner adds them manually.

Any eligible contact within the applicable third-party or engagement scope can become the questionnaire owner if the current owner uses the **Reassign** action to transfer ownership.

## Reassign ownership versus manage contributors

The **Reassign** and **Manage Contributors** actions serve different purposes and have different effects on questionnaire access.

Use **Reassign** to transfer questionnaire ownership to a different person. After reassignment, the new owner gains full control of the questionnaire, including the ability to submit and manage contributors. Only one person can be selected as the new owner.

**Important:**

When ownership is reassigned, the previous owner loses access to the questionnaire unless the new owner adds them back as a contributor.

Use **Manage Contributors** to add or remove people who can help complete the questionnaire. Adding contributors does not change who the questionnaire owner is. Contributors can respond to questions but cannot submit the questionnaire or manage other contributors.

Only the current questionnaire owner can use either action. Being a third-party primary contact or engagement primary contact does not grant access to these actions unless the contact is also the questionnaire owner for that specific questionnaire.

**Related topics**  


[Managing the Third-party portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/vendor-portal.md)

[Third-party portal contact roles and permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-contact-roles.md)

[Manage questionnaire contributors and ownership](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-manage-contributors.md)

[Respond to a questionnaire in the third-party portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-respond-questionnaire.md)

[Invite a contact to the third-party portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-invite-contact.md)

