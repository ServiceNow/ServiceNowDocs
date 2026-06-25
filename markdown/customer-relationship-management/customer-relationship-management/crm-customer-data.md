---
title: Customer data
description: Configure and manage the core customer records, accounts, contacts, consumers, households, and billing accounts, that agents, sales teams, and technicians rely on across the CRM portfolio. Because customer data is shared across all CRM products, a record created in one context is immediately available in another without duplication or manual transfer.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-28"
reading_time_minutes: 6
---

# Customer data

Configure and manage the core customer records, accounts, contacts, consumers, households, and billing accounts, that agents, sales teams, and technicians rely on across the CRM portfolio. Because customer data is shared across all CRM products, a record created in one context is immediately available in another without duplication or manual transfer.

## Customer data entities

Customer data in the CRM portfolio consists of information about the people and organizations your business serves, along with the financial entities that manage billing and payments. The following entities form the core of the customer data model.

|Entity|What it represents|Key characteristics|
|------|------------------|-------------------|
|Account|A customer or partner organization that your business serves or works with.|Functions as a customer account, partner account, or both. Supports hierarchical parent-child relationships across the organization.|
|Contact|An individual employee of an account who interacts with your service organization.|Belongs to one account. Can be associated with multiple assets and service contracts. Can log in to the Customer Service Portal.|
|Consumer|An individual customer in a B2C service model.|Operates independently of a business account. Interacts with the organization through self-service portals or assisted service channels.|
|Household|A group of consumers who share an address and common products or services.|Groups consumers under a designated head of household. Provides visibility into cases and account information for all members.|
|Billing account|A financial entity that manages payment and invoicing for services, separate from the customer relationship.|Allows multiple billing arrangements per customer and consolidated billing across customers. Supports parent-child hierarchies for complex billing structures.|

## Account structure and relationships

Customer data entities are connected through a set of relationships that control visibility, access, and management responsibilities across the CRM portfolio. These relationships determine which users can see which records, who can act on behalf of whom, and how organizational structures are represented in the system.

The following table summarizes every relationship type available in the customer data model.

|Relationship type|What it connects|What it enables|
|-----------------|----------------|---------------|
|Account hierarchy|Parent account to child accounts.|Represents the legal entity structure. Gives parent account administrators visibility and management access across all child accounts, contacts, cases, and assets.|
|Account relationship|Account to account or account to partner.|Creates bi-directional relationships between accounts. Allows partner accounts to manage cases and view assets on behalf of customer accounts.|
|Contact relationship|Contact to an account other than their own.|Associates a contact with additional accounts beyond their primary account. Enables the contact to view information and perform actions on behalf of associated accounts through the customer portal.|
|Account team|Employees and contacts to a specific account.|Assigns responsibility definitions \(roles\) to internal employees and customer contacts who support a particular account. Built using the responsibility definition framework.|
|Consumer relationship|Consumer to consumer.|Creates an authorized representative relationship between two consumers. The authorized representative can manage cases on behalf of the other consumer.|
|Consumer team|Agent to consumer.|Creates a relationship manager relationship between an agent and a consumer. The agent can access and manage all cases for that consumer.|
|Household relationship|Consumer to household.|Adds consumers as members of a household. A consumer can belong to multiple households with one designated as primary. Supports head of household and relationship manager roles.|
|Asset contact relationship|Asset to contact.|Assigns specific assets to one or more customer contacts. When enabled, restricts asset visibility on the customer portal to only the assigned contacts.|

## Account hierarchy

Accounts can be organized into a parent-child hierarchy to reflect the legal or operational structure of a customer organization. A parent account provides visibility across all child accounts, allowing customer administrators to view and manage cases, contacts, and assets at any level of the hierarchy.

Each account is assigned a unique account code, and the hierarchy is tracked through an account path that combines the account codes of each account in the chain. For example, a parent company with two regional subsidiaries produces three account paths: the parent’s own code, and a parent/child path for each subsidiary.

## Account relationships

Account relationships create bi-directional links between accounts. Each relationship has a defined type \(such as “Partner of”\) and an automatic reverse relationship on the target account \(such as “Customer of”\). These relationships allow partner accounts to report and manage cases on behalf of customer accounts, view associated assets, and coordinate service delivery.

Account relationship types are defined by the administrator and can link a customer account to another customer account, a customer account to a partner, or a partner to a partner. Deleting a relationship record automatically deletes the reverse relationship. Existing customer service cases that reference the relationship are not affected.

## Contact relationships

A contact belongs to one account, but contact relationships allow that contact to be associated with additional accounts. Through a contact relationship, a contact with the customer or customer administrator role can view information and perform actions, such as creating or updating cases from the customer portal, on behalf of the associated accounts.

When creating a contact relationship, the available contacts include those from any related partner or account, as well as contacts from the account hierarchy. Each contact relationship includes a responsibility that defines the contact’s role for that account. Starting with the Zurich release, administrators can assign multiple responsibilities per account for a single contact.

## Account teams

Account teams bring together employees and customer contacts who fulfill specific roles in supporting a particular account. Teams are built using responsibility definitions, named roles that the administrator creates and assigns to team members.

There are two types of responsibility definitions: one for employees \(internal users\) and one for contacts \(external users\). Once definitions are created, the customer service manager assigns them to specific users for each account. Team members appear in the Account Team Members related list on the account record. An account team member assigned an account manager responsibility can view information and perform actions on behalf of the account through the customer portal.

## Consumer relationships

Consumer relationships connect individual consumers to each other or to agents who manage their cases. Two types of consumer relationships are available:

-   Consumer-to-consumer relationships use the authorized representative responsibility. A consumer with this relationship can manage cases on behalf of the other consumer, regardless of whether they share a household.
-   Consumer team relationships use the relationship manager responsibility. An agent with this relationship can access and manage all cases for that consumer.

## Household relationships

A household groups consumers who share an address and common products or services. A consumer can belong to multiple households, with one designated as the primary household. Each household can have a designated head of household who has access to all cases and information for the other household members.

Household relationships also support household teams, which are relationships between an agent and a household created using the relationship manager responsibility. Agents with this relationship can manage all cases for that household. When a household is deleted, the system clears references and associations to the household but does not delete the associated consumers, cases, or work orders.

## Asset contact relationships

Asset contact relationships assign specific assets to one or more customer contacts who are responsible for managing those assets. By default, all account and partner contacts can see all assets related to an account. To restrict visibility, administrators create asset contact relationships and enable the associated system property.

When enabled, asset visibility on the customer portal is limited to the assigned contacts: the My Assets list shows only assigned assets, and the Asset field on the Create Case form shows only assets for which the user is a contact. Asset contacts can be selected from the account that owns the asset, the partner of that account, or any contacts added through contact relationships.

**Related topics**  


[Data models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/data-models.md)

[User management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/user-management.md)

[Product data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/product-data.md)

[Customer data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-data.md)

[Configure Service Model Foundation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-industry-data-model.md)

