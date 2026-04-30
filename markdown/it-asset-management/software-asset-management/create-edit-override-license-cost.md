---
title: Create or update an override license cost record
description: Create or update an override license cost record for your software entitlements based on your requirements.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Create or update an override license cost record

Create or update an override license cost record for your software entitlements based on your requirements.

## Before you begin

Role required: sam\_user, sam\_admin

## About this task

You can manually add or update the override license cost information for your software models and entitlements. When you create an entitlement for the Employee license metric, override license cost records are populated for Oracle Java, based on the data present in the Price tier \[samp\_price\_tier\] table. You can update the existing override license cost records according to the licensing agreement. For details on the tier-based pricing model, see [Pricing model for Oracle Java SE Universal](../reference/oracle-price-tiers.md).

## Procedure

1.  Navigate to **Software Asset Workspace** &gt; **License operations**.

2.  Select the target software model that you want to create or update the override license cost for.

3.  Select the **Override License Costs** tab.

4.  Select **New/Edit ranges**.

    -   If you select **New**, the lower limit is calculated based on the employee count range in the Price tier \[samp\_price\_tier\] table, incrementing the previous upper limit by 1. For example, if the previous employee range is 40000-49999, then the lower limit is automatically populated as 50,000 for a new record.
    -   If you select **Edit ranges**, all the existing records are set to inactive. You can select **Activate** after completing your updates to override license cost ranges.
5.  On the form, fill in the fields.

    For details on the override license cost fields and descriptions, see [Override License Costs](../reference/software-model-fields.md#section_acq_cgl_4jb).

    **Note:** You can revert your changes to the default values by selecting **Restore to default**.

6.  Select **Save**.


## Result

The override license cost record you created or modified appears in the **Override License Cost** list view. The following details are displayed for each record:

-   Metric group
-   License metric
-   License cost
-   License and maintenance cost

**Parent Topic:**[Using Software Asset Workspace](../concept/using-sam-workspace.md)

