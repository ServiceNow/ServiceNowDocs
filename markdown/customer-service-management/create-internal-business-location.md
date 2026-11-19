---
title: Create an internal organization
description: Create an internal organization \(formerly internal business location\) to enable users and consumers to create accounts, contacts, consumers, and households.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/create-internal-business-location.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a business organization, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Create an internal organization

Create an internal organization \(formerly internal business location\) to enable users and consumers to create accounts, contacts, consumers, and households.

## Before you begin

Role required: admin

## About this task

A business organization \(formerly business location\) has a manager. When you create an internal organization , you add a user to the **Manager** field on the Internal Organization form. Users then added as internal organization managers are automatically assigned the sn\_customerservice.svc\_location\_manager\_contributor role.

However, to assign the sn\_customerservice.svc\_location\_manager role to the internal organization managers, the **sn\_bus\_loc.int\_bus\_loc.onboard\_location\_manager\_as\_contributor** system property must be set to **false**.

**Note:** Only internal users can be added as managers for internal business locations.

The manager of an internal organization can access all the cases for account, household, or consumer in the location hierarchy, including cases for child business organizations. The manager can also:

-   Add staff members to business organizations in the location hierarchy.
-   Create account team or consumer team relationships with staff members from the location hierarchy.
-   View customer information.
-   Update cases created in the location hierarchy.
-   Create cases for customers in the location hierarchy.

**Important:** Some table and field labels have been changed across recent releases. For a mapping of former labels to current labels, see [Service Model Foundation renamed Entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/renamed-entities.md).

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Business Organizations** &gt; **Internal Organizations**.

2.  Select **New** on the Internal Organizations list.

3.  Fill in the fields on the [Internal Business Organization \(formerly Business Location\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/data-model-business-location-form.md) form.

4.  Select **Submit**.

    The location is added to the Internal Organizations list.

    After creating an internal organization, add staff members to it. You can then create relationships with accounts, households, and consumers, and track customers served by that location.


## What to do next

Create related lists as required:

<table id="table_tbc_btz_djc"><thead><tr><th>

Related list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Business Organization

</td><td>

You can **Register Member**, or **Delete**, or **Copy URL** and can see all the organizations details.

</td></tr><tr><td>

Members

</td><td>

You can create, update, or delete members details

</td></tr><tr><td>

Child Internal Organizations

</td><td>

You can create, update, or delete a child internal organization details.

</td></tr><tr><td>

Child External Organizations

</td><td>

You can create, update, or delete a child external organization details.

</td></tr><tr><td>

Assignment Groups

</td><td>

Assign a assignment group to your organization

</td></tr><tr><td>

Organization Customer Criteria

</td><td>

Search and select a criteria for your organization

</td></tr><tr><td>

Cases Requested by Location

</td><td>

List and details of the cases requested by the location

</td></tr><tr><td>

Cases Assigned to Location

</td><td>

List and details of the cases assigned to your location

</td></tr><tr><td>

Sold Products

</td><td>

View details of sold products, including the Buyer organization member and Parent sold product.

**Note:**

A manager can assign a member by selecting **Assign member** and then choosing the buyer organization member.

</td></tr><tr><td>

Install Base Items

</td><td>

View details of install base items, including the Buyer organization member and Parent sold product.

**Note:** A manager can assign a member by selecting **Assign member** and then choosing the buyer organization member.

</td></tr></tbody>
</table>**Related topics**  


[Create an external organization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/create-external-business-location.md)

