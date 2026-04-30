---
title: Set up third-party contacts
description: Set up your third-party contacts so that you can send assessments, address issues, and communicate any additional required information with these contacts using Third-party Risk Management.
locale: en-US
release: zurich
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Manage the third-party portal, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Set up third-party contacts

Set up your third-party contacts so that you can send assessments, address issues, and communicate any additional required information with these contacts using Third-party Risk Management.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager and admin for steps 4 and 5

## About this task

Third-party contacts are external users at the third-party organization. They use the Third-party portal to securely organize, prioritize, and perform tasks like responding to questionnaires for assessments, performing tasks, and communicating with your risk-assessment staff regarding issues. You grant access to the Third-party portal and specify the permissions for third-party contacts. The third-party risk \(TPR\) manager must contact a team member with the admin role to complete steps 4 and 5.

**Important:** The third-party contact role should be used only for external contacts. The role prohibits access to your ServiceNow AI Platform instance and grants access only to the Third-party portal.

## Procedure

1.  Navigate to **All** &gt; **Third-party Risk Management** &gt; **Third Parties** &gt; **Third-party Contacts** to determine whether a third-party contact has already been assigned.

    The number of contacts is listed for each third party on the third-party contacts page.

2.  On the third-party contacts page, select a third party to view the list of associated contacts.

    -   To manage existing contacts:

        -   Select each contact to verify that the contact is associated with the appropriate third party, is active, and, if applicable, is specified as the primary contact.

            **Note:** The questionnaires, document requests, and issues that are currently assigned to the contact are listed in the associated tab.

        -   If you don't have the admin role, ask a user who does to verify that the vendor\_contact role appears for the user on the Roles related list. If the user with the admin role can't see the Roles related list, they have to go to step 4. If the user with the admin role can't see the vendor\_contact role listed for the user, they have to go to step 5.
        **Note:** For more information on managing third-party contacts, see [Manage the access for your third-party contacts](../../grc-vendor-risk/task/tprm-manage-tp-contact.md).

    -   To add a contact, select **New** and continue with the following steps.
    **Note:** It’s normal for a contact to have the snc\_external role because the vendor\_contact role includes it.

3.  On the form, fill in the fields.

<table id="table_yng_2dk_dzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

First name, Last name, Email, Title, Department

</td><td>

Standard contact information for the user at the third-party organization.

</td></tr><tr><td>

User ID

</td><td>

ID used to log in to the Third-party portal instance.

</td></tr><tr><td>

Third-party

</td><td>

Third-party organization of the contact.

</td></tr><tr><td>

Language, Time Zone

</td><td>

Preferred language and time zone for the user at the third-party organization.

</td></tr><tr><td>

Active

</td><td>

Option to activate the contact to be eligible to work in the Third-party portal.

</td></tr><tr><td>

Primary contact

</td><td>

Third-party contact who can directly answer assessment questions or assign another contact at the third party to answer the questions. They can also manage other contacts for the third party.

</td></tr></tbody>
</table>    **Note:** An email notification is sent out to the new third-party contact after the form is submitted. The email contains a link to the third-party portal and login credentials.

4.  Validate that each contact has the vendor\_contact role by adding the **Roles** value to the Vendor Contact page.

    1.  Add the Roles related list by selecting the actions icon and selecting **Configure** &gt; **Related Lists**.

        ![Adding a related list to the form.](../image/vrm-vendor-contact-menu.png)

    2.  Move the Roles related list to the Selected list and then select **Save**.

        ![Adding the Roles heading to the related list.](../image/vrm-vendor-contact-form.png)

5.  Grant third-party contacts access to the third-party portal by selecting **Edit** and adding **vendor\_contact** to the Roles list.

    ![Assigning the vendor_contact role to a third-party contact.](../image/vrm_add_vendor_contact_role.png)

    **Warning:** If the user has other roles, such as snc\_internal, then the user might also be able to log in to your platform and have visibility into critical records.


