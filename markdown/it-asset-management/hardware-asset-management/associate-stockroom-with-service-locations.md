---
title: Associate a stockroom with service locations
description: Manage sourcing requests that consume from local stockrooms effectively by associating your stockroom with multiple service locations. Optimize your loaner asset workflow and automated asset tasks by serving multiple locations using a single stockroom.
locale: en-US
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage stockrooms, Use, Hardware Asset Management, IT Asset Management]
---

# Associate a stockroom with service locations

Manage sourcing requests that consume from local stockrooms effectively by associating your stockroom with multiple service locations. Optimize your loaner asset workflow and automated asset tasks by serving multiple locations using a single stockroom.

## Before you begin

Role required: inventory\_admin

## About this task

**Note:**

You can't add service locations to a stockroom that is excluded from providing location coverage. For more details, see [Exclude a stockroom from service locations](exclude-stockroom-from-service-locations.md).

## Procedure

1.  Navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Inventory**.

2.  Select the **All stockrooms** tab.

3.  Select the stockroom that you want to associate with service locations.

4.  Select the **Service locations** tab.

5.  Select **Add**.

6.  In the Add service locations dialog box, select the active locations that you want the stockroom to support and select **Add**.

    When you add a parent location, all its child locations are also supported by the stockroom. For example, when you add the city San Francisco, the stockroom supports all the locations within San Francisco.

    **Note:** If the Active check box isn’t selected, the stockroom doesn't support that location, or its child locations so that location can’t be added to the stockroom.


## Result

The selected locations are added to the list shown in the **Service locations** tab.

**Parent Topic:**[Manage stockrooms](../concept/manage-your-stockrooms.md)

**Related topics**  


[Source requests from local stockrooms](../../procurement/task/consume-local-asset-stock.md)

[Request a loaner asset](loaner-asset-request.md)

[Create a transfer order from a request](../../procurement/task/t_CreatingTransferOrderFromReq.md)

[Asset life-cycle automation](../concept/asset-lifecycle-automation.md)

