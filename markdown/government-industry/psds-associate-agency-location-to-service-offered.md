---
title: Associate an agency location to a Public Service definition
description: Associate your government service agency locations with a service definition using the Public Sector Digital Services \(PSDS\) application. With this association, your government service agency staff can address constituent requests for documents, records, or services that are offered at a particular agency location, and can raise a case on behalf of a constituent or business.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Case Management, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Associate an agency location to a Public Service definition

Associate your government service agency locations with a service definition using the Public Sector Digital Services \(PSDS\) application. With this association, your government service agency staff can address constituent requests for documents, records, or services that are offered at a particular agency location, and can raise a case on behalf of a constituent or business.

## Before you begin

Role required: admin

## About this task

An agency location can have multiple public services associated with it. This can include 311 service or maintenance requests, federal or state public records requests, or requests for license and permit services. For example, a specific agency location can offer an application for food stamps or medical assistance, but not an application for a CDL license or a commercial fishing license. A public service-to-agency-location criteria association can be added to each existing service definition in the Service Organizations offering Service \[service\_organizations\_offering\_service\] table.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Service Definition**.

2.  Select a service definition by selecting the number.

3.  In the Service Organizations offering Service related list, select **New**.

4.  On the form, fill in the fields.

<table id="table_qzx_5fl_byb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Organizations/Agency Location criteria

</td><td>

Reference

</td><td>

Criteria to define the agency locations that provide the service.

</td></tr><tr><td>

Service definition

</td><td>

Reference

</td><td>

Service that this specific agency location provides.

**Note:** The **Service definition** field is automatically filled in with the name of the selected service definition.

</td></tr><tr><td>

Active

</td><td>

True/False

</td><td>

Check box to activate or deactivate the agency location criteria.

 By default, the active field is set to **True**.

 **Note:** Only one active criterion is enabled per table to be associated to a service definition.

</td></tr></tbody>
</table>5.  Select **Submit**.

    The agency locations criteria are added to the Agency Locations offering Public Service related list.


