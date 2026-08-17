---
title: Create and manage install base items for a business organization
description: As a staff member with the location agent role, create and manage install base items for your business organizations \(formerly business locations\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/create-ib-items-for-business-locations.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Business Organizations, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Create and manage install base items for a business organization

As a staff member with the location agent role, create and manage install base items for your business organizations \(formerly business locations\).

## Before you begin

Role required: sn\_customerservice\_manager, sn\_customerservice.svc\_location\_agent, or admin

## About this task

Staff members with the sn\_customerservice\_manager role, create install base items by choosing the correct configuration item. Whereas the staff members with the sn\_customerservice.svc\_location\_agent role, can view the list of install base items installed at any service organization.

**Important:** Some table and field labels have been changed across recent releases. For a mapping of former labels to current labels, see [Service Model Foundation renamed Entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/renamed-entities.md).

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Business Organizations** &gt; **Internal/External Organizations**.

2.  Select either an internal or external organization \(formerly internal or external business location\).

3.  In the Install Base Item related lists, select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Number|Unique ID of the install base item. The system automatically sets this field value, but you can change it.|
    |Name|Name of the install base item.|
    |Configuration Item|If the sold product contains child components, reference it to another sold product.|
    |Buyer Organization \(formerly Service Organization\)|Internal or external entity that is involved in providing service to the customer.|
    |Owned by|Business manager of the install base item.|
    |Supported by|Configuration item supported by.|

5.  Select **Submit**.

    An install base item record is created for the selected business organization.


**Related topics**  


[Create an install base item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/create-install-base-item.md)

