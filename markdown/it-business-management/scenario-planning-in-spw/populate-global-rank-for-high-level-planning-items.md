---
title: Populate global rank for high-level planning items
description: To enable high-level planning on a table that is not a planning item in Strategic Planning Workspace, populate global rank for existing records of this table.
locale: en-US
release: zurich
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [High-level planning configuration in Strategic Planning, Configure, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Populate global rank for high-level planning items

To enable high-level planning on a table that is not a planning item in Strategic Planning Workspace, populate global rank for existing records of this table.

## Before you begin

[Enable high-level planning for a lens entity](enable-high-level-planning-for-lens-entity.md).

Role required: admin

## About this task

Use the Strategic Planning diagnostics module to populate global rank for all existing records of the table that your planning managers chose for high-level planning. Completing this task would generate a value for the Global rank field of your table.

For this task, consider the example of generating a rank value for all existing records of the Strategic Priority \[sn\_gf\_strategy\] table.

## Procedure

1.  Navigate to **All** &gt; **Strategic Planning** &gt; **Diagnostics**.

2.  Run the Identify the high-level entities enabled for planning, without a global rank diagnostic script by selecting **Run Diagnosis**.

    The diagnosis would fail and show you the type and the total number of records that are missing a global rank.

3.  Select **Run fix script** to populate global rank value for all the flagged records.

    You can verify that the rank is populated by running the diagnostic script again. You would see that the diagnosis is a success.


## What to do next

Create a business rule to populate global rank on any future records create on your high-level planning table. See [Create a business rule for high-level planning](create-a-business-rule-for-high-level-planning.md).

