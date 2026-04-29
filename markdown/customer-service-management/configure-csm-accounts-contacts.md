---
title: Configure accounts and contacts
description: An account is a supported external customer and a contact is a user who is an employee of an account.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customer data, Set up your environment, Configure, Customer Service Management]
---

# Configure accounts and contacts

An account is a supported external customer and a contact is a user who is an employee of an account.

## Before you begin

Role required: One of the following roles:

-   sn\_crm\_account\_data\_manager
-   sn\_crm\_account\_relationship\_data\_manager
-   sn\_crm\_foundation\_data\_manager
-   sn\_crm\_foundation\_admin
-   admin

## About this task

There are two types of accounts: customer accounts and partner accounts. The **Customer** and **Partner** fields on the Account form denote the account type. An account can be a customer account, a partner account, or both.

A partner is a supported external customer that sells to and supports other customers. A partner can report and manage cases on behalf of customers. A partner can also be a customer.

**Note:** After importing customer account data, you must also [set the account code system property](../reference/set-csm-account-code-property.md).

An account can have multiple contacts but a contact can be associated with only one account. A contact can have one or more associated assets and service contracts. A contact can also have a user ID and can log in to the customer portal.

**Note:** A contact is a user in the system. If you create a contact, that person is also added to the User table \(sys\_user\).

## Procedure

-   You can import existing accounts and contacts using guided setup.

-   You can create accounts and contacts using the Customer Service Management application.


