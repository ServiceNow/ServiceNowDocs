---
title: Create an install base item
description: Create an install base item in the Customer Service Management application that represents the instance of the product that has been configured for a customer. The install base item enables you to track all the purchases that were made by a customer.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Install base items, Configure install base, Configure product data, Product data, Set up your environment, Configure, Customer Service Management]
---

# Create an install base item

Create an install base item in the Customer Service Management application that represents the instance of the product that has been configured for a customer. The install base item enables you to track all the purchases that were made by a customer.

## Before you begin

Ensure that the Customer Service Install Base Management plugin \(com.snc.install\_base\) is installed.

Role required: sn\_customerservice\_manager or admin

## About this task

An install base item is any configuration item \(CI\) that has been made accessible to customers. For Software as a Service \(SaaS\) products, an install base item refers to an application service configuration item. Each install base item references the configuration item record for the customer. If issues arise with a configuration item, customer service agents can trace which install base items that the case is affecting.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Products** &gt; **Install Base Items**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_slg_dqz_pgb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique ID of the install base item. This field is automatically filled in, but you can change it.

</td></tr><tr><td>

Name

</td><td>

Name of the install base item.

</td></tr><tr><td>

Configuration Item

</td><td>

Configuration item that is associated with the install base item.The sn\_customerservice\_manager role must also have the app\_service\_user role to create the install base items for the Application Service configuration item class. For more information, see [Application services](https://www.servicenow.com/docs/access?context=application-services&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

Service models have a model category called the Application Service, which links a service model to the Application Service CI class. For more information, see [Models](https://www.servicenow.com/docs/access?context=c_Models&version=australia&pubname=australia-it-asset-management&ft:locale=en-US) and [Model categories](https://www.servicenow.com/docs/access?context=c_ModelCategories&version=australia&pubname=australia-it-asset-management&ft:locale=en-US).

</td></tr><tr><td>

Buyer Organization

</td><td>

Internal or external entity that is involved in providing service to the customer.**Note:** If you select a buyer organization, the **Account**, **Contact**, and **Consumer** fields are hidden. The **Buyer Organization** field is active only when the Service Organization \(com.snc.service\_organization\) plugin is installed.

</td></tr><tr><td>

Account

</td><td>

Account that is associated with the install base item.**Note:** If you enter an account, the **Consumer** field is hidden. The Consumer field is active only when the B2B2C plugin is installed.

</td></tr><tr><td>

Contact

</td><td>

Account contact that is primarily responsible for the install base item.

</td></tr><tr><td>

Consumer

</td><td>

Consumer that is associated with the install base item. **Note:** The Account field is hidden if the **Consumer** field is entered first.

</td></tr><tr><td>

Owned by

</td><td>

Business manager of the install base item. If the business manager is entered in the configuration item, this field is automatically filled in with the information from the configuration item.

</td></tr><tr><td>

Supported by

</td><td>

If the CI contains this information, this field is automatically filled in with the information from the configuration item.

</td></tr><tr><td>

Service Context

</td><td>

Service that is associated to the underlying CI for calculating the impact severity from Event Management. For more information, see [Service health status for install base](../concept/service-health-pcso.md).**Note:** This field is only available if you have the Proactive Customer Service Operations with Event Management plugin installed. The health status of an install base item appears only if an install base item has a CI and a service context that is associated to it.

Configure the form layout to add this field.

</td></tr><tr><td>

Parent install base item

</td><td>

Install base item that is the parent of the current install base item.

</td></tr><tr><td>

Root install base item

</td><td>

Install base item that is used to fetch the entire install base hierarchy in a single query.

</td></tr><tr><td>

Household

</td><td>

Household that is associated with the install base item.**Note:** This field is available only when the Customer Household Data Model \(com.snc.household\) plugin is installed.

</td></tr><tr><td>

Product

</td><td>

Product model that is associated with an install base and is used to identify the services that are associated with any product model.**Note:** A product model must have a single specification. The specification that is associated to the product model appears only on the install base form.

</td></tr><tr><td>

Location

</td><td>

Location that is associated with the product.

</td></tr><tr><td>

State

</td><td>

Current state of the Install base item and represents the various phases of the life cycle.**Note:** The state of the install base item determines the **Active** field and the **Uninstall date** field on the install base form.

</td></tr><tr><td>

Status

</td><td>

Option that determines whether the product is original or a replacement.

</td></tr><tr><td>

Life cycle stage

</td><td>

CSDM life cycle stage of an install base item.

</td></tr><tr><td>

Life cycle stage status

</td><td>

CSDM life cycle stage status of an install base item.

</td></tr><tr><td>

Active

</td><td>

Option that represents whether the install base is active or inactive. If the state is active, related cases for a product can be created.**Note:** A sync between the active state, install date, and uninstall date is always present. On the install base form, if the **State** is **In Use**, it means that the **Active** option is selected. The **Active** option remains unselected if the **State** is set to **Inactive**.

</td></tr><tr><td>

Install date

</td><td>

Date on which the install base becomes active.

</td></tr><tr><td>

Uninstall date

</td><td>

Date on which the install base becomes inactive.

</td></tr><tr><td>

Asset

</td><td>

Asset that is associated with an install base.

</td></tr><tr><td>

Specification

</td><td>

Specification that is associated with an install base item. Option that helps in fulfilling orders to create an install base item and its hierarchy.**Note:** The **Specification** field appears only to CSM agents, managers, and contributor persona.

</td></tr><tr><td>

Install base identifier

</td><td>

Identify finished goods in the system using their unique identifier.

</td></tr><tr><td>

Provider organization

</td><td>

The service organization that sells and supports the products or services owned by the customer.

</td></tr></tbody>
</table>    **Note:** In the List view of the install base item, you can filter the data by Condition, Active, Uninstall Date, and Asset.

4.  Right-click the form header and select **Save**.

    The Sold Products, Entitlements, and Cases related lists are displayed.

5.  Fill out the related lists as described in the following table.

<table id="table_zch_sgz_3hb"><thead><tr><th>

Related list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Child Install Base items

</td><td>

List of all child install bases that are related to the parent install base item.

</td></tr><tr><td>

Sold Products

</td><td>

List of the sold products that are associated with an install base Item. Edit a sold product by selecting **Edit**.

</td></tr><tr><td>

Cases

</td><td>

List of cases that are associated with an install base item.

</td></tr><tr><td>

All Cases

</td><td>

List of all cases that are related to an install base in the install base hierarchy.**Note:** The All Cases related list appears only when an install base hierarchy is added to the Install base item.

</td></tr><tr><td>

Entitlements

</td><td>

List of entitlements that are associated with an install base item. Add an entitlement for the install base item by selecting **New**. **Note:** Customer service managers can create entitlements. Customer service agents can view entitlements.

</td></tr><tr><td>

Contracts

</td><td>

List of contracts that are related to an install base. Edit a contract by selecting **Edit**.

</td></tr><tr><td>

Install Base Related Parties

</td><td>

List of contacts, consumers, accounts, members, contributors, and service organizations that have access to an install base. For more information on Install Base Related Parties, see [Create related party configurations](adding-related-party-config-to-case.md).

</td></tr></tbody>
</table>    For more information on related lists, see [Related list for an install base item](../concept/install-base-related-list.md).

6.  Select **Update**.

    The install base item is added to the account or consumer that you selected. You can select an account or consumer to see a list of all the install base items that are related to the account or consumer.

    **Note:** You can also create install base items directly from an account or a consumer.

    1.  Navigate to **Customer Service** &gt; **Customer** &gt; **Accounts** or **Customer Service** &gt; **Customer** &gt; **Consumer**.
    2.  Select an account or a consumer.
    3.  Select the Install Base Items related list.
    4.  Select **New**.

**Related topics**  


[Create and manage install base items for a business location](create-ib-items-for-business-locations.md)

