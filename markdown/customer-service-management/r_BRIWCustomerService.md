---
title: Business rules installed with Customer Service Management
description: Business rules are added with activation of Customer Service Management.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Components installed with Customer Service Management, Reference, Customer Service Management]
---

# Business rules installed with Customer Service Management

Business rules are added with activation of Customer Service Management.

The following table describes the business rules and their related tables that are added with Customer Service Management.

<table id="table_jhr_czw_kt"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Account query for customer

</td><td>

Account \[customer\_account\]

</td><td>

Queries the account for the customer contact.

</td></tr><tr><td>

Account relationship display rule

</td><td>

Account Relationship \[account\_relationship\]

</td><td>

Displays the correct values in the bi-directional diagram on the Account Relationship form.

</td></tr><tr><td>

Add customer role to contacts

</td><td>

Contact \[customer\_contact\]

</td><td>

Adds the customer role \(sn\_customerservice.customer\) to a customer contact if the contact has no assigned roles or if the user ID for the contact is set.

</td></tr><tr><td>

Add snc external role to contacts

</td><td>

Contact \[customer\_contact\]

</td><td>

Adds the snc\_external user role to each contact.

</td></tr><tr><td>

Add Primary Contact to Asset Contact

</td><td>

Asset \[alm\_asset\]

</td><td>

When an asset is assigned a new primary contact, the primary contact is added to the asset contact.

</td></tr><tr><td>

Approver query for customer

</td><td>

Approval \[sysapproval\_approver\]

</td><td>

Queries the approver for a customer contact.

</td></tr><tr><td>

Asset query for customer

</td><td>

Asset \[alm\_asset\]

</td><td>

Queries the assets for a customer contact.

</td></tr><tr><td>

Auto assessment business rule

</td><td>

Case\[sn\_customerservice\_case\]

</td><td>

Triggers a customer satisfaction survey when a case is set to **Closed**.

</td></tr><tr><td>

Case query for customer

</td><td>

Case \[sn\_customerservice\_case\]

</td><td>

Queries the cases for a customer contact.

</td></tr><tr><td>

Case display rule

</td><td>

Case\[sn\_customerservice\_case\]

</td><td>

A display business rule on the Case form which passes some values to the browser when a case is displayed.

</td></tr><tr><td>

Change Awaiting to Open

</td><td>

Case\[sn\_customerservice\_case\]

</td><td>

Changes the case state from **Awaiting Info** to **Open**.

</td></tr><tr><td>

Check duplicate

</td><td>

Asset Contact \[sn\_customerservice\_m2m\_asset\_contact\]

</td><td>

Checks for duplicate records before creating a new asset contact.

</td></tr><tr><td>

Check duplicate for responsibility

</td><td>

Contact Relationship \[sn\_customerservice\_contact\_relationship\]

</td><td>

Checks for duplicate responsibilities before creating a new contact relationship.

</td></tr><tr><td>

Check duplicate for responsibility

</td><td>

Asset Contact \[sn\_customerservice\_m2m\_asset\_contact\]

</td><td>

Checks for duplicate responsibilities before creating a new asset contact.

</td></tr><tr><td>

Check snc\_external roles exist

</td><td>

Contact \[customer\_contact\]

</td><td>

Checks if the com.glide.security\_schema plugin is activated.

</td></tr><tr><td>

Contact query for customer

</td><td>

Contact \[customer\_contact\]

</td><td>

Queries the contacts for a customer.

</td></tr><tr><td>

Contract query for customer

</td><td>

Contract \[ast\_contract\]

</td><td>

Queries the contracts for a customer.

</td></tr><tr><td>

Create bi-direction relationship

</td><td>

Account Relationship \[account\_relationship\]

</td><td>

After an account relationship is created, this business rule creates the bi-directional account relationship record.

</td></tr><tr><td>

Delete Account Contacts and Assets

</td><td>

Account Relationship \[account\_relationship\]

