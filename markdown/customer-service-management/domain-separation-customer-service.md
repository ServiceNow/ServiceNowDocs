---
title: Domain separation and Customer Service Management
description: Domain separation is supported in Customer Service Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Administer Customer Service Management, Customer Service Management]
---

# Domain separation and Customer Service Management

Domain separation is supported in Customer Service Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## Overview

Domain separation for Customer Service Management is designed for:

-   **Customers using the application in a domain-separated environment or in a hybrid environment**. With domain separation, a customer can grant access to end users \(contacts or consumers\) to other entities in addition to customer service cases. For example, contacts or consumers can access problems, changes, or projects. Administrators can synchronize the CSM account model with the domain structure and maintain data separation for entities that don’t have account-based data separation enabled.
-   **Managed service providers \(MSPs\) using the application to provide customer support**. In this scenario, an MSP can provide support to multiple customers, where domains are necessary to contain all relevant customer data and processes. For example, an MSP providing support to customers related to billing questions, contract renewals, or other non-service operations.
-   **Managed service providers offering the application as a service that customers can provide to their customers**. In this scenario, an MSP can offer Customer Service Management as a service to customers who, in turn, use the application to support their end customers. This scenario requires additional configuration due to domain support for some of the core entities in the platform such as Product Model.

## How domain separation works in Customer Service Management

Domain separation for Customer Service Management aligns each customer account to one domain. To use domain separation with the application, all customer accounts must be assigned to a domain.

The customer account is the main entity within Customer Service Management. All entities related to the account, such as contacts and cases, are created in the same domain as the account. This rule also applies for all entities on customer service cases, including addresses, assets, and contacts.

When a new account is created, a domain of the same name is also created and assigned to the account. All related entities for an account, such as contacts and cases, must reside in the same domain. When a related entity for a domain-separated account is created, the entity is assigned to the account domain.

## Setting up domain separation for Customer Service Management

Domain separation for Customer Service Management requires the domain separation plugin. Contact ServiceNow to activate domain separation.

Domain separation for Customer Service Management also requires enabling the **csm\_auto\_account\_domain\_generation** property. This property is installed with Customer Service Management and is available only after the domain separation plugin is active. Contact ServiceNow to enable this property.

When the **csm\_auto\_account\_domain\_generation** property is enabled, the Customer Service Management application automatically creates a domain of the same name when a new account is created.

**Note:** Enabling the **csm\_auto\_account\_domain\_generation** property doesn’t add domains for existing accounts. It only creates domains for newly created accounts. Adding domains for existing accounts requires a migration script. You can request for the migration script from the ServiceNow Professional Services team.

## Changes to Customer Service Management tables

Domain separation for Customer Service Management adds the **Domain** and **Domain Path** fields to the Account \[customer\_account\] table. These fields aren’t exposed by default. Customers can customize lists and forms to view these fields.

## Account domains and related entities

When creating related entities for an account, the domain for the related entities is set to the account domain. Related entities include:

-   Contacts
-   Cases
-   Assets
-   Contracts
-   Entitlements
-   Addresses
-   Social profiles
-   Escalations
-   Sold Products
-   Installed Products
-   Install Base Items
-   Affected Install Base Items
-   Sold Product Covered

Changing the domain for an account also changes the domain for all the account’s related entities.

## Domain visibility for customer service agents and managers

Users with the customer service agent \(sn\_customerservice\_agent\) and customer service manager \(sn\_customerservice\_manager\) roles must be manually assigned to the **TOP/MSP/Default** domain. Agents and managers can’t see case or account details until they’re assigned to the **TOP** domain.

## Domain separation for case and account escalation

Escalation template records and escalation severity records are domain separated. By default, these records reside in the global domain. Users can configure the Escalation Template and Escalation Severity forms to display the **Domain** field and set the domain as needed.

When an escalation record is created from a case or account, it’s created in the account domain.

## Domain separation for ribbon configuration, Lookup and Verify configuration, and Special Handling Notes

Ribbon and Lookup Verify configurations and Special Handling Notes support domain separation as process-separated tables.

When inserting or updating a record for process-separated tables, the picker domain scope takes precedence by design with the Overrides \[sys\_override\] field on process-separated tables. For more information, see [Process administration](https://www.servicenow.com/docs/access?context=c_DelegatedAdministration&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

-   **[Domain separation and entity relationships](../reference/domain_separation_csm_accounts.md)**  
With domain separation in Customer Service Management, you can further control visibility and access to data by using contact, partner, and parent-child relationships.

**Parent Topic:**[Customer Service Management](c_CustomerServiceManagement.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

