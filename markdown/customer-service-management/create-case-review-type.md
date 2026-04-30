---
title: Create a case digest configuration
description: Create case digest configurations to handle different types of case review processes.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure case digests, Configure case management, Case management, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Create a case digest configuration

Create case digest configurations to handle different types of case review processes.

## Before you begin

Role required: admin

## About this task

As part of creating a case digest configuration, you can define the specific information from a customer service case that needs to be captured as part of the review. Two configurations are included with the Case Digests plugin:

-   CAS Configuration
-   PCR Configuration

## Procedure

1.  Navigate to **All** &gt; **Case Digest** &gt; **Administration** &gt; **Configuration**.

2.  Click **New** to create a new configuration.

    You can also modify an existing configuration by clicking the configuration name and opening the configuration form.

3.  Fill in the following fields on the Case Digest Configuration form.

<table id="table_nbm_c24_bhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The configuration name.

</td></tr><tr><td>

Table name

</td><td>

The table that contains the fields to include in the configuration.-   Case Action Summary \[sn\_csm\_case\_digest\_cas\]
-   Post Case Review \[sn\_csm\_case\_digest\_pcr\]


</td></tr><tr><td>

Order

</td><td>

Determine the order for the configuration. When multiple configurations match for a case, the configuration with the lowest order number is used.

</td></tr><tr><td>

Document template

</td><td>

Select a template to use when creating a case action summary from the Case Action Summary form or a post case review document from the Post Case Review form. You can select from a list of templates that have been defined for the table selected in the **Table name** field.

</td></tr><tr><td>

Case table

</td><td>

A read-only field that displays the Case \[sn\_customerservice\_case\] table.

</td></tr><tr><td>

Approval workflow

</td><td>

If using an optional approval workflow, select the workflow from the Workflow list.

</td></tr><tr><td>

Case condition

</td><td>

Use the condition builder to select the case conditions to which this configuration applies.

</td></tr></tbody>
</table>4.  Click **Submit** or **Update**.


