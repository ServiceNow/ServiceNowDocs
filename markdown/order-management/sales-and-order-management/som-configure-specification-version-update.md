---
title: Configure update specification versions
description: Configure specification version updates so that product specification versions can be updated to reflect changes and updates.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Updating specification versions, Specifications and product offerings, Product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Configure update specification versions

Configure specification version updates so that product specification versions can be updated to reflect changes and updates.

## Before you begin

Role required: system\_catalog\_admin

## About this task

To configure the product specification version change, modify the check-for-an-incoming-specification ID and the product inventory specification ID.

## Procedure

1.  Navigate to **All** and enter `sys_properties.list` in the search area to open the **System Properties** list.

2.  In the **System Properties** list, search for `sn_ind_tmt_orm.allowSpecVersionUpdateInChangeOrder` then select to open the system property.

    If the system property record is in an uneditable state, select the message to make the record editable.

3.  In the **Value** field, set the value to `true`.

4.  Select **Update**.

    The specification version update is activated.


**Parent Topic:**[Updating specification versions](../concept/som-specification-version-update.md)

