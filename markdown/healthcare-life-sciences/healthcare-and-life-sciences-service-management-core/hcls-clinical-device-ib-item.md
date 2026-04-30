---
title: Medical device install base item table
description: The Medical device install base item \[sn\_hcls\_medical\_device\_install\_base\_item\] table stores the medical device details associated with a healthcare case or its extended case types.
locale: en-US
release: yokohama
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Data Model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Medical device install base item table

The Medical device install base item \[sn\_hcls\_medical\_device\_install\_base\_item\] table stores the medical device details associated with a healthcare case or its extended case types.

## Key features

-   Extends the Install Base Item \[sn\_install\_base\_item\] table to medical device details associated with a healthcare case or its extended case types.
-   Includes the name, configuration item, service organization, risk score, and protected health information \(PHI\) indication details.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_gsz_dbb_npb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration Item

</td><td>

Reference

</td><td>

Medical device stored as an install base item.

</td></tr><tr><td>

Name

</td><td>

String

</td><td>

Name to identify the medical device.

</td></tr><tr><td>

Number

</td><td>

String

</td><td>

Alpha-numeric profile identifier of the medical device.

 The value is auto-generated and is incremented every time you add a new medical device to your ServiceNow instance. The initial value for the **Number** field is IBITM0001001.

**Note:** To customize the number, define the auto-numbering format for the Medical device install base item \[sn\_hcls\_medical\_device\_install\_base\_item\] table. For more information, see [Add auto-numbering records in a table](https://www.servicenow.com/docs/access?context=t_AutoNumberingRecordsInATable&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Protected health information \(PHI\)

</td><td>

True/False

</td><td>

Option to indicate whether the medical device is a protected health information \(PHI\) item.

</td></tr><tr><td>

Risk score

</td><td>

String

</td><td>

Rating calculated for the medical device.

</td></tr><tr><td>

Serial number

</td><td>

String

</td><td>

Serial number of the medical device.

</td></tr><tr><td>

Service Organization

</td><td>

Reference

</td><td>

Location of the medical device.

</td></tr><tr><td>

State

</td><td>

Choice list

</td><td>

Installation status of the medical device.

 The following install statuses for a medical device are available by default:

-   Absent
-   Canceled
-   In Maintenance
-   Installed
-   Pending install
-   Retired
-   Stolen

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

