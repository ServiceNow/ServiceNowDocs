---
title: Set up Planning dependency update configuration
description: Configure the Planning dependency update configuration record to configure the plan record \(for which the dependencies are updated\), its target records, sources, and notification preferences.
locale: en-US
release: zurich
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring planning dependency updates, Dependency Configuration records, General administration setup for BCM, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Set up Planning dependency update configuration

Configure the Planning dependency update configuration record to configure the plan record \(for which the dependencies are updated\), its target records, sources, and notification preferences.

## Before you begin

Role required: sn\_bcm.admin, sn\_bcp.plan\_admin

## Procedure

1.  Navigate to **Business Continuity** &gt; **General Administration** &gt; **Planning dependency update configuration**.

2.  Select **New**.

    The example shows the Planning dependency update configuration record.

    ![Updating the BCP dependencies.](../image/plan-dep-update-config.png)

3.  On the form, fill in the fields.

    For more information on the fields in the form, see [Planning dependency update configuration form](../reference/pla-dep-update-confi-form.md).

4.  Select **Submit**.

    As per the sources and preferences set up by the BCM administrator in the BCM administrator in the Planning dependency update configuration record, the planning dependency updates are auto-updated for the plan record.

    The BCP owner and approver review the updated dependencies and complete the BCP workflow.


-   **[Planning dependency update configuration form](../reference/pla-dep-update-confi-form.md)**  
Use the Planning dependency update configuration form to configure the plan record, its sources, and preferences such as the plan record name, sources, and notification preferences and schedule an auto-update of the related assets in the plans.

**Parent Topic:**[Configuring planning dependency updates](../concept/confi-planning-dep-updates.md)

