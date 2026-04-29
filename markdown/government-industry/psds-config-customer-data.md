---
title: Configuring Public Sector Digital Services customer data
description: Customer data constitutes the data linked to a case using associated entities such as Accounts, Contacts, Constituents, Household, Products, and Service Contracts. This information provides the government service agent the information necessary to resolve constituent issues.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up your environment, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configuring Public Sector Digital Services customer data

Customer data constitutes the data linked to a case using associated entities such as Accounts, Contacts, Constituents, Household, Products, and Service Contracts. This information provides the government service agent the information necessary to resolve constituent issues.

The following list is a list of key entities in the Public Sector Digital Services foundational data model.

-   **Constituent**

    A constituent is a customer in the business-to-consumer \(B2C\) business model.

-   **Contacts**

    A contact is an employee of an account and can be associated with only one account. Contacts can have multiple assets and service contracts, can have one or various roles associated with them, and has a user ID and can log in to the Government Service Portal, as well as view and work from the consumer instance in Service Bridge for Public Sector Digital Services \(PSDS\).

    An employee of a company is an example of a contact.

    A contact record stores information about a contact, such as the name, phone number, and email address. Contact information is stored in the Contact \[customer\_contact\] table.

-   **Applicants**

    In the Social Benefits, License and Permits, and Grants Management space, an applicant is a user that applies for a grant, license and permit, or social benefit using the Government Service Portal.

-   **Households**

    A household is a group of constituents who live at the same address and share products and services. A household can have a designated head of household and multiple current members. The head of household has access to all cases and information for the other household members.

    Household information is stored in the Household table, and also includes the relationships between household members.

    For more information on households in Public Sector, see [Configure households in Public Sector Digital Services](psds-config-customer-data-household.md).