</td><td>

When an account relationship is deleted, this business rule deletes the corresponding account and asset contacts.

</td></tr><tr><td>

Delete relationship type

</td><td>

label \[account\_relationship\_type\]

</td><td>

Checks to see if any relationship records are using a relationship type before that relationship type is deleted.

</td></tr><tr><td>

Delete responsibility definition

</td><td>

Responsibility Definition\[sn\_customerservice\_responsibility\_def\]

</td><td>

Checks to see if any account team members are using a responsibility definition before that responsibility definition is deleted.

</td></tr><tr><td>

Display request message

</td><td>

Registration Request \[sn\_customerservice\_registration\]

</td><td>

After registration request submittal, shows info message to user

</td></tr><tr><td>

Display rule

</td><td>

Registration Request \[sn\_customerservice\_registration\]

</td><td>

Shows message to remind users to enter a correct registration code

</td></tr><tr><td>

Entitlement query for customer

</td><td>

Entitlement \[service\_entitlement\]

</td><td>

Queries the entitlements for a customer contact.

</td></tr><tr><td>

Insert Case Work Notes

</td><td>

Appointment \[sn\_customerservice\_appointment\]

</td><td>

Updates the case work notes with the appointment details when an an appointment is created.

</td></tr><tr><td>

Populate company for case

</td><td>

Case\[sn\_customerservice\_case\]

</td><td>

Populates the **Company** field on the Case form based on the name entered in the **Contact** field.

</td></tr><tr><td>

Set First Response Time

</td><td>

Case\[sn\_customerservice\_case\]

</td><td>

When a case is created or updated, this rule sets the current time in the first\_response\_time field. Also used when a case is set to **Resolved** or **Awaiting Info** or when comments or close notes are added. **Note:** The first\_response\_time field is not used.

</td></tr><tr><td>

Update account based on reg code

</td><td>

Registration Request\[sn\_customerservice\_registration\]

</td><td>

Validates the registration registration code and assigns the account associated with the registration code.

</td></tr><tr><td>

Update account relationship labels

</td><td>

Account Relationship Type\[sn\_customerservice\_account\_relationship\_type\]

</td><td>

When the labels for an account relationship type are updated, this business rule updates all of the related account relationship records.

</td></tr><tr><td>

Update case entitlement on Close

</td><td>

Case\[sn\_customerservice\_case\]

</td><td>

Updates the associated entitlement when the state of a case is set to **Closed**.

</td></tr><tr><td>

Update Case Work notes

</td><td>

Appointment\[sn\_customerservice\_appointment\]

</td><td>

Adds work notes to the case when an appointment for the case is updated.

</td></tr><tr><td>

Update Case Work Notes

</td><td>

Knowledge\[kb\_knowledge\]

</td><td>

Adds work notes to the case when a knowledge article associated with the case gets updated.

</td></tr><tr><td>

Update Parent Case for new task

</td><td>

Task\[sn\_customerservice\_task\]

</td><td>

Updates the case when a new case task is created.

</td></tr><tr><td>

Update Parent case for state change

</td><td>

Task\[sn\_customerservice\_task\]

</td><td>

Updates the case when a new case task is changed.

</td></tr><tr><td>

Update relationship label

</td><td>

Account Relationship \[account\_relationship\]

</td><td>

Updates the relationship labels for bi-directional account relationships.

</td></tr><tr><td>

Update User Task State

</td><td>

Case\[sn\_customerservice\_case\]

</td><td>

Calculates the work load for the agent based on the number of cases assigned to the agent. Also updates the last assigned time. This rule is used by the matching rule engine.

</td></tr><tr><td>

Validate registration

</td><td>

Registration Request\[sn\_customerservice\_registration\]

</td><td>

Checks if the registration is valid based on the user’s email address. If the user exists in the system or a request has already been submitted and is in the pending state, the registration request is not allowed.

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with Customer Service Management](r_InstalledWithCustomerService.md)

