---
title: Organization tax details outbound staging table
description: The Organization tax details outbound \[sn\_spend\_intg\_outbound\_tax\_detail\] staging table stores important data about an organization's tax information so that an ERP integrator can export this data to a third-party ERP system.
locale: en-US
release: zurich
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Outbound staging tables for Accounts Payable Operations, Outbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Organization tax details outbound staging table

The Organization tax details outbound \[sn\_spend\_intg\_outbound\_tax\_detail\] staging table stores important data about an organization's tax information so that an ERP integrator can export this data to a third-party ERP system.

## Organization tax details outbound staging table

The following table lists fields for the Organization tax details outbound \[sn\_spend\_intg\_outbound\_tax\_detail\] staging table.

<table id="table_c23_ss5_hzb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

String

</td><td>

Tax registration status of the organization or supplier.

</td></tr><tr><td>

Country

</td><td>

String

</td><td>

Name of the country.

</td></tr><tr><td>

Integration status

</td><td>

String

</td><td>

Status of the integration process.

</td></tr><tr><td>

Organization

</td><td>

String

</td><td>

Name of the organization.This is a mandatory field.

</td></tr><tr><td>

Process message

</td><td>

String

</td><td>

Describes fields that stores information related to a specific process.

</td></tr><tr><td>

State/Province

</td><td>

String

</td><td>

Name of the state or province where the supplier or organization details are registered.

</td></tr><tr><td>

Tax ID

</td><td>

String

</td><td>

Tax ID of the organization.This is a mandatory field.

</td></tr></tbody>
</table>