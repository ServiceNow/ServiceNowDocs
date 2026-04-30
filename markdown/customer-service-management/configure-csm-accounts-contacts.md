---
title: Configure accounts and contacts
description: An account is a supported external customer and a contact is a user who is an employee of an account.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Customer data, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Configure accounts and contacts

An account is a supported external customer and a contact is a user who is an employee of an account.

## Before you begin

Role required: admin

## About this task

There are two types of accounts: customer accounts and partner accounts. The **Customer** and **Partner** fields on the Account form denote the account type. An account can be a customer account, a partner account, or both.

A partner is a supported external customer that sells to and supports other customers. A partner can report and manage cases on behalf of customers. A partner can also be a customer.

**Note:** After importing customer account data, you must also [set the account code system property](../reference/set-csm-account-code-property.md).

An account can have multiple contacts but a contact can be associated with only one account. A contact can have one or more associated assets and service contracts. A contact can also have a user ID and can log in to the customer portal.

**Note:** A contact is a user in the system. If you create a contact, that person is also added to the User table \(sys\_user\).

## Procedure

-   You can import existing accounts and contacts using guided setup.

-   You can create new accounts and contacts using the Customer Service Management application.


