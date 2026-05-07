---
title: Sync regulatory list regulations for a chemical substance
description: You can trigger a sync with the 3E Regulatory Intelligence server to retrieve all regulatory list data associated with a chemical substance based on its CAS \(Chemical Abstracts Service\) number.
locale: en-US
release: australia
product: Health and Safety
classification: health-and-safety
topic_type: task
last_updated: "2026-04-28"
reading_time_minutes: 1
breadcrumb: [3E Regulatory Intelligence, 3E, Integration with third-party services, Health and Safety, Employee Service Management]
---

# Sync regulatory list regulations for a chemical substance

You can trigger a sync with the 3E Regulatory Intelligence server to retrieve all regulatory list data associated with a chemical substance based on its CAS \(Chemical Abstracts Service\) number.

## Before you begin

Verify 3E credentials are configured correctly. A valid 3E subscription is required. For more information see, [Configure the application registry for 3E Regulatory Intelligence](hs-configure-app-register-3e-reg-intelligence.md).

Role required: sn\_hs\_chm.manager

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety Workspace**.

2.  Select **Environmental Management** \(![environmental management](../../hs-environmental-management/image/icon-hs-envt-mgmt.png)\) icon.

3.  In the **Chemical substance** list, select **All** and then open a record.

4.  Select the **Regulatory** tab.

5.  Select **Sync regulatory list**.

    A service provider request is created in the background to track the sync process.

6.  Review retrieved regulations on the **Regulatory** tab of the chemical substance, once the sync is complete.


## What to do next

-   Use the filter options to narrow regulations by regulatory list topic, country, or region. Open individual regulation records to review detailed parameters, thresholds, and conformance status. For more information, see [Monitor and manage the Regulatory list for a chemical substance](hs-monitor-manage-regulatory-tab.md).
-   In the **Regulatory** tab select **New** to create a 3E regulatory list manually when integration with 3E Regulatory Intelligence is not available. For more information on completing the 3E regulatory list regulation form, see [Regulatory list regulation form](../reference/hs-regulatory-list-regulation-form.md).

**Parent Topic:**[3E Regulatory Intelligence](../concept/hs-3e-regulatory-intelligence.md)

