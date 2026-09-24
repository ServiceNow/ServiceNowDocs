---
title: Define the configuration type for customers or business locations
description: Define the configuration type to provide service to customers or business organizations within any service organization \(SO\) using the Customer Service Management \(CSM\) application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/associate-customer-criteria-to-service-organization.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Configuring business organizations, Setting up inter-organization support, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Define the configuration type for customers or business locations

Define the configuration type to provide service to customers or business organizations within any service organization \(SO\) using the Customer Service Management \(CSM\) application.

## Before you begin

Role required: admin, sn\_customerservice\_manager, sn\_customerservice.svc\_location\_manager, sn\_customerservice.svc\_location\_manager\_contributor, and sn\_bus\_loc.location\_relationship\_manager

**Important:** Some table and field labels have been changed across recent releases. For a mapping of former labels to current labels, see [Service Model Foundation renamed Entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/renamed-entities.md).

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Business Organizations** &gt; **Internal or External Business Organizations**.

2.  Select the desired internal or external Organization record and go to the **Configurations** tab.

3.  Select the configuration type based on whether you intend to provide service to customers or business organizations within any service organization.

<table id="choicetable_tgr_32q_1cc"><thead><tr><th align="left" id="d158953e111">

Configuration type

</th><th align="left" id="d158953e114">

Description

</th></tr></thead><tbody><tr><td id="d158953e120">

**Customers served**

</td><td>

Customers that are served at a business organization. The customers served can be defined with two options:-   **All customers**: Enables service organization staff to create and resolve issues for all the customers.
-   **Criteria-based**: Enables service organization staff to create and resolve issues only for customers associated with the service organization using a criteria.


</td></tr><tr><td id="d158953e141">

**Business locations served**

</td><td>

Internal or external organizations that are served by a business organization. The business organizations served can be defined with three options:-   **None**: Exclude support for any other business organization.
-   **Hierarchy-based**: Enables location support agents to create and resolve cases for service organizations through hierarchical relationships.

In other words, it’s a service organization relationship where a business location serves every business organization within its hierarchy. For example, regional support agents.

-   **Criteria-based**: Enables location support agents to create and resolve cases for service organizations that meet the defined criteria. For example, shared services.


</td></tr></tbody>
</table>4.  If **Customers served** is set to **Criteria-based**, select the [Restricted Customer Access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/associate-customers-or-bus-loc-to-so.md) check box in the Organization Customer Criteria form.

    This setting controls which customer records staff members at this business organization can view. For more information, see [Associate customers or business organizations to a service organization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/associate-customers-or-bus-loc-to-so.md).

    Restricted Customer Access is available only when the business organization has an Organization Customer Criteria assigned to it. This check box is unchecked by default. Turning it on applies that same criteria to read access as well, only the accounts, consumers, households, that match the criteria are visible to staff at this business organization. Before this field existed, the criteria controlled only which customers staff could create cases, orders, quotes, and opportunities for, business organization staff could still see every customer record in the system.

    **Note:** This field controls visibility, not edit permissions. It doesn't change who can update a record, and it doesn't change how criteria themselves are created or edited.

5.  Select **Update**.


## What to do next

Once the configuration is defined, you can associate your customers or business locations to a service organization. For more information, see [Associate customers or business organizations to a service organization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/associate-customers-or-bus-loc-to-so.md).

