---
title: Manage access for your third-party contacts
description: View your existing third-party contacts and adjust their information and access permissions as needed by using Third-party Risk Management. When you keep the contact details up to date, you can help to avoid your third-party contacts from getting unauthorized access or losing authorized access to the third-party portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm-manage-tp-contact.html
release: brazil
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Manage the third-party portal, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Manage access for your third-party contacts

View your existing third-party contacts and adjust their information and access permissions as needed by using Third-party Risk Management. When you keep the contact details up to date, you can help to avoid your third-party contacts from getting unauthorized access or losing authorized access to the third-party portal.

## Before you begin

The third-party risk \(TPR\) manager must contact a team member with the admin role to delete a contact, lock out a contact, set a password, or reset a password.

**Note:**

This content applies to your organization's internal management of third-party contacts. This is the admin interface used by TPR managers and assessors in your TPRM instance. For guidance on how third-party contacts manage their team members' access through the portal \(SAE\), see [Managing the Third-party portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/vendor-portal.md).

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager. Admin access is required to delete a contact, lock out a contact, set a password, or reset a password.

## About this task

Your third-party contacts are external users at the third-party organization. They use the third-party portal to securely organize, prioritize, and perform tasks like responding to questionnaires for assessments and communicating with your risk-assessment staff about issues. You can also adjust the access to the third-party portal and permissions for your third-party contacts.

## Procedure

1.  Navigate to **All** &gt; **Third-party Risk Management** &gt; **Third Parties** &gt; **Third-party Contacts** to view your existing third-party contacts.

    The number of contacts is listed for each third party on the third-party contacts page.

2.  Select the third party that you want to view the list of associated contacts for and then select the third-party contact.

    \[Omitted image "tprm-manage-tp-contact.png"\] Alt text: Third-party contact's information and the relevant buttons, options, and related link locations on the form. For a description of each action, refer to the steps that follow.

3.  Manage the access to the portal for your third-party contacts.

<table id="choicetable_x4v_zdv_2bc"><thead><tr><th align="left" id="d258742e119">

Option

</th><th align="left" id="d258742e122">

Description

</th></tr></thead><tbody><tr><td id="d258742e128">

**Deactivate the account**

</td><td>

Deactivate the account by clearing the **Active** check box.

 After you deactivate the account, the third-party contact can't log in or appear in the list of associated contacts.

</td></tr><tr><td id="d258742e146">

**Resend Invite**

</td><td>

Resend an email invitation for accessing the third-party contact portal by selecting the **Resend Invite** related link.

 The email contains a link to the third-party portal and login credentials.

</td></tr><tr><td id="d258742e164">

**Delete Contact**

</td><td>

Remove the snc\_external role from the third-party contact and deactivate the third-party contact by selecting the **Delete Contact** related link.

</td></tr><tr><td id="d258742e176">

**Locked out**

</td><td>

Lock out the third-party contact by selecting the **Locked out** option.

 After you lock out the third-party contact, that person can't log in. The contact record remains active, but portal access is blocked.

</td></tr><tr><td id="d258742e195">

**Set password**

</td><td>

Generate a new password and send it to the third-party contact by selecting **Set Password**.

</td></tr><tr><td id="d258742e207">

**Reset a password**

</td><td>

Send an email with a link for resetting a third-party contact's password by selecting the **Reset a password** related link.

 Additional setup by your team member with the admin role is required.

</td></tr></tbody>
</table>4.  Select **Update**.

    **Note:** For more information on setting up third-party contacts, see [Set up third-party contacts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-tp-contact-config.md) and [Enable email with third-party contacts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/set_sys_props_for_email.md).


**Related topics**  


[Managing the Third-party portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/vendor-portal.md)

[Set up third-party contacts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-tp-contact-config.md)

[Third-party portal contact roles and permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-contact-roles.md)

[Invite a contact to the third-party portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-invite-contact.md)

[Deactivate a third-party portal contact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-portal-deactivate-contact.md)

