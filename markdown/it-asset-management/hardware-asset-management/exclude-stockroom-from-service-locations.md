---
title: Exclude a stockroom from service locations
description: Exclude a stockroom from service locations so that the stockroom isn't shown in the Stockrooms missing service locations important actions card in the Inventory view.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/hardware-asset-management/exclude-stockroom-from-service-locations.html
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage stockrooms, Use, Hardware Asset Management, IT Asset Management]
---

# Exclude a stockroom from service locations

Exclude a stockroom from service locations so that the stockroom isn't shown in the Stockrooms missing service locations important actions card in the Inventory view.

## Before you begin

Role required: inventory\_admin

## About this task

**Note:** You can't exclude a stockroom that already has associated service locations. You must first remove the associated service locations and then exclude the stockroom from service locations. For more details, see [Remove service locations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/remove-service-locations.md).

## Procedure

1.  Navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Inventory**.

2.  Select the **All stockrooms** tab.

3.  From the list of available stockrooms, select the stockroom that you want to exclude from service locations.

4.  Select the **Exclude from service locations** check box.

5.  Select **Save**.


## Result

-   The stockroom isn't shown in the Stockrooms missing service locations important actions card even if the stockroom doesn't support service locations.
-   The **Service location** tab doesn't show the **Add** option for adding service locations to the stockroom.

**Parent Topic:**[Manage stockrooms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/manage-your-stockrooms.md)

