---
title: Set up Impact analysis dependency update configuration
description: Configure the Impact analysis dependency update configuration record to configure the BIA record \(for which the dependencies are updated\), its target records, sources, and notification preferences.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring impact analysis dependency updates, Dependency Configuration records, General administration setup for BCM, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Set up Impact analysis dependency update configuration

Configure the Impact analysis dependency update configuration record to configure the BIA record \(for which the dependencies are updated\), its target records, sources, and notification preferences.

## Before you begin

Role required: sn\_bcm.admin, sn\_bcp.plan\_admin

## Procedure

1.  Navigate to **Business Continuity** &gt; **General Administration** &gt; **Impact analysis dependency update configuration**.

2.  Select **New**.

    The example shows the Impact analysis dependency update configuration record.

    ![Updating the BIA dependencies.](../image/impact-ana-dep-update-config.png)

3.  On the form, fill in the fields.

    For more information on the fields in the form, see [Impact analysis dependency update configuration form](../reference/imp-ana-dep-update-form.md).

4.  Select **Submit**.

    According to the configuration set up by the BCM administrator in the Impact analysis dependency update configuration record, the dependencies are updated in the BIA.

    The BIA owner and approver review the updated dependencies and complete the BIA workflow. For more information on scheduling an auto-update of the dependencies in the BIA, see [Scheduling auto-update of dependencies](../concept/update-impactanalysis-dep-based-on-cmdb-changes.md).


-   **[Impact analysis dependency update configuration form](../reference/imp-ana-dep-update-form.md)**  
Use the Impact analysis dependency update configuration form to configure the details of the dependency updates such as the BIA record name, target records, sources, and notification preferences.

**Parent Topic:**[Configuring impact analysis dependency updates](../concept/imp-ana-dep-update-config-module.md)

