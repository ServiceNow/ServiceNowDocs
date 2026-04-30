---
title: Associate customers or business locations to a service organization
description: Associate your customers or business locations with a service organization \(SO\) using the Customer Service Management \(CSM\) application. By establishing a relationship between your customers or business locations and the SO, your service organization staff can create or resolve cases for the customers and business locations raised by other business location.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring business locations serviced by a business location, Setting up inter-organization support, Configure Service Model Foundation, Data models, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Associate customers or business locations to a service organization

Associate your customers or business locations with a service organization \(SO\) using the Customer Service Management \(CSM\) application. By establishing a relationship between your customers or business locations and the SO, your service organization staff can create or resolve cases for the customers and business locations raised by other business location.

## Before you begin

Role required: admin, sn\_customerservice\_manager, sn\_customerservice.svc\_location\_manager, sn\_customerservice.svc\_location\_manager\_contributor, and sn\_bus\_loc.location\_relationship\_manager

## About this task

You can associate customers \(accounts, consumers, and households\) and business locations \(both internal and external\) by using the service organization criteria \[service\_organization\_criteria\] table. This association helps your organization to gain access to all customers and business locations associated with a service organization.

For more information about defining service organization criteria, see [Create the criteria for a service organization](create-service-organization-criteria.md).

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Service Organizations** &gt; **Business Locations** &gt; **Internal or External Business Locations**.

2.  Select the desired internal or external business locations record.

3.  From the Service Organization Customer Criteria related list, select **New**.

4.  On the form, fill in the fields.

<table id="table_ykh_hfr_1cc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Organization Criteria

</td><td>

Criteria that define the customers at a service organization.

</td></tr><tr><td>

Service Organization

</td><td>

Service organization that serves the customers that match the criteria.

</td></tr><tr><td>

Active

</td><td>

Check box to activate or deactivate the service organization customer criteria.

 By default, the active field is set to **True**.

 **Note:** Only one active criterion is enabled per table to be associated with a service organization.

</td></tr></tbody>
</table>5.  Select **Submit**.


## Result

A service organization criterion is successfully defined for a business location.

