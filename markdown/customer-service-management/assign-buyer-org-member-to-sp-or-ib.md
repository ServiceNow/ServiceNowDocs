---
title: Assign a buyer organization member to sold products or install base items
description: Assign a business organization member to a sold product or install base item so that the member can raise cases for the asset on the Business Location Service Portal \(BLSP\) or in workspaces.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/assign-buyer-org-member-to-sp-or-ib.html
release: australia
product: Customer Service Management
classification: customer-service-management
topic_type: task
last_updated: "2026-06-04"
reading_time_minutes: 1
breadcrumb: [Create a business location, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Assign a buyer organization member to sold products or install base items

Assign a business organization member to a sold product or install base item so that the member can raise cases for the asset on the Business Location Service Portal \(BLSP\) or in workspaces.

## Before you begin

The member must already exist as a business organization member at the location.

Role required: sn\_customerservice.svc\_location\_manager\_core or admin

## About this task

You can assign a buyer organization member from the following locations:

-   Install base item or sold product record
-   BLSP portal: Business Organization details page on the Products or Install Base tab
-   Workspace: Install base or sold product view

All locations opens the same Assign Buyer Organization Member dialog and produce the same outcome.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Business Organizations** &gt; **Internal Organizations**.

2.  Select an internal or external organization record.

3.  Select the desired record from the install base or sold product related lists tab where you want to assign a member.

4.  Select **Assign Member** form the install base record.

5.  Select the **Buyer Organization Member** from the Assign Buyer Organization Member dialog box.

    The lookup is filtered to members of the same business organization; members of other organizations are not selectable.

6.  Select **Save**.


## Result

The Buyer Organization Member field on the record is populated.

**Note:**

For install base items, if you assigned the member to a parent install base item, the Buyer Organization Member field on every child install base item is also populated.

