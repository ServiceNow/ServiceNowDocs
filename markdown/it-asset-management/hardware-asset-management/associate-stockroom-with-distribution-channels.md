---
title: Link stockrooms into a distribution channel
description: Link two geographically related stockrooms to create a distribution channel and make the distribution of assets more efficient. You can assign a preference order for each channel to source assets to the stockroom.
locale: en-US
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Manage stockrooms, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Link stockrooms into a distribution channel

Link two geographically related stockrooms to create a distribution channel and make the distribution of assets more efficient. You can assign a preference order for each channel to source assets to the stockroom.

## Before you begin

Role required: inventory\_admin

## About this task

A distribution channel is a defined sourcing relationship between two geographically related stockrooms. It determines which stockroom assets are drawn from or transferred to when fulfilling requests, and in what order of preference. Setting up distribution channels helps streamline asset distribution across your organization by automating sourcing decisions rather than handling them manually.

Each distribution channel is created from the perspective of the base stockroom — the stockroom you're configuring. The Function field describes the direction of asset flow relative to the base stockroom:

-   Inbound: Assets flow into the base stockroom. The channel stockroom is the source.
-   Outbound: Assets flow out of the base stockroom. The channel stockroom is the destination.

When you create a distribution channel, the function is automatically set to Inbound for the base stockroom and Outbound for the channel stockroom.

**Note:**

You can't create distribution channels for a stockroom that doesn't support sourcing assets through distribution channels. For more details, see [Exclude a stockroom from distribution channels](exclude-stockroom-from-distribution-channel.md).

## Procedure

1.  Navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Inventory**.

2.  Select the **All stockrooms** tab.

3.  Select the stockroom for which you want to create a distribution channel.

4.  Select the **Distribution Channel** tab.

5.  Select **New**.

6.  On the form, fill in the fields.

<table id="table_x23_chb_kxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Base stockroom

</td><td>

Name of the stockroom for which you want to create a distribution channel. This field is automatically populated.

</td></tr><tr><td>

Channel stockroom

</td><td>

Name of the stockroom that you want to link to the base stockroom to create a distribution channel for sourcing assets.

</td></tr><tr><td>

Rank

</td><td>

Numeric order of preference given to the distribution channel for sourcing assets.

</td></tr><tr><td>

Function

</td><td>

Function of the distribution channel. This field is read-only and is automatically set to Inbound.

</td></tr><tr><td>

Active

</td><td>

Option that indicates whether the distribution channel is active for sourcing assets to the base stockroom.**Note:** When you clear the **Active** check box, the outbound function of the base stockroom for that channel stockroom also becomes inactive automatically.

</td></tr></tbody>
</table>7.  Select **Save**.

8.  Repeat steps 4–7 to create another distribution channel for this base stockroom.


## Result

-   The distribution channel is added to the list shown in the **Distribution Channel** tab.
-   The base stockroom is added as an outbound distribution channel for the channel stockroom. The **Function** field of the base stockroom is set to **Outbound**.

**Parent Topic:**[Manage stockrooms](../concept/manage-your-stockrooms.md)

**Related topics**  


[Create a transfer order from a request](../../procurement/task/t_CreatingTransferOrderFromReq.md)

[Source requests from local stockrooms](../../procurement/task/consume-local-asset-stock.md)

