---
title: FinancialsWidgetUtil - Scoped
description: The FinancialsWidgetUtil script include provides methods to customize widgets in the Financials section of Project Workspace and Strategic Planning Workspace.Instantiates a FinancialsWidgetUtil object.Returns the actual cost for any planning items and work items linked to an investment.Returns the budget for any planning items and work items linked to an investment.Returns the estimate at completion \(EAC\) value for any planning items and work items linked to an investment.Returns the planned cost for any planning items and work items linked to an investment.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# FinancialsWidgetUtil- Scoped

The FinancialsWidgetUtil script include provides methods to customize widgets in the **Financials** section of Project Workspace and Strategic Planning Workspace.

The following widgets are available in Project Workspace and Strategic Planning Workspace by default.

-   Budget
-   Estimate at Completion
-   Planned Cost
-   Actual Cost to Date

You can use the FinancialsWidgetUtil script include to add child widgets that show values for a specified time period or expense type.

![This screenshot shows widgets for Budget, Estimate at Completion, Budget vs EAC Variance, Planned Cost, and Actual Cost to Date.](../image/financials-widgets.png "Financials section in Project Workspace")

In this example from Project Workspace, the Planned Cost widget has child widgets that show CapEx and OpEx values, while the Budget widget doesn't have any child widgets.

