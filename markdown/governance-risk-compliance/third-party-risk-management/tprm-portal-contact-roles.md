---
title: Third-party portal contact roles and permissions
description: The third-party portal uses a role-based access model to control who can view, respond to, and manage questionnaire requests, issues, and tasks. Each of the four contact role types has a defined scope and set of permissions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm-portal-contact-roles.html
release: brazil
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 6
breadcrumb: [Manage the third-party portal, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Third-party portal contact roles and permissions

The third-party portal uses a role-based access model to control who can view, respond to, and manage questionnaire requests, issues, and tasks. Each of the four contact role types has a defined scope and set of permissions.

**Important:**

This content describes contact roles and permissions in Smart Assessment Engine \(SAE\). The same four contact role types exist in both Smart and Classic engine, but their permissions differ due to different questionnaire assignment and submission models. In Classic, questionnaires are assigned to a single primary contact; in SAE, all primary contacts are automatically assigned and one is designated as the questionnaire owner. For information on the Classic assignment model, see [Managing the Third-party portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/vendor-portal.md).

Third-party organizations may have multiple engagements with a customer—for example, different projects, services, or business units—and different team members may be responsible for responding to different questionnaire requests. The contact role system helps ensure that the right people have access to the correct information.

There are four contact role types in the third-party portal, organized by scope: third-party-level roles apply across the entire third-party organization, and engagement-level roles are scoped to a single engagement.

## Third-party primary contact

A third-party primary contact is the main administrator for the third-party organization in the portal. This role manages portal access for the third-party organization and can invite contacts, assign contacts to engagements, and coordinate questionnaire responses.

Third-party primary contacts are automatically added as the questionnaire owner or contributor to active third-party-level questionnaire requests. They are not automatically added to engagement-level questionnaire requests unless they are also added to the engagement or added to the questionnaire by the questionnaire owner.

When a third-party organization has multiple third-party primary contacts, the system selects one as the questionnaire owner based on alphabetical order by last name. The remaining primary contacts are added as questionnaire contributors. All primary contacts can view and respond to questions, but only the questionnaire owner can submit the completed questionnaire or reassign ownership.

This role is appropriate for vendor relationship managers, compliance officers, executive sponsors, and portal administrators.

**Note:** When you are designated as a third-party primary contact, the system automatically synchronizes you to existing third-party-level questionnaire requests. This synchronization occurs in the background. If you do not see questionnaire requests, refresh your browser or log out and log back in.

## Third-party secondary contact

A third-party secondary contact is a regular user within the third-party organization with limited permissions. Unlike third-party primary contacts, secondary contacts are not automatically added to questionnaire requests. A questionnaire owner must explicitly add them using the **Manage Contributors** or **Reassign** actions.

When added to a questionnaire, third-party secondary contacts can view and respond to questions but cannot submit the questionnaire. If a questionnaire owner reassigns ownership to a third-party secondary contact, that contact gains full questionnaire owner permissions for that specific questionnaire.

This role is appropriate for subject matter experts, technical staff, and department representatives who respond to specific assessments.

## Engagement primary contact

An engagement primary contact has administrative privileges scoped to a single engagement. This role manages engagement-level access and questionnaire coordination for that engagement.

Engagement primary contacts are automatically added as the questionnaire owner or contributor to all questionnaire requests linked to their engagement. They cannot access questionnaire requests from other engagements or vendor-level questionnaire requests not tied to a specific engagement.

**Important:**

An engagement must have at least one engagement primary contact for questionnaire requests to be sent. Without an engagement primary contact, the system cannot assign a questionnaire owner for engagement-level assessments.

This role is appropriate for project managers, service delivery leads, and regional managers responsible for specific customer engagements.

## Engagement secondary contact

An engagement secondary contact is a regular team member assigned to a specific engagement with limited permissions. Like third-party secondary contacts, engagement secondary contacts are not automatically added to questionnaire requests and must be manually added by the questionnaire owner.

Engagement secondary contacts can only be assigned to questionnaire requests within their specific engagement. If ownership is reassigned to an engagement secondary contact, that contact gains full questionnaire owner permissions for that specific questionnaire.

This role is appropriate for individual contributors, technical specialists, and consultants working on a particular engagement.

## Contact routing for element-scoped assessments, issues, and tasks

A third-party element can be linked to multiple engagements. For an element-scoped assessment, issue, or task, contact routing considers the engagement primary contacts from all linked engagements, not just a single engagement. The system collects the engagement primary contact from each linked engagement and assigns the contact whose last name appears first in alphabetical order. At least one linked engagement must have an engagement primary contact. Otherwise, you receive the message "At least one primary contact must exist in the linked engagements for the element", and the assessment, issue, or task can't be submitted to the third party.

When you resend an assessment for the same element and questionnaire template, the system routes the assessment to the contact who handled the previous assessment for that template, provided that the contact is still active. If that contact is no longer available, the system falls back to the current engagement primary contacts from the element's linked engagements and applies the standard routing logic. For element-scoped records, reassignment and collaborator selection are also limited to engagement primary contacts from the element's linked engagements.

## Contact role permissions

The following table summarizes the permissions available to each contact role type in Smart Assessment Engine \(SAE\) environments.

|Capability|Third-party primary|Third-party secondary|Engagement primary|Engagement secondary|
|----------|-------------------|---------------------|------------------|--------------------|
|Invite new users to portal|Yes|No|No|No|
|Designate third-party primary contacts|Yes|No|No|No|
|Designate engagement primary contacts|Yes|No|Yes \(own engagement only\)|No|
|View all third-party-level questionnaire requests|Yes|No|No|No|
|View all questionnaire requests for an engagement|No|No|Yes \(own engagement only\)|No|
|Automatically added to third-party-level questionnaire requests|Yes \(as owner or contributor\)|No|No|No|
|Automatically added to engagement questionnaire requests|No|No|Yes \(own engagement only\)|No|
|Submit questionnaire \(only if questionnaire owner\)|Yes|Yes|Yes|Yes|
|Reassign questionnaire ownership \(if questionnaire owner\)|Yes|Yes|Yes|Yes|
|Manage questionnaire contributors \(if questionnaire owner\)|Yes|Yes|Yes|Yes|
|Manage engagement team membership|Yes \(all engagements\)|No|Yes \(own engagement only\)|No|
|Deactivate contacts|Yes \(third-party primary contact only\)|No|No|No|
|Access multiple engagements|Yes \(all\)|No|Yes \(assigned engagements only\)|Yes \(assigned engagements only\)|

**Related topics**  


[Managing the Third-party portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/vendor-portal.md)

[Questionnaire ownership and contributor access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-questionnaire-ownership.md)

[Manage questionnaire contributors and ownership](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-manage-contributors.md)

[Invite a contact to the third-party portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-invite-contact.md)

[Assign a contact to an engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-assign-engagement-contact.md)

[Deactivate a third-party portal contact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-deactivate-contact.md)

[Manage access for your third-party contacts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-manage-tp-contact.md)

