---
title: Define the configuration type for customers or business locations
description: Define the configuration type to provide service to customers or business locations within any service organization \(SO\) using the Customer Service Management \(CSM\) application.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring business locations, Setting up inter-organization support, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Define the configuration type for customers or business locations

Define the configuration type to provide service to customers or business locations within any service organization \(SO\) using the Customer Service Management \(CSM\) application.

## Before you begin

Role required: admin, sn\_customerservice\_manager, sn\_customerservice.svc\_location\_manager, sn\_customerservice.svc\_location\_manager\_contributor, and sn\_bus\_loc.location\_relationship\_manager

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Service Organizations** &gt; **Business Locations** &gt; **Internal or External Business Locations**.

2.  Select the desired internal or external business locations record and go to the **Configurations** tab.

3.  Select the configuration type based on whether you intend to provide service to customers or business locations within any service organization.

<table id="choicetable_tgr_32q_1cc"><thead><tr><th align="left" id="d149582e96">

Configuration type

</th><th align="left" id="d149582e99">

Description

</th></tr></thead><tbody><tr><td id="d149582e105">

**Customers served**

</td><td>

Customers that are served at a business location. The customers served can be defined with two options:-   **All customers**: Enables service organization staff to create and resolve issues for all the customers.
-   **Criteria-based**: Enables service organization staff to create and resolve issues only for customers associated with the service organization using a criteria.


</td></tr><tr><td id="d149582e126">

**Business locations served**

</td><td>

Internal or external business locations that are served by a business location. The business locations served can be defined with three options:-   **None**: Exclude support for any other business location.
-   **Hierarchy-based**: Enables location support agents to create and resolve cases for service organizations through hierarchical relationships.

In other words, it’s a service organization relationship where a business location serves every business location within its hierarchy. For example, regional support agents.

-   **Criteria-based**: Enables location support agents to create and resolve cases for service organizations that meet the defined criteria. For example, shared services.


</td></tr></tbody>
</table>4.  Select **Update**.


## What to do next

Once the configuration is defined, you can associate your customers or business locations to a service organization. For more information, see [Associate customers or business locations to a service organization](associate-customers-or-bus-loc-to-so.md).

