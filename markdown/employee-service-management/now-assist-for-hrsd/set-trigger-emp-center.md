---
title: Set Onboarding ramp up trigger to use Employee Center portal
description: Set Onboarding ramp-up trigger to use Employee Center portal in the trigger configuration so the onboarding ramp-up plan workflow is accessible through the portal. Without setting the portal, the trigger will not be visible or usable in the Employee Center portal.
locale: en-US
release: zurich
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2025-09-08"
reading_time_minutes: 1
breadcrumb: [Generate onboarding ramp-up plan agentic workflow, Use agentic workflows, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Set Onboarding ramp up trigger to use Employee Center portal

Set Onboarding ramp-up trigger to use Employee Center portal in the trigger configuration so the onboarding ramp-up plan workflow is accessible through the portal. Without setting the portal, the trigger will not be visible or usable in the Employee Center portal.

## Before you begin

Role required: admin

## Procedure

1.  In the **Filter navigator** enter `sn_aia_trigger_configuration.list`.

2.  Select and open **Onboarding ramp-up trigger** from the **AIA Trigger Configurations** list.

3.  Select the **Active** check box.

    **Note:** The **Active** check box is not made available by default. Configure the **Form Layout** from the context menu, and move `Active` from **Available** to **Selected**.

4.  Add `Employee Center` to the **Portal** field.

    **Note:** The **Portal** field is not made available by default. Configure the **Form Layout** from the context menu, and move `Portal` from **Available** to **Selected**.

5.  Click **Save**.


