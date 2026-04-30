---
title: Financial Services Operations Core
description: The Financial Services Operations \(FSO\) Core application provides a framework to enable financial institutions to organize and manage their data effectively to meet their business needs. This section introduces FSO Core and explains its purpose and key data design components.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-26"
reading_time_minutes: 2
---

# Financial Services Operations Core

The Financial Services Operations \(FSO\) Core application provides a framework to enable financial institutions to organize and manage their data effectively to meet their business needs. This section introduces FSO Core and explains its purpose and key data design components.

## Introduction to FSO Core

The Financial Services Operations Core data model enhances and utilizes tables from the ServiceNow AI Platform and the Customer Service Management \(CSM\) application to create a streamlined data environment. It organizes information into two main categories:

-   Foundational Data: This includes tables that store essential customer information such as financial accounts, product models, and transactions. These elements are crucial for handling customer service requests.
-   Operational Workflow Data: This records data generated during the execution of related processes, such as creating tasks and cases.

![Diagram illustrating the high-level data model of the FSO Core, detailing its extensions from CSM and Platform.](../../fso-complaints-mgmt/image/intro-fso-core.png "High-level overview of the FSO Core")

## Key components in Financial Services Operations Core

The Financial Services Operations Core feature includes the following key data design components or models.

<table id="table_ky1_wy4_dmb"><thead><tr><th>

Model

</th><th>

Definition

</th><th>

Examples

</th></tr></thead><tbody><tr><td>

Service organizations

</td><td>

A list of all branches and agencies within an organization. It includes the internal and external entities that belong to a service organization.

</td><td>

-   Financial service organizations with multiple branches
-   Internal or external insurance agents and agencies
-   Stores
-   Branches
-   Centers
-   Franchises
-   Dealerships

</td></tr><tr><td>

Customer

</td><td>

A list of all customers served by the organization.

</td><td>

-   Accounts
-   Contacts
-   Consumers
-   Households

</td></tr><tr><td>

Product/Sold product

</td><td>

A list of all products offered by the organization. Tracks the products or services sold to an account or consumer, linking them to financial accounts, insurance policies, and financial services.

</td><td>

-   Chase Total Checking
-   Chase Sapphire Credit Card
-   Auto Insurance
-   Life Insurance
-   Home Insurance

</td></tr><tr><td>

Financial Account

</td><td>

Represents the financial products owned by clients, such as deposits, line of credit, loans, cards, and investments. It connects these products to the account owner and supports integration with core systems.

</td><td>

-   Savings account number at your bank
-   Home insurance policy number at your insurance company.

</td></tr><tr><td>

Financial Services

</td><td>

Captures the treasury services a customer has enabled for a specific Financial Account.

</td><td>

-   Wired services
-   Standing sweep services on a financial account

</td></tr></tbody>
</table>-   **[Understanding FSO Core relationships](fso-core-relationships.md)**  
This section describes the key tables in FSO Core and their relationships. Understanding these relationships helps you manage data effectively and enhances system functionality.
-   **[FSO Core Banking tables](fso-core-banking-tables.md)**  
This section describes the banking tables in FSO Core and shows how they store and manage banking information.
-   **[FSO Core Insurance tables](fso-core-insurance-tables.md)**  
This section explains the insurance tables in FSO Core and how they handle insurance data.

**Parent Topic:**[Data Model](data-models.md)

