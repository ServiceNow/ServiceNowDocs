---
title: Add a healthcare organization in Healthcare and Life Sciences Service Management Core
description: Create a healthcare organization for use with Healthcare and Life Sciences Service Management Core.
locale: en-US
release: yokohama
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: task
last_updated: "2025-02-20"
reading_time_minutes: 1
breadcrumb: [Configure, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Add a healthcare organization in Healthcare and Life Sciences Service Management Core

Create a healthcare organization for use with Healthcare and Life Sciences Service Management Core.

## Before you begin

Role required: admin

## About this task

The Healthcare organization \[sn\_hcls\_organization\] table stores the details of a healthcare organization in your ServiceNow instance.

When a healthcare organization is created, an associated business location is also created with the same name that references the healthcare organization.

## Procedure

1.  Navigate to **All** &gt; **HCLS Service Management** &gt; **Organization data** &gt; **Healthcare organizations**.

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

Type of healthcare organization you represent.

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

Parent organization

</td><td>

Parent organization associated with the organization.

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

A description of this healthcare organization.

</td></tr><tr><td>

This is an internal location

</td><td>

Indicates whether this organization is considered an internal location.

</td></tr><tr><td>

Common location

</td><td>

The associated common location.

</td></tr></tbody>
</table>4.  Select **Save**.


