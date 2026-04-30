---
title: OrderUtil - Scoped
description: The OrderUtil script include enables you to view and retrieve order details.Creates an instance of the OrderUtil class.Gets the state of a specified order.Returns whether the state of a specified order is in draft state.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# OrderUtil- Scoped

The OrderUtil script include enables you to view and retrieve order details.

To access the methods in this script include, use the `sn_ind_tmt_orm` namespace identifier. The Order Management \(com.sn\_ind\_tmt\_orm\) plugin is required to access the OrderUtil script include.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## OrderUtil - OrderUtil\(\)

Creates an instance of the OrderUtil class.

|Name|Type|Description|
|----|----|-----------|
|None| | |

The following example shows how to instantiate an OrderUtil object called myOrder.

```
var myOrder = new sn_ind_tmt_orm.OrderUtil();
```

## OrderUtil - getStateFromOrder\(String orderSysId\)

Gets the state of a specified order.

|Name|Type|Description|
|----|----|-----------|
|orderSysId|String|The sys\_id of the order located in the Customer Order \[sn\_ind\_tmt\_orm\_order\] table.|

|Type|Description|
|----|-----------|
|String|Returns the state value from the order record. If there’s an issue with getting the order record or there’s no order sys\_id passed, then the method returns null.|

The following example shows how to get the state value of a specified order.

```
var orderId = "<order_sys_id>"; // order sys_id, with state draft
var state = new sn_ind_tmt_orm.OrderUtil().getStateFromOrder(orderId);
gs.info(state);
```

Output:

```
draft
```

## OrderUtil - isOrderInDraftState\(String orderSysId\)

Returns whether the state of a specified order is in draft state.

|Name|Type|Description|
|----|----|-----------|
|orderSysId|String|The sys\_id of the order located in the Customer Order \[sn\_ind\_tmt\_orm\_order\] table.|

<table id="table_tcg_csh_b2c" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the state of a specified order is in draft state.Valid values:

-   true: The specified order is in draft state.
-   false: The specified order is either not in draft state, there’s an issue retrieving the order record, or no sys\_id was passed.

</td></tr></tbody>
</table>The following example shows how to determine a specified order is in draft state.

```
var orderId = "<order_sys_id>"; // order sys_id, with state draft
var state = new sn_ind_tmt_orm.OrderUtil().isOrderInDraftState(orderId);
gs.info(state);
```

Output:

```
true
```

