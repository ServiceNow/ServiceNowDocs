---
title: Create a Data Discovery policy
description: Create a Data Discovery Policy for granular control over your Data Discovery jobs.
locale: en-US
release: australia
product: Data Discovery
classification: data-discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data Discovery policies, Exploring Data Discovery \(Classic\), Data Discovery, Platform Privacy]
---

# Create a Data Discovery policy

Create a Data Discovery Policy for granular control over your Data Discovery jobs.

## Before you begin

Role required: admin, sn\_data\_discovery\_admin, data\_privacy\_admin

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Data Discovery \(Classic\)** &gt; **Data Discovery Policies**.

2.  Select the **New** button.

3.  Fill in the form.

<table id="table_rw2_21h_cgc"><thead><tr><th>

Label

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the policy

</td></tr><tr><td>

Target Column\(s\)

</td><td>

Select the target columns to use in the policy**Note:** If no columns are selected, all columns of the target table will be scanned

</td></tr><tr><td>

Target Table

</td><td>

Select the target table to use in the policy

</td></tr><tr><td>

Active

</td><td>

Determines if the policy is active or inactive**Note:** Defaults to active

</td></tr><tr><td>

Data Pattern

</td><td>

The data pattern the policy will use.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

Select the policy when creating a [Data Discovery jobs](../concept/data-discovery-jobs.md).

