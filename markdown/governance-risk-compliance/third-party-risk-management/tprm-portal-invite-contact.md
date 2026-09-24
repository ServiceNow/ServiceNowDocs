---
title: Invite a contact to the third-party portal
description: Invite a new team member to the third-party portal so they can access questionnaire requests, tasks, and issues for your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm-portal-invite-contact.html
release: brazil
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Third-party portal contact roles and permissions, Manage the third-party portal, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Invite a contact to the third-party portal

Invite a new team member to the third-party portal so they can access questionnaire requests, tasks, and issues for your organization.

## Before you begin

**Important:**

This task applies to Third-Party Risk Management \(TPRM\) with Smart Assessment Engine \(SAE\) usage only. Portal contact invitation and management may differ in Classic TPRM environments.

The contact invitation process is the same in both Classic and SAE. However, how invited contacts are assigned to questionnaires differs between the two engines \(see [Third-party portal contact roles and permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-contact-roles.md) for details\).

Role required: third-party primary contact.

## About this task

Invite a contact to give a team member access to the third-party portal. When you invite a contact, the contact receives an email invitation to register for the portal.

## Procedure

1.  Navigate to **Manage Team** on the home page.

2.  Select **Invite Contact**.

3.  Fill in the contact's information.

    |Field|Description|
    |-----|-----------|
    |First Name|The contact's first name.|
    |Last Name|The contact's last name. When multiple third-party primary contacts exist, the system uses last name alphabetical order to determine the questionnaire owner.|
    |Email Address|The contact's work email address. The portal invitation is sent to this address.|
    |Title/Role|The contact's job title or role within your organization.|

4.  Specify whether the contact is a primary contact by using the **Primary Contact** option.

    -   Select **Primary Contact** to create the contact as a third-party primary contact.
    -   Leave **Primary Contact** unchecked to create the contact as a third-party secondary contact.
    **Important:**

    Third-party primary contacts are automatically added as questionnaire owners or contributors to questionnaire requests. The system selects the questionnaire owner based on alphabetical order by last name when multiple primary contacts exist. For details, see [Questionnaire ownership and contributor access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-questionnaire-ownership.md).

5.  Select **Save**.

    The contact receives an email invitation to register for the portal.

    If the contact does not receive the invitation email, verify that the email address is correct and ask your customer's administrator to confirm that the portal email settings are configured.


**Related topics**  


[Managing the Third-party portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/vendor-portal.md)

[Third-party portal contact roles and permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-contact-roles.md)

[Questionnaire ownership and contributor access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-questionnaire-ownership.md)

[Manage questionnaire contributors and ownership](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-manage-contributors.md)

[Assign a contact to an engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-assign-engagement-contact.md)

[Deactivate a third-party portal contact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-deactivate-contact.md)

