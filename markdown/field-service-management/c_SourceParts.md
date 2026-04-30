---
title: Source parts
description: Sourcing a part is the process of reserving and obtaining an asset described in a part requirement record by transferring it from one stockroom to another.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Part requirements, Managing inventory in Field Service Management, Using Field Service Management, Field Service Management]
---

# Source parts

Sourcing a part is the process of reserving and obtaining an asset described in a part requirement record by transferring it from one stockroom to another.

Users who can create work orders can create part requirements by using [work order templates](../../it-services/concept/c_WorkOrderTemplates.md) or by manually using the procedures on this page. Agents, qualifiers, and dispatchers, including users with the combination roles, can create and source a part requirement.

-   A qualifier determines if parts are necessary to execute work order tasks.
-   A dispatcher sources the part requirements and creates transfer order lines.
-   A dispatcher or agent moves the parts through the transfer process.
-   An agent accepts delivery of the parts and records part usage.

Part requirements must be associated with a work order task. After parts are identified, a [transfer order](../task/create-transfer-order.md) is created to move the parts from the stockroom where they are located to a different stockroom or directly to an agent. Agents can be selected based on skills and the availability of parts in their personal stockrooms. One work order task can have multiple part requirements and multiple transfer orders.

-   In one work order task, multiple part requirements may require different items that can all be found in one stockroom. One transfer order can satisfy the part requirements. The transfer order will have multiple transfer order lines, each specifying a different item based on the part requirements.
-   When one stockroom has all required items, a single transfer order line can fulfill the order when moving consumable assets. One or more transfer order lines may need to be created when moving non-consumable assets. \(For more information about consumable and non-consumable assets, see [Managing Assets](https://www.servicenow.com/docs/access?context=c_ManagingAssets&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).\)
-   If a single stockroom does not contain all the items needed for the part requirement, create an additional transfer order line to a different stockroom. Because the new transfer order line specifies a different stockroom, a separate transfer order is automatically created. One part requirement is then fulfilled by two separate transfer orders to two different stockrooms.

When a technician/agent is working on a task, and requires a part, they should be able to use the part from a personal stock room, when available, without going through the sourcing process.

With simplified part sourcing, when ever a task is assigned to an agent the part requests are automatically sourced from their preferred stockroom without going through the sourcing process. If any part is not available in the preferred stockroom then agents can manually source from the assignment groups or stockrooms.

## Using assets

The technician can create a part requirement and use a part from their personal stockroom without going through the sourcing process. This is helpful for agents who are already working on tasks and have access to the necessary parts. To use this feature, click the [**Use Asset**](../task/t_RecordAssetUsageUseAsset.md) button on the Asset Usages related list on the Work Order Task form.

## Advanced part sourcing

With advanced part sourcing, the technician can source multiple assets at once from a single or multiple stockrooms. For more information, see [Request multiple parts](../../field-service-management/concept/request-inventory.md#).

**Parent Topic:**[Part requirements](c_PartRequirements.md)

**Related topics**  


[View asset usage](../task/t_RecordAssetUsage.md)

