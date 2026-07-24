---
title: Configure install base item
description: Create and configure install base item records to track sold products and assets associated with customer accounts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/manufacturing/mco-create-install-base-item.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Initial setup, Configure, Manufacturing Commercial Operations]
---

# Configure install base item

Create and configure install base item records to track sold products and assets associated with customer accounts.

## Before you begin

Role required: admin or sn\_customerservice\_manager

## About this task

Install base items represent the products and assets sold to customers. Each install base item links to a corresponding asset record and maintains critical customer and service organization information. Setting up accurate install base items enables proper asset tracking and service delivery.

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **CSM/FSM Configurable Workspace.**

2.  Select the List icon.

3.  Navigate to **MCO Setup** &gt; **Install Base Items**.

4.  Select **New**.

5.  On the Install based item form, fill in the fields.

    For a description of the field values, see [Install based item form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/install-based-item-form.md).

6.  Select **Save**.

    The Sold Products, Entitlements, and Cases related lists are displayed.

7.  Fill out the related lists as described in the following table.

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
</table>    For more information on the related lists, see .

8.  Select **Update**.

    For more information on importing install base items, see .


## Result

The install base item is added to the account or consumer that you selected. You can select an account or consumer to see a list of all the install base items that are related to the account or consumer.

**Related topics**  


[bundle-csm.install-base-item]

