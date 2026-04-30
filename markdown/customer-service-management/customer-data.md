---
title: Customer data
description: Customer data for Customer Service Management \(CSM\) consists of information about people who aren’t part of your organization, including accounts, contacts, consumers, and households.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up your environment, Configure, Customer Service Management]
---

# Customer data

Customer data for Customer Service Management \(CSM\) consists of information about people who aren’t part of your organization, including accounts, contacts, consumers, and households.

-   **Accounts**

    An account is a customer or a partner who sells to and supports other customers. Accounts can be customer accounts, partner accounts, or both, and their information is stored in the Account \[customer\_account\] table.

    There are two types of accounts: customer accounts and partner accounts.

    -   A partner is a supported external customer that sells to and supports other customers. A partner can report and manage cases on behalf of customers. A partner can also be a customer.
    -   An account can be a customer account, a partner account, or both. The **Customer** and **Partner** fields on the Account form denote the account type.
-   **Contacts**

    A contact is an employee of an account and can be associated with only one account. Contacts can have multiple assets and service contracts and can log in to the Customer Service Portal.

    Contact information is stored in the Contact \[customer\_contact\] table.

-   **Consumers**

    In the business-to-consumer \(B2C\) model, consumers are customers, and their information is stored in the Consumer \[csm\_consumer\] table.

-   **Households**

    A household is a group of consumers who live at the same address and share products and services. A household can have a designated head of household and multiple current members. The head of household has access to all cases and information for the other household members.

    Household information is stored in the Household \[csm\_household\] table.


