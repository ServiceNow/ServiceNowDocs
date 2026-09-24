---
title: Assign a contact to an engagement
description: Add a contact from your third-party organization to a specific engagement team so they can access questionnaire requests for that engagement.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm-portal-assign-engagement-contact.html
release: brazil
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Third-party portal contact roles and permissions, Manage the third-party portal, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Assign a contact to an engagement

Add a contact from your third-party organization to a specific engagement team so they can access questionnaire requests for that engagement.

## Before you begin

The contact must be registered in the third-party portal before being assigned to an engagement.

**Important:**

This task applies to Third-Party Risk Management \(TPRM\) with Smart Assessment Engine \(SAE\) usage only. Engagement contact assignment and management may differ in Classic TPRM environments.

In both Classic and SAE, contacts can be assigned to engagements. However, questionnaire assignment behavior differs: In Classic, only one primary contact receives the questionnaire; in SAE, all primary contacts are automatically assigned to questionnaire requests for that engagement, with one designated as the questionnaire owner \(see [Third-party portal contact roles and permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-contact-roles.md) for details\).

Role required: third-party primary contact, or engagement primary contact for the specific engagement.

## About this task

Assigning a contact to an engagement gives them access to that engagement's questionnaire requests, tasks, and issues. You can designate the contact as an engagement primary contact during assignment or at any time afterward.

## Procedure

1.  Navigate to **My Team** from the home page.

2.  In the right panel, select the engagement from the dropdown list.

3.  In the left panel under **All contacts**, find the contact you want to add.

4.  Select **Add** next to the contact's name.

    The contact appears in the right panel under **Engagement contacts**.

    If the contact does not appear in the list of all contacts, verify that they have been invited to and registered in the portal. See [Invite a contact to the third-party portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-invite-contact.md).

5.  To designate the contact as an engagement primary contact, select the **Primary Contact** check box next to their name.

    In SAE, engagement primary contacts are automatically added to all active questionnaire requests for the engagement and can manage the engagement team. An engagement must have at least one engagement primary contact for questionnaire assignment to work properly. For details, see [Questionnaire ownership and contributor access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-questionnaire-ownership.md).

    If the contact can access the engagement but cannot see any questionnaire requests, verify that questionnaire requests for the engagement are in an active state and that the contact has been added as a questionnaire owner or contributor. In SAE, secondary contacts are not automatically added to questionnaire requests.


**Related topics**  


[Managing the Third-party portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/vendor-portal.md)

[Third-party portal contact roles and permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-contact-roles.md)

[Questionnaire ownership and contributor access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-questionnaire-ownership.md)

[Invite a contact to the third-party portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-invite-contact.md)

[Manage questionnaire contributors and ownership](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-manage-contributors.md)

[Deactivate a third-party portal contact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-deactivate-contact.md)

