---
title: Associate customers or business organizations to a service organization
description: Associate your customers or business organizations \(formerly business locations\) with a service organization \(SO\) using the Customer Service Management \(CSM\) application. By linking customers or business organizations \(formerly business locations\) to the service organization, staff can create or resolve cases for customers and locations raised by other business organizations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/associate-customers-or-bus-loc-to-so.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Configuring business organizations, Setting up inter-organization support, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Associate customers or business organizations to a service organization

Associate your customers or business organizations \(formerly business locations\) with a service organization \(SO\) using the Customer Service Management \(CSM\) application. By linking customers or business organizations \(formerly business locations\) to the service organization, staff can create or resolve cases for customers and locations raised by other business organizations.

## Before you begin

Role required: admin, sn\_customerservice\_manager, sn\_customerservice.svc\_location\_manager, sn\_customerservice.svc\_location\_manager\_contributor, and sn\_bus\_loc.location\_relationship\_manager

## About this task

You can associate customers \(accounts, consumers, and households\) and business organizations \(both internal and external\) by using the organization criteria \[service\_organization\_criteria\] table. This association helps your organization to gain access to all customers and business organizations associated with an service organization.

For more information about defining organization criteria, see [Create the criteria for a service organization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/create-service-organization-criteria.md).

**Important:** Some table and field labels have been changed across recent releases. For a mapping of former labels to current labels, see [Service Model Foundation renamed Entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/renamed-entities.md).

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Business Organizations** &gt; **Internal or External Organizations**.

2.  Select the desired internal or external organizations \(formerly internal or external business locations\) record.

3.  From the Organization Customer Criteria \( formerly Service Organization Customer Criterias\) related list, select **New**.

4.  On the form, fill in the fields.

<table id="table_ykh_hfr_1cc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Organization Criteria

</td><td>

Criteria that define the customers at an organization \(formerly service organization\).

</td></tr><tr><td>

Organization

</td><td>

Organization that serves the customers that match the criteria.

</td></tr><tr><td>

Active

</td><td>

Check box to activate or deactivate the organization customer criteria.

 By default, the active field is set to **True**.

 **Note:** Only one active criterion is enabled according to table to be associated with a service organization .

</td></tr><tr><td id="restricted-access">

Restricted Customer Access

</td><td>

When selected, only the accounts, consumers, and households that match this criteria are visible to the organization staff at a business organization. The check box is unchecked by default.Before this field existed, the criteria controlled only which customers staff could create cases, orders, quotes, and opportunities for staff could still see every customer record in the system.

**Note:**

-   This check box is available only when the **Customers served** field is set to [Criteria-based](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/associate-customer-criteria-to-service-organization.md) in the Organization Customer Criteria form. In other words, Restricted Customer Access is available only when a business organization has an Organization Customer Criteria assigned to it.
-   This field controls visibility, not edit permissions. It doesn't change who can update a record, and it doesn't change how criteria themselves are created or edited.


</td></tr></tbody>
</table>5.  Select **Submit**.


## Result

An organization criterion is successfully defined for a business organization.

