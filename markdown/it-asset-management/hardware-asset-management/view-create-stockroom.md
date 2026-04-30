---
title: Create a stockroom
description: Create stockrooms to assign places to assets.
locale: en-US
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage stockrooms, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Create a stockroom

Create stockrooms to assign places to assets.

## Before you begin

Role required: inventory\_admin

## About this task

Stockrooms are separate, standalone entities in the Asset Management application. When stock is low on a particular asset, stock rules can notify an asset manager, or automatically transfer inventory from one stockroom to another.

## Procedure

1.  Create a stockroom.

<table id="choicetable_njv_thg_kyb"><thead><tr><th align="left" id="d329994e93">

Interface

</th><th align="left" id="d329994e96">

Action

</th></tr></thead><tbody><tr><td id="d329994e102">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Inventory** &gt; **Stock** &gt; **Stockrooms**.
2.  Select **New**.


</td></tr><tr><td id="d329994e138">

**Hardware Asset Workspace**

</td><td>

1.  Navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Inventory**.
2.  Select **All stockrooms**.
3.  Select **New**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Display name of the stockroom type.|
    |Assignment group|Group that primarily uses the stockroom.|
    |Location|Physical location of the stockroom.|
    |Type|Type of stockroom, such as Field Agent or On site.|
    |Manager|Person in charge of the stockroom. Receives restocking notifications and requests for the stockroom's stock rules.|

3.  Select **Save**.


## Result

The stockroom is added to the list shown in the All stockrooms tab.

**Parent Topic:**[Manage stockrooms](../concept/manage-your-stockrooms.md)

