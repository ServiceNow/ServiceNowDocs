---
title: Calculating the order priority
description: Order priority is calculated based on the rank defined in the decision table and the weightage assigned to each table.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring order priority and routing, Configure, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Calculating the order priority

Order priority is calculated based on the rank defined in the decision table and the weightage assigned to each table.

The rank and weightage can be a number between 0 to 100 and priority levels are defined as follows:

-   Critical: 80 - 100
-   High: 60 - 80
-   Medium: 40 - 60
-   Low: &lt;40

**Note:** Depending on your business requirements, you can modify the order priority by editing the rank and weightage in the `sn_ind_tmt_orm.PriorityManagement` extension script. This extension point script is used to manage priority ranks from decision tables for order line items. Any changes made in the script will override the rank and rank and weightage defined in the decision tables.

Priority is calculated as follows:

`sum of (rank * weight)/sum of weight`

For example, if the rank and weight for each decision table is defined as follows:

|Decision table|Rank|Weight|
|--------------|----|------|
|Customer|100|10|
|Specification|80|25|
|Order type|80|35|
|Urgency|60|30|

In this example, priority is calculated as:

`Priority = (100 * 10 + 80 * 25 + 80 * 35 + 60 * 30) / (10 + 25 + 35 + 30) = (7600)/100 = 76`

The order priority is set to **high** in the customer order and in the order line items.

**Note:** The highest priority specified for the order line items is used to set the priority for the customer order. The order line item priority is then propagated to the corresponding domain orders and order tasks.

## Adding a new priority rule

Apart from the rules defined in the decision tables provided with the base system \(see [Configuring order priority and routing](order-mgt-priority-management.md)\), you can create additional decision tables and a new extension point implementation to add new priority rules. To create a new priority rule, follow these steps:

1.  Navigate to**All** &gt; **Decision tables**.
2.  Click **New** and select **Decision table**.
3.  Enter a name for the decision table, select the application and application scope for the decision table and click **Build decision table**.
4.  Define the inputs and conditions for the decision table.
5.  Add the Rank in the Result column and click **Save**.
6.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.
7.  Click the `sn_ind_tmt_orm.PriorityManagement` script.
8.  Click **Create implementation** in the Related Links section.
9.  Enter a name for the new script \(implementation\) and edit the getRank\(\) and getWeightage\(\) methods in the script to return the rank and weightage values and click **Update**. A sample implementation script is shown below:

```
var PriorityManagement = Class.create();
PriorityManagement.prototype = {
    initialize: function() {},
    getRank: function(customerOrderItemGr) {
        /*
            get rank from decision policy or scripting
            return rank;
        */
        return getRankFromNewDecisionTable(customerOrderItemGr);
    },
    getWeightage: function(){
        /*
            get weightage to calculate priority
            weight should be an integer value, and range is from 0 to 100.
            return weight;
        */
        return weight_value_for_this_decision_policy;
    },
    type: 'PriorityManagement'
};
```

## Calculating the priority for external orders

Orders created by external order capture systems can also be processed by Order Management for Telecommunications. In this case, for

-   Order line items:
    -   If a valid priority value has been defined for the external order, this value is used to calculate the priority.
    -   If a priority value has not been defined or is invalid, the order priority is calculated by the Order Management for Telecommunications system.
-   Customer orders: The priority value is calculated based on the categories defined in the decision tables and this value overrides the value specified in the external order.