To use this script include, [create a child widget](https://www.servicenow.com/docs/access?context=configure-widget-project-financials&version=australia&pubname=australia-it-business-management&ft:locale=en-US) with one of the available financials widgets as the parent. Use the methods from this script include in the **Script** field of the child widget record.

The FinancialsWidgetUtil script include requires the Financials Core application \(sn\_invst\_pln\), as well as the Strategic Planning application \(sn\_apw\_advanced\) or Project Workspace application \(sn\_pw\). This script include is provided within the `sn_invst_pln` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## FinancialsWidgetUtil - FinancialsWidgetUtil\(GlideRecord investmentGr, Object timeScope, String expenseType\)

Instantiates a FinancialsWidgetUtil object.

This object is used to get aggregate values such as budget and planned cost for an investment.

<table id="table_f1z_33y_yzb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

investmentGr

</td><td>

[GlideRecord](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#)

</td><td>

Investment to get aggregate values for.Table: Investment \[sn\_invst\_pln\_invst\_investment\]

</td></tr><tr><td>

timeScope

</td><td>

Object

</td><td>

List of fiscal periods to use as the start and end dates for the aggregation.```
{ 
   "startFiscalPeriodSysId": "String", 
   "endFiscalPeriodSysId": "String" 
} 
```

</td></tr><tr><td>

timeScope.startFiscalPeriodSysId

</td><td>

String

</td><td>

Sys\_id of the fiscal period to use as the start date for the aggregation.Table: Fiscal Period \[fiscal\_period\]

</td></tr><tr><td>

timeScope.endFiscalPeriodSysId

</td><td>

String

</td><td>

Sys\_id of the fiscal period to use as the end date for the aggregation.Table: Fiscal Period \[fiscal\_period\]

</td></tr><tr><td>

expenseType

</td><td>

String

</td><td>

Optional. Type of expense to include in the aggregation, such as capital expenditure \(CapEx\) or operating expense \(OpEx\).Valid values:

-   capex
-   opex

</td></tr></tbody>
</table>This example instantiates a FinancialsWidgetUtil object that can be used to return aggregate values for an investment where the expense type is CapEx and the time period is `context.timeScope`.

```
var context = JSON.parse(context);
var investment = context.investment;
(function initializeFWU() {
   var invGr = new GlideRecord('sn_invst_pln_invst_investment');
   if (invGr.get(investment.sys_id)) {
      var capexCost = new sn_invst_pln.FinancialsWidgetUtil(invGr, context.timeScope, 'capex');
   }
})();
```

## FinancialsWidgetUtil - getActuals\(\)

Returns the actual cost for any planning items and work items linked to an investment.

To use this method, [create a child widget](https://www.servicenow.com/docs/access?context=configure-widget-project-financials&version=australia&pubname=australia-it-business-management&ft:locale=en-US) with the Actual Cost to Date widget as the parent. Use this method in the **Script** field of the child widget record.

The actual cost returned by this method is for the time period and expense type specified when instantiating the FinancialsWidgetUtil object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_xwh_m3y_yzb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object containing the display value and value for the actual cost.

 ```
{ 
   "displayValue": "String", 
   "value": Number
}
```

</td></tr><tr><td>

&lt;Object&gt;.displayValue

</td><td>

Display value of the actual cost, such as `$1.00 K`.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.value

</td><td>

Value of the actual cost, such as `1000`.Data type: Number

</td></tr></tbody>
</table>This example adds a child widget to the Actual Cost to Date widget that shows the actual cost for OpEx only.

```
var context = JSON.parse(context);
var investment = context.investment;
(function getCost() {
   var invGr = new GlideRecord('sn_invst_pln_invst_investment');
   if (invGr.get(investment.sys_id)) {
      var opexCost = new sn_invst_pln.FinancialsWidgetUtil(invGr, context.timeScope, 'opex').getActuals();
      return {
         displayValue: PPMCurrencyHelper.getFormattedAmountWithCurrency(opexCost.value),
         value: opexCost.value
      };
   }
})();
```

## FinancialsWidgetUtil - getBudget\(\)

Returns the budget for any planning items and work items linked to an investment.

To use this method, [create a child widget](https://www.servicenow.com/docs/access?context=configure-widget-project-financials&version=australia&pubname=australia-it-business-management&ft:locale=en-US) with the Budget widget as the parent. Use this method in the **Script** field of the child widget record.

The budget returned by this method is for the time period and expense type specified when instantiating the FinancialsWidgetUtil object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_xwh_m3y_yzb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object containing the display value and value for the budget.

 ```
{ 
   "displayValue": "String", 
   "value": Number
}
```

</td></tr><tr><td>

&lt;Object&gt;.displayValue

</td><td>

Display value of the budget, such as `$2.50 K`.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.value

</td><td>

Value of the budget, such as `2500`.Data type: Number

</td></tr></tbody>
</table>This example adds a child widget to the Budget widget that shows the budget for OpEx only.

```
var context = JSON.parse(context);
var investment = context.investment;
(function getCost() {
   var invGr = new GlideRecord('sn_invst_pln_invst_investment');
   if (invGr.get(investment.sys_id)) {
      var opexCost = new sn_invst_pln.FinancialsWidgetUtil(invGr, context.timeScope, 'opex').getBudget();
      return {
         displayValue: PPMCurrencyHelper.getFormattedAmountWithCurrency(opexCost.value),
         value: opexCost.value
      };
   }
})();
```

## FinancialsWidgetUtil - getEAC\(\)

Returns the estimate at completion \(EAC\) value for any planning items and work items linked to an investment.

To use this method, [create a child widget](https://www.servicenow.com/docs/access?context=configure-widget-project-financials&version=australia&pubname=australia-it-business-management&ft:locale=en-US) with the Estimate at Completion widget as the parent. Use this method in the **Script** field of the child widget record.

The EAC value returned by this method is for the time period and expense type specified when instantiating the FinancialsWidgetUtil object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_xwh_m3y_yzb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object containing the display value and value for the EAC.

 ```
{ 
   "displayValue": "String", 
   "value": Number
}
```

</td></tr><tr><td>

&lt;Object&gt;.displayValue

</td><td>

Display value of the EAC, such as `$2.38 K`.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.value

</td><td>

Value of the EAC, such as `2380`.Data type: Number

</td></tr></tbody>
</table>This example adds a child widget to the Estimate at Completion widget that shows the EAC for OpEx only.

```
var context = JSON.parse(context);
var investment = context.investment;
(function getCost() {
   var invGr = new GlideRecord('sn_invst_pln_invst_investment');
   if (invGr.get(investment.sys_id)) {
      var opexCost = new sn_invst_pln.FinancialsWidgetUtil(invGr, context.timeScope, 'opex').getEAC();
      return {
         displayValue: PPMCurrencyHelper.getFormattedAmountWithCurrency(opexCost.value),
         value: opexCost.value
      };
   }
})();
```

## FinancialsWidgetUtil - getPlannedCost\(\)

Returns the planned cost for any planning items and work items linked to an investment.

To use this method, [create a child widget](https://www.servicenow.com/docs/access?context=configure-widget-project-financials&version=australia&pubname=australia-it-business-management&ft:locale=en-US) with the Planned Cost widget as the parent. Use this method in the **Script** field of the child widget record.

The planned cost returned by this method is for the time period and expense type specified when instantiating the FinancialsWidgetUtil object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_xwh_m3y_yzb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object containing the display value and value for the planned cost.

 ```
{ 
   "displayValue": "String", 
   "value": Number
}
```

</td></tr><tr><td>

&lt;Object&gt;.displayValue

</td><td>

Display value of the planned cost, such as `$4.05 K`.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.value

</td><td>

Value of the planned cost, such as `4050`.Data type: Number

</td></tr></tbody>
</table>This example adds a child widget to the Planned Cost widget that shows the planned cost for OpEx only.

```
var context = JSON.parse(context);
var investment = context.investment;
(function getCost() {
   var invGr = new GlideRecord('sn_invst_pln_invst_investment');
   if (invGr.get(investment.sys_id)) {
      var opexCost = new sn_invst_pln.FinancialsWidgetUtil(invGr, context.timeScope, 'opex').getPlannedCost();
      return {
         displayValue: PPMCurrencyHelper.getFormattedAmountWithCurrency(opexCost.value),
         value: opexCost.value
      };
   }
})();
```

