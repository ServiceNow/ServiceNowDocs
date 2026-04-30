---
title: Create a healthcare organization in Healthcare Operations Core
description: Create a healthcare organization for use with Healthcare Operations Core.
locale: en-US
release: yokohama
product: Care Team Operations
classification: care-team-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Healthcare Operations Core, Healthcare Operations Core, Healthcare Operations, Healthcare and Life Sciences]
---

# Create a healthcare organization in Healthcare Operations Core

Create a healthcare organization for use with Healthcare Operations Core.

## About this task

The Healthcare organization \[sn\_hcls\_organization\] table stores the details of a healthcare organization in your ServiceNow instance.

When a healthcare organization is created, an associated business location is also created with the same name that references the healthcare organization.

For more information, see [Example - Organizing your healthcare organizations](example-organizing-hcls-organizations.md)

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Healthcare Operations** &gt; **Healthcare organizations** &gt; **All**.

2.  Select **New**.

3.  Fill in the following fields.

<table id="table_zkv_ppj_vcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of your healthcare organization.

</td></tr><tr><td>

Organization type

</td><td>

Type of healthcare organization represented.

 The following types are available by default:

 -   Clinical research sponsor

-   Community group

-   Educational institute

-   Government

-   Healthcare provider

-   Hospital department

-   Non-healthcare business

-   Organizational team

-   Other

-   Payer

-   Pharmaceutical company

-   Religious institution

 For more information about the available organization types, see [organization types](https://www.hl7.org/fhir/valueset-organization-type.html) defined in the FHIR specifications.

</td></tr><tr><td>

Parent Organization

</td><td>

Parent organization associated with the organization.Setting a parent organization will create a hierarchy in which the current organization being created is a child organization of the value selected here.

</td></tr><tr><td>

Phone

</td><td>

Phone number of the organization.

</td></tr><tr><td>

Email

</td><td>

Email address associated with the organization.

</td></tr><tr><td>

Description

</td><td>

A description of the organization being created.

</td></tr><tr><td>

This is an internal location

</td><td>

Indicated whether the organization being created is associated with an internal location.

</td></tr><tr><td>

Common location

</td><td>

The common location address associated with the healthcare organization being created.

</td></tr></tbody>
</table>4.  Select **Submit**.


