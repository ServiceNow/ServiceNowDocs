---
title: Create AWS Gov accounts mapping
description: Create an AWS GovCloud account mapping with an associated standard AWS account to enable Cloud Cost Management to consolidate usage data and provide accurate cost recommendations across your government cloud environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/cloud-cost-management/map-aws-gov-acc.html
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Cloud Cost Management for AWS, Configuring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Create AWS Gov accounts mapping

Create an AWS GovCloud account mapping with an associated standard AWS account to enable Cloud Cost Management to consolidate usage data and provide accurate cost recommendations across your government cloud environment.

## Before you begin

Make sure you meet the following requirements:

-   Verify that the AWS GovCloud account has already been created within Cloud Cost Management.
-   Verify that the standard AWS account to be linked is active and has billing permissions configured.

Role required: sn\_cmp.cloud\_admin

## About this task

AWS GovCloud accounts are separate from standard AWS accounts and can't be used directly for billing or support. Creating a mapping links a GovCloud account to its associated standard AWS account and provides access to billing data.

## Procedure

1.  Navigate to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Administration** &gt; **AWS Gov account mappings**.

2.  Select **New**.

3.  On the AWS Gov Accounts Mapping form, fill in the fields.

<table id="table_g5v_n4x_zxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Gov account

</td><td>

The AWS Gov account that you want to map to the standard AWS account.

</td></tr><tr><td>

Linked account

</td><td>

Standard AWS account that you want to link to the AWS Gov account.This account must already exist in your Cloud Cost Management configuration.

</td></tr></tbody>
</table>4.  Select **Save**.


## Result

The mapping you created gets displayed on the AWS Gov account mapping page with details such as Sys ID, tags.

