---
title: Managing the Third-party portal
description: Third-party contacts respond to questionnaires, requests for documentation, tasks, and issues on the Third-party portal. The portal is the point of interaction between third parties and risk assessors.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/vendor-portal.html
release: brazil
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 9
breadcrumb: [Third-party Risk Management, Governance, Risk, and Compliance]
---

# Managing the Third-party portal

Third-party contacts respond to questionnaires, requests for documentation, tasks, and issues on the Third-party portal. The portal is the point of interaction between third parties and risk assessors.

## Third-party contacts

Third-party contacts represent the third party and use the third-party portal to respond to questionnaires, complete tasks, and address issues raised by your assessment team. Contacts can be primary or secondary.

Each third party must have at least one primary contact. Primary contacts coordinate questionnaire responses, manage portal access, and can assign work to other contacts. Secondary contacts typically respond to assigned work and have limited access.

Contacts can exist at two levels:

-   Third party-level contacts, who support the overall vendor organization
-   Engagement-level contacts, who participate in specific engagements

Third-party contacts are automatically assigned the `vendor_contact` and `snc_external` roles. The `vendor_contact` role provides access to the third-party portal, and the `snc_external` role restricts access to the portal only.

**Important:** The third-party contact role is designed only for external users and restricts access to the third-party portal.

## Launching the portal

Third-party contacts access the portal using **\[your instance URL\]/svdp**.

## Tasks for third-party contacts

Primary contacts can perform the following tasks:

-   Delegate questionnaires, tasks, and issues to other contacts
-   Manage contact and engagement assignments
-   Update contact information and notification preferences

Secondary contacts can:

-   View and respond to assigned assessments
-   Participate in questionnaires and tasks assigned to them
-   Manage their account access

**Note:**

Issue indicators appear in the third-party portal only after an issue is submitted and the **Visible in third-party portal** field is selected.

Assessment counts include only active, pending, and in-progress assessments. Cancelled and inactive assessments are excluded.

The comments field saves automatically when focus moves away from the field.

## Questionnaire and document request states

Progress in questionnaires and document requests is tracked through request states:

-   **New**

    The request is sent to the third party.

-   **In progress**

    Responses are being entered.

-   **Completed**

    All responses are completed.

    **Note:** You must submit the assessment after all requests are complete.

    For more information on states, see [External assessment lifecycle states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-external-assessment-lifecycle.md).


## Responding to questionnaires

Third-party contacts respond to questionnaires and document requests assigned to them in the portal. They can provide responses, upload supporting documentation, and track progress.

Contacts can respond directly in the portal or by using a Microsoft Excel template or SIG questionnaire format.

For information on responding to a questionnaire, see [Respond to a questionnaire in the third-party portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-respond-questionnaire.md).

## Learning to use the portal—the FAQ page

Third-party contacts can select **FAQ** to view answers to common questions about using the portal.

## Setting up the third-party portal \(Admin\)

ServiceNow administrators and TPR managers use TPRM to set up and manage third-party contacts in your instance. Admin responsibilities include:

-   Create contact records and manage contact logins
-   Enable or disable portal access
-   Reset passwords and resend invitations
-   Assign roles and permissions
-   Manage contact information and account status

For step-by-step guidance, see the following admin tasks:

-   [Set up third-party contacts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-tp-contact-config.md) — Create and configure contact records in the admin interface
-   [Manage access for your third-party contacts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-manage-tp-contact.md) — Manage access, deactivate accounts, reset passwords, and resend invitations

**Note:** You can respond on behalf of third-party contacts if the **sn\_svdp.allow\_assessor\_edit** property is enabled.

## Using the third-party portal \(Contact\)

Third-party contacts \(external users\) use the third-party portal to manage questionnaires, invite team members, and coordinate assessment responses. Contact tasks include:

-   Invite new team members to the portal
-   Assign contacts to engagements
-   Manage questionnaire contributors and ownership
-   Respond to questionnaires and submit assessments
-   Deactivate inactive team members

For step-by-step guidance, see the following contact tasks:

-   [Third-party portal contact roles and permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-contact-roles.md) — Understand contact role types and permissions
-   [Questionnaire ownership and contributor access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-questionnaire-ownership.md) — Learn about questionnaire ownership and contributor access
-   [Invite a contact to the third-party portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-invite-contact.md) — Invite new team members to the portal
-   [Assign a contact to an engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-assign-engagement-contact.md) — Assign contacts to engagements
-   [Manage questionnaire contributors and ownership](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-manage-contributors.md) — Manage questionnaire contributors and reassign ownership
-   [Respond to a questionnaire in the third-party portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-respond-questionnaire.md) — Respond to and submit questionnaires
-   [Deactivate a third-party portal contact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-deactivate-contact.md) — Deactivate team members

## Assessment assignment behavior by engine

Assignment and submission behavior for questionnaires differs depending on whether your organization uses the Classic assessment engine or Smart Assessment Engine \(SAE\). This section explains how each engine assigns questionnaires to primary contacts and how submission works.

## Classic assessment engine

In Classic environments, when a questionnaire is generated for a third party or engagement, the system assigns the questionnaire to a single primary contact based on alphabetical order. That contact is responsible for completing and submitting the questionnaire.

Secondary contacts and other primary contacts do not automatically receive the questionnaire and cannot submit it on behalf of the assigned contact.

## Smart Assessment Engine \(SAE\)

In SAE environments, questionnaire assignment and submission work differently than in Classic:

-   All primary contacts are automatically assigned to the questionnaire.
-   The system designates one primary contact as the questionnaire owner, typically based on alphabetical order by last name.
-   The questionnaire owner is responsible for submitting the questionnaire and managing contributor access.
-   Other primary contacts are added as questionnaire contributors.

For detailed information on the questionnaire owner and contributor roles, permissions, and how to manage them, see the following topics:

-   [Questionnaire ownership and contributor access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-questionnaire-ownership.md) — Explains the owner and contributor model and how to reassign ownership or manage contributors
-   [Manage questionnaire contributors and ownership](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-manage-contributors.md) — Step-by-step guidance on managing contributors

**Important:**

Questionnaire owner and contributor behavior applies only to SAE assessments. Classic assessments do not use this model.

**Related topics**  


[Set up third-party contacts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-tp-contact-config.md)

[Manage access for your third-party contacts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-manage-tp-contact.md)

[Third-party portal contact roles and permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-contact-roles.md)

[Questionnaire ownership and contributor access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-questionnaire-ownership.md)

[Invite a contact to the third-party portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-invite-contact.md)

[Assign a contact to an engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-assign-engagement-contact.md)

[Manage questionnaire contributors and ownership](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-manage-contributors.md)

[Deactivate a third-party portal contact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-deactivate-contact.md)

[Respond to a questionnaire in the third-party portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-respond-questionnaire.md)

[Upload and manage documents in the third-party portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-add-document-portal.md)

[Using a Microsoft Excel spreadsheet template for external questionnaires](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-excel-template-support.md)

[Respond using a Microsoft Excel template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-tpcontact-use-excel.md)

[Using the SIG questionnaire for a risk assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-sig-use-and-support.md)

[Respond using the SIG](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-tpcontact-use-sig.md)

[TPRM and the Explicit Roles plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/vrm-and-explicit-roles-plugin.md)

[E-signatures on questionnaires or document requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-ws-approve-with-e-sig.md)

