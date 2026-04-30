---
title: Healthcare organization table
description: The Healthcare organization \[sn\_hcls\_organization\] table stores the details of a healthcare organization in your ServiceNow instance.
locale: en-US
release: zurich
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Healthcare organization table

The Healthcare organization \[sn\_hcls\_organization\] table stores the details of a healthcare organization in your ServiceNow instance.

## Key features

-   Models healthcare organizations of different types including providers and payers.
-   Other healthcare organizations can be nested within while also being associated with multiple healthcare locations.
-   When a healthcare organization is created, an associated business location is also created with the same name that references the healthcare organization.
-   Contains the Business location field, which references the CSM business location \[sn\_csm\_business\_location\] table.
-   To associate healthcare organizations with healthcare locations, see [Associate healthcare locations with a healthcare organizations](../task/hcls-sm-associate-healthcare-locations-organization.md).

For more information on how healthcare locations and healthcare organizations function, see [Setting up healthcare locations and healthcare organizations](../concept/understanding-healthcare-locations-and-healthcare-organizations.md).

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_egs_nss_mpb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Business location

</td><td>

Reference

</td><td>

The associated business location.

 References the CSM business location \[sn\_csm\_business\_location\] table.

</td></tr><tr><td>

Identifier

</td><td>

String

</td><td>

The unique identifier of the healthcare organization.

</td></tr><tr><td>

Name

</td><td>

String

</td><td>

Name to identify the healthcare organization.

</td></tr><tr><td>

Number

</td><td>

String

</td><td>

ID number generated for this healthcare organization record.

 This field is read-only.

</td></tr><tr><td>

Organization type

</td><td>

Choice list

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

</td></tr><tr><td>

Parent

</td><td>

Reference

</td><td>

Parent organization associated with the organization.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

