---
title: Configuring a contact relationship
description: You can configure a contact relationship to establish a relationship between an account and a contact in the Customer Service Management \(CSM\) application.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Contact relationships, Create customer relationships, Configure accounts and contacts, Customer data, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Configuring a contact relationship

You can configure a contact relationship to establish a relationship between an account and a contact in the Customer Service Management \(CSM\) application.

## Configuring the contacts to be associated with an account

When you create a contact relationship, you select a user from the **Contact** field. This field displays the contacts from:

-   All accounts in the account relationship
-   All accounts in the account hierarchy
-   All accounts, if the **sn\_customerservice.contact\_relationship.restrict\_within\_account\_hierarchy** system property is set to **false**. However, when the **sn\_customerservice.contact\_relationship.restrict\_within\_account\_hierarchy** system property is set to **true**, only the contacts within the account hierarchy and account relationship are displayed.

    **Note:** By default, the **sn\_customerservice.contact\_relationship.restrict\_within\_account\_hierarchy** system property is set to **true**.


If you're a customer service manager \(sn\_customerservice\_manager\), you can create, update, delete, and view the list of contact relationships for an account. If you're a customer service manager \(sn\_customerservice\_manager\) or a customer service agent \(sn\_customerservice\_agent\), you can view a list of the contact relationships for an account.

When you select a responsibility for the contact, the responsibilities that are available are those responsibility definitions that are created with a type of **Contact**.

**Note:** A contact can only be assigned with one responsibility per account.

## Configuring multiple contact relationships per account for a contact

Before the Vancouver release, configuring multiple contact relationships for a contact with an account wasn’t enabled. The database-level unique index `company_contact` can be turned off only by the administrators.

Starting with the Vancouver release, the Customer Service Management \(CSM\) application replaced the unique index and introduced the **Prevent duplicate for account-contact** business rule. This business rule enables administrators to disable the restriction of a unique index combination in the contact relationship by setting the **Active** flag to **False**. As a result, an administrator can assign multiple responsibilities per account for a contact.

