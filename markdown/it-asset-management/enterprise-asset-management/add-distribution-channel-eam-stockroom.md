---
title: Add a distribution channel to a stockroom in the Enterprise Asset Workspace
description: Add a distribution channel to a stockroom so that you can link that stockroom with other geographically-related stockrooms. By linking your stockrooms, you can efficiently source and transfer assets between those stockrooms. You can also assign a rank to each linked stockroom to specify the order of stockrooms that you can source and transfer assets between.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create stockroom for enterprise assets, Create and manage enterprise asset inventory, Manage enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Add a distribution channel to a stockroom in the Enterprise Asset Workspace

Add a distribution channel to a stockroom so that you can link that stockroom with other geographically-related stockrooms. By linking your stockrooms, you can efficiently source and transfer assets between those stockrooms. You can also assign a rank to each linked stockroom to specify the order of stockrooms that you can source and transfer assets between.

## Before you begin

Role required: sn\_eam.enterprise\_admin

## Procedure

1.  From the Enterprise Asset Workspace, open the Inventory view.

2.  On the **All stockrooms** tab, select the stockroom that you want to add a distribution channel to.

    The stockroom record opens.

3.  On the **Distribution Channel** tab of the stockroom record, select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Channel Stockroom|Stockroom that you want to link as part of the distribution channel.|
    |Rank|Rank of the stockroom that you want to link. If the distribution channel contains more than one linked stockroom, this rank corresponds directly with the order of linked stockrooms that you can source and transfer assets between. Enter a numerical value, such as `1` or `5`. The lower the numerical value is, the higher the stockroom is within the order of linked stockrooms.|
    |Active|Option that indicates if the linked stockroom is active within the distribution channel.|

5.  Select **Save**.

6.  Repeat steps 3 to 5 for each stockroom that you want to link as part of the distribution channel.


**Parent Topic:**[Create stockroom for enterprise assets](create-eamstockroom.md)

