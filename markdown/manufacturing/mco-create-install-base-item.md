---
title: Create an install base item
description: Create an install base item that represents the instance of the product that has been configured for a customer The install base item enables you to track all the purchases that were made by a customer.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up Manufacturing Commercial Operations, Configure, Manufacturing Commercial Operations]
---

# Create an install base item

Create an install base item that represents the instance of the product that has been configured for a customer The install base item enables you to track all the purchases that were made by a customer.

## Before you begin

Verify that the Customer Service Install Base Management plugin \(com.snc.install\_base\) is installed.

Role required: admin

## About this task

Install base items help to track instances that have been provisioned for an account or customer. An install base item can be any configuration item that has been made accessible to customers. The install base item enables you to track all the purchases that were made by a customer.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** &gt; **Lists** &gt; **MCO Setup** &gt; **Install Base Items**.

2.  Select **New**.

3.  On the Install based item form, fill in the fields.

    For a description of the field values, see [Install based item form](../reference/install-based-item-form.md).

4.  Select **Save**.

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

Entitlements

</td><td>

List of entitlements that are associated with an install base item. Add an entitlement for the install base item by selecting **New**. **Note:** Customer service managers can create entitlements. Customer service agents can view entitlements.

</td></tr><tr><td>

Contracts

</td><td>

List of contracts that are related to an install base. Edit a contract by selecting **Edit**.

</td></tr></tbody>
</table>    For more information on the related lists, see [Related list for an install base item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/install-base-related-list.md).

6.  Select **Update**.


## Result

The install base item is added to the account or consumer that you selected. You can select an account or consumer to see a list of all the install base items that are related to the account or consumer.

**Related topics**  


[Install base items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/install-base-item.md)

