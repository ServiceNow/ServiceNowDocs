---
title: Add an AWS CI class type to ensure accurate billing data
description: Specify the details of a new CI or CI type to enable the CI placement process to assign cost and usage data correctly. The process is a part of Billing Download job execution. The CI placement process associates downloaded cost and usage data with the appropriate CIs.
locale: en-US
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up access to AWS billing and usage data, Configure Cloud Cost Management for AWS, Configuring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Add an AWS CI class type to ensure accurate billing data

Specify the details of a new CI or CI type to enable the CI placement process to assign cost and usage data correctly. The process is a part of Billing Download job execution. The CI placement process associates downloaded cost and usage data with the appropriate CIs.

## Before you begin

Role required: Cloud Insights Admin \[sn\_clin\_core.insights\_admin\]

## About this task

Billing Download jobs store downloaded billing data in the billing node table. The Class Type table holds CI type definitions for the cost usage table. Cloud Cost Management executes the CI placement process to associate the billing and usage data with CIs in the CMDB. The CI placement process queries the billing node table using the CI type definitions that reside in the CI placement type table. For a new CI \(or a CI type from a new provider\), you specify the parameters that uniquely define the CI, a CI type definition, and a class type table to store the CI type definition.

**Important:** If the Cloud Cost Management Infra Stack application is installed, you can't add a new AWS CI class type. However, you can use the existing CI class types.

The CI placement type table for AWS \[sn\_cld\_intg\_aws\_ci\_placement\_type\] inherits from the Core CI placement type table \(sn\_cld\_intg\_core\_ci\_placement\_type\).

**Important:** If the Discovery patterns application is not installed, then CIs in the following class types are not placed: cmdb\_ci\_cloud\_gateway, cmdb\_ci\_dynamodb\_table, cmdb\_ci\_cloud\_object\_storage, and cmdb\_ci\_cloud\_function.

## Procedure

1.  Go to the CI placement type table and select **New**.

    ![List of AWS class types in the Core CI placement type table.](../image/aws-class-type-table.png "AWS class types in the Core CI placement type table [sn_cld_intg_core_ci_placement_type]")

2.  Fill in the form.

    ![Example class type definition.](../image/aws-class-type-defintion.png)

<table id="table_udx_w3f_hlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Class type

</td><td>

CMDB class type table that this type of CI is stored in. New CIs of this type are added to the table.

</td></tr><tr><td>

Name

</td><td>

Name of the CI type.

</td></tr><tr><td>

Query table

</td><td>

Billing node table that the CI placement process queries to find instances of the CI type.

 The Query table is sn\_cld\_aws\_cost\_usage and cannot be changed.

</td></tr><tr><td>

Query params

</td><td>

Parameter values in the billing node table that uniquely define the CI type.

</td></tr></tbody>
</table>3.  After you add a class type, you must reimport billing and usage data to ensure that CIs are correctly placed into the new type.

    See [Schedule and manage the jobs that download AWS billing data](aws-bill-dwnld-job-cloudin.md).

    **Note:** The supported CIs are placed after the Cumulus Unsupported CI Placement scheduled job runs daily. For more information, see [Supported CI class types for Amazon AWS Cloud services](../reference/aws-supported-ci-class-types.md).


