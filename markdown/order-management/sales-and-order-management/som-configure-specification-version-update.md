---
title: Configure update specification versions
description: Configure specification version updates so that product specification versions can be updated to reflect changes and updates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/order-management/sales-and-order-management/som-configure-specification-version-update.html
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Updating specification versions, Create an order in Order Management, Using Order Management, Using Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Configure update specification versions

Configure specification version updates so that product specification versions can be updated to reflect changes and updates.

## Before you begin

Role required: system\_admin

## About this task

To configure the product specification version change, modify the check-for-an-incoming-specification ID and the product inventory specification ID.

## Procedure

1.  Navigate to **All** and enter `sys_properties.list` in the search area to open the **System Properties** list.

2.  In the **System Properties** list, search for `sn_ind_tmt_orm.allowSpecVersionUpdateInChangeOrder` then select to open the system property.

    If the system property record is in an uneditable state, select the message to make the record editable.

3.  In the **Value** field, set the value to `true`.

4.  Select **Update**.

    The specification version update is activated.


**Parent Topic:**[Updating specification versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/order-management/sales-and-order-management/som-specification-version-update.md)

