---
title: Manage transfer orders
description: Use a transfer order to move necessary parts between company stockrooms or to a location where an agent can receive them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/field-service-management/work-order-management/c\_TransferOrders.html
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage inventory in Field Service Management, Manage work order tasks, Prepare work orders, Using Field Service Management, Field Service Management]
---

# Manage transfer orders

Use a transfer order to move necessary parts between company stockrooms or to a location where an agent can receive them.

The transfer order defines delivery dates, the stockrooms involved in the transfer, and the general status of the order. A transfer order contains one or more transfer order lines which allow the transfer of multiple parts or assets on one transfer order. A transfer order line describes the part, the quantity required, and the status of the part in the transfer process.

The system creates a transfer order automatically when you create a transfer order line. You can add additional transfer order lines to a transfer order as long as the transfer order is in the **Draft** stage. When any of the transfer order lines advance to the next stage, the transfer order stage also advances, and can no longer accept additional transfer order lines.

-   **[Consumable and non-consumable models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/field-service-management/work-order-management/r_ConsumableAndNonConsumableModels.md)**  
The transfer process is slightly different for consumables than it is for non-consumables.
-   **[Create a transfer order](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/field-service-management/work-order-management/create-transfer-order.md)**  
Create a transfer order that moves the necessary parts or assets to the correct stockroom or agent location.
-   **[Merge transfer orders](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/field-service-management/work-order-management/c_MergeTransferOrders.md)**  
After you submit a new transfer order, the system examines all existing transfer orders attached to the current work order task to determine if the new transfer order can be merged with any of the existing orders.

**Parent Topic:**[Manage inventory in Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/field-service-management/work-order-management/sourcing-parts.md)

