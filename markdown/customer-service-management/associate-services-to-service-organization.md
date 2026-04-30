---
title: Associate service organizations with a service
description: Associate your service organizations with a service by using the Customer Service Management \(CSM\) application. With this association, your service organization \(SO\) staff can address customer queries for products and services offered at the business location and can raise a case on the behalf of the customer.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring service definitions, Service definitions, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Associate service organizations with a service

Associate your service organizations with a service by using the Customer Service Management \(CSM\) application. With this association, your service organization \(SO\) staff can address customer queries for products and services offered at the business location and can raise a case on the behalf of the customer.

## Before you begin

Role required: sn\_csm\_case\_types.service\_definition\_manager, sn\_csm\_case\_types.service\_definition\_admin, or admin

## About this task

An SO can have multiple services associated with it. A service-to-service organization criteria association is contained in the Service Organizations offering Service \[service\_organizations\_offering\_service\] table.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Service Definitions**.

2.  Select a service definition.

3.  In the Service Organizations offering Service related list, select **New**.

4.  On the form, fill in the fields.

<table id="table_qzx_5fl_byb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service organization criteria

</td><td>

Reference

</td><td>

Criteria to define the service organizations that provide the service.

 **Note:** For more information about the criteria for the service organization, see [Create the criteria for a service organization](create-service-organization-criteria.md).

</td></tr><tr><td>

Service definition

</td><td>

Reference

</td><td>

Service that the service organizations provide.

**Note:** The **Service definition** field is automatically filled in with the name of the selected service definition.

</td></tr><tr><td>

Active

</td><td>

True/False

</td><td>

Check box to activate or deactivate the service organization criteria.

 By default, the active field is set to **True**.

 **Note:** Only one active criterion is enabled per table to be associated to a service definition.

</td></tr></tbody>
</table>5.  Select **Submit**.

    The service organization criteria are added to the Service Organizations offering Service related list.


