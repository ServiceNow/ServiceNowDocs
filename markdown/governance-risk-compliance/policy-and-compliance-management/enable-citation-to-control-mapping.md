---
title: Enable associations of citation to controls mapping
description: Enable the Citation to Control Mapping feature for more accurate compliance scoring and management.
locale: en-US
release: yokohama
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2025-11-17"
reading_time_minutes: 1
breadcrumb: [Association of citations to controls, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Enable associations of citation to controls mapping

Enable the Citation to Control Mapping feature for more accurate compliance scoring and management.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Administration** &gt; **Properties**.

2.  Set the Enable association of Citations to controls Mapping property to **Yes** and select **Save**.

    **Note:** You cannot disable this feature after enabling it, because manual associations might exist that cannot be automatically reverted.

3.  Deactivate the Compliance Score V2 scheduled job.

    Compliance Score V2 runs every 2 minutes and processes incremental changes. For example, when a control status changes. If it remains active during the bulk recalculation, it may pick up partial updates and overwrite or interfere with the new formula logic.

4.  Run the Calculate All Citations and Authority Documents Compliance Score scheduled job to recalculate all scores using the new formula.

    **Note:** Recalculating compliance scores after enabling this feature is mandatory to ensure accurate results.

5.  Reactivate the Compliance Score V2 scheduled job.


## Result

Dashboards and reports will now reflect the new citation compliance score formula.

