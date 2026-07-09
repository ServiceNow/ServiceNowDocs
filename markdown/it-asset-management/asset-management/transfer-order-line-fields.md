---
title: Transfer order line fields
description: Transfer order line form and related fields description.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-asset-management/asset-management/transfer-order-line-fields.html
release: yokohama
product: Asset Management
classification: asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [transfer order line fields, create transfer order line]
breadcrumb: [Asset Management references, Asset Management, IT Asset Management]
---

# Transfer order line fields

Transfer order line form and related fields description.

## Transfer order line form

<table id="table_q5c_pcb_fr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Internal unique number identifying the transfer order line.

</td></tr><tr><td>

Transfer Order

</td><td>

The transfer order to which the transfer order line belongs.

</td></tr><tr><td>

Model

</td><td>

Model of the items requested by the transfer order line. For example, a printer. If the Asset field is filled out first, the Model field is automatically filled in with the model corresponding to the asset.

</td></tr><tr><td>

Quantity requested

</td><td>

Number of items requested by the transfer order line. For example, 3 computers are requested to be transferred.

</td></tr><tr><td>

Quantity received

</td><td>

Number of items already received. For example, 3 keyboards are transferred, 2 are received.

</td></tr><tr><td>

Stage

</td><td>

Current stage of the transfer order. Transfer order lines can only be created when a transfer order is in **Draft** stage.

</td></tr><tr><td>

Request line

</td><td>

Requested item to associate with the transfer order line.

</td></tr><tr><td>

Asset

</td><td>

Asset requested by the transfer order line. For example, a specific printer. The asset can filter on stockrooms.**Note:** To create transfer order for an asset, the asset must have a state of **In Stock** and a substate of either **Available** or **Pre-allocated**.

</td></tr><tr><td>

Quantity remaining

</td><td>

Number of items yet to be received. For example, 3 keyboards had been requested, 2 are received, 1 is remaining.

</td></tr><tr><td>

Quantity returned

</td><td>

Number of items that already needed to be returned.

</td></tr></tbody>
</table>**Parent Topic:**[Asset Management references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/asset-management/references-asset-management.md)

**Related topics**  


[Domain separation and Asset Management]()

[Quick start test for Asset Management]()

[Installed with Asset Management]()

[Installed with Model Management]()

[Transfer assets using transfer orders](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/asset-management/t_TransferAssetsUsingTransferOrders.md)

