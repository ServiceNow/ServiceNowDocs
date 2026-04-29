---
title: Add block content in a document template block
description: Add one or more block contents in a document template block and define its condition and execution order.
locale: en-US
release: australia
product: Legal Simple Contracts
classification: legal-simple-contracts
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure legal contract of type HTML, Legal contract templates, Configure Legal Simple Contracts, Configure, Legal Simple Contracts, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Add block content in a document template block

Add one or more block contents in a document template block and define its condition and execution order.

## Before you begin

Role required: admin

## About this task

**Note:** All block content in a document template block must be created in the Legal Request Management application scope only.

## Procedure

1.  Navigate to **All** &gt; **Legal Administration** &gt; **Simple Contracts Admin** &gt; **Template Blocks**.

2.  Select a document template block.

3.  In the **Document Templates Block Contents** related list, click **New**.

4.  On the form, fill in the fields.

<table id="table_lld_cps_ypb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the block content.

</td></tr><tr><td>

Block

</td><td>

Name of the document template block associated with the document block content.

</td></tr><tr><td>

Order

</td><td>

Order in which a block content is used. If multiple block contents meet a condition, the block content with the lower-order value is chosen first.

</td></tr><tr><td>

Active

</td><td>

Option to indicate that the block content is active and available for use.

</td></tr><tr><td>

Applies when

</td><td>

Filter conditions applied on the selected table to determine which document template block to use.

</td></tr><tr><td>

Applies to

</td><td>

User criteria to which the block content is applicable.For example, a block content applicable to employees of a specific location, associate the block content with a user criteria containing only employees of that region.

</td></tr><tr><td>

Body

</td><td>

Text in the block content that appears on the document generated from the associated document template.Include fields from the selected table from the **Select Variable** pane.

</td></tr></tbody>
</table>5.  Click **Submit**.


## What to do next

[Create a legal contract template of type HTML](create-legal-contract-template-html.md).

