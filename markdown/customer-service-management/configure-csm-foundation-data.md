---
title: Configure foundation data
description: With Customer Service Management, you can import or create customer information including names, addresses, and phone numbers; account details; products and assets; and service contracts. You can also assign roles to users and create customer relationships.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Getting started with Customer Service Management, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Configure foundation data

With Customer Service Management, you can import or create customer information including names, addresses, and phone numbers; account details; products and assets; and service contracts. You can also assign roles to users and create customer relationships.

## Before you begin

Role required: admin

## About this task

Foundation data includes all of the data that you need to configure in order to support your customers. This includes information about:

-   Customers \(external users\)
-   Customer relationships
-   Users \(internal users such as agents and employees\)
-   Customer and user roles
-   Products and assets
-   Service contracts and entitlements

You can import and configure most of this foundation data using the Customer Service Management guided setup. This feature takes you through the entire setup and configuration process.

To create new data, such as adding new accounts and contacts, you can use the Customer Service Management application.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Guided Setup**.

2.  On the Getting Started page of the guided setup, click **Get Started**.

    The guided setup reopens with a page of different categories of Customer Service Management features that you can configure.

3.  In the Foundation Data category, click **Get Started**.

    The Foundation Data page opens with a list of tasks to configure the different types of customer information.

4.  To perform a task, click **Configure**.

<table id="table_tth_54l_mlb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Import Accounts

</td><td>

In the business-to-business \(B2B\) model, an account is a supported external customer. Import and verify existing account data. For more information, see [Import accounts and contacts with guided setup](configure-csm-accounts-contacts.md#).**Note:** After importing customer account data, you must also [set the account code system property](configure-csm-accounts-contacts.md#).

</td></tr><tr><td>

Import Contacts \(B2B\)

</td><td>

A contact is a user who is an employee of an account. Import and verify existing contact data. For more information, see [Import accounts and contacts with guided setup](configure-csm-accounts-contacts.md#).

</td></tr><tr><td>

Import Consumers \(B2C\)

</td><td>

A consumer is a customer in the business-to-consumer \(B2C\) business model. Import and verify existing consumer data. For more information, see [Import consumers with guided setup](configure-csm-consumers.md#).

</td></tr><tr><td>

Import Users

</td><td>

A user is an individual who can access your instance. Import and verify existing user data. For more information, see [Configure users and groups](configure-csm-users-groups.md).

</td></tr><tr><td>

Import Groups

</td><td>

A group is a set of users who share a common purpose. Import and verify existing group data. For more information, see [Configure users and groups](configure-csm-users-groups.md).

</td></tr><tr><td>

Import Group Members

</td><td>

The users associated with a group are listed as group members. Import and verify existing group member data.

</td></tr><tr><td>

Assign Roles

</td><td>

Roles control access to features and capabilities. The Customer Service Management application provides two types of roles:

-   Internal roles for agents and managers
-   External roles for customers, customer partners, and consumers
 Assign the necessary roles to internal and external users. For more information, see [Assign roles to CSM users](assign-csm-roles.md).

</td></tr><tr><td>

Create Customer Relationships

</td><td>

Create relationships between partners, contacts, and customers to make account and asset management easy and flexible. For more information, see [Create customer relationships](../concept/c_CustomerServiceRelationships.md).You can create the following types of relationships:

-   Bi-directional account relationships
-   Account hierarchy
-   Contact relationships


</td></tr><tr><td>

Import Product Models

</td><td>

A product is a type of good or service that your company sells and supports. Product models identify different types of products, such as service, hardware, software, or consumables. For more information, see [Import product models with guided setup](import-csm-product-models.md).

</td></tr><tr><td>

Import Sold Products

</td><td>

Sold products are products and components that have been sold to an account or a consumer. Importing sold products provides an overview of the complete product sold to an account or consumer. For more information, see [Import sold products with guided setup](import-csm-sold-products.md).

</td></tr><tr><td>

Create product model and catalog items relationships

</td><td>

Enable self-service for customers to request services on products by creating relationships between product models and catalog items. For more information, see [Configure product model and catalog item relationships](create-csm-product-model-items.md).

</td></tr><tr><td>

Import Install Base Items

</td><td>

Install base items represent the instances that have been configured for a customer. Each install base item references the configuration item record for the customer. For more information, see [Import install base items with guided setup](import-csm-install-base-items.md).

</td></tr><tr><td>

Import Installed Products

</td><td>

Installed products create an association between sold products and install base items. Installed products also provide information on the sold products and how they are deployed or installed. For more information, see [Import installed products with guided setup](import-csm-installed-products.md).

</td></tr><tr><td>

Import Assets

</td><td>

An asset is a specific product or instance that is supported for a customer. There are different types of assets and Information for each type of asset is stored in a different table. For more information, see [Import assets with guided setup](import-csm-assets.md).

</td></tr><tr><td>

Create Asset Contact Relationships

</td><td>

Assign assets to the customer contacts who are responsible for managing those assets. If desired, enable a property that limits access to asset information to just the assigned contacts. For more information, see [Create asset contact relationships](../concept/c_AssetContactRelationships.md#).

</td></tr><tr><td>

Create Service Contracts

</td><td>

A service contract contains information about the type of support that is provided to a customer and can include coverage for specific assets. It can also include multiple service entitlements and SLAs. For more information, see [Create service contracts](create-csm-service-contracts.md).

</td></tr><tr><td>

Create Entitlements

</td><td>

An entitlement defines the type of support that a customer receives as well as the supported communication channels. Entitlements are counted and tracked using two types of units: cases and hours. For more information, see [Configure entitlements](configure-csm-entitlements.md).

</td></tr><tr><td>

Create Account Teams

</td><td>

Account teams are made up of employees who fulfill specific jobs or roles for a particular account. Create these roles, or responsibility definitions, and then assign them to employees and contacts. For more information, see [Creating an account team](../concept/configure-csm-account-teams.md).

</td></tr></tbody>
</table>
