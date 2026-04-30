---
title: Cost rollup in project currency
description: Cost rollup calculation in projects and sub-projects with different currencies varies with the budget reference rate. The rate at which the amount is converted depends on the conversion rate.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Multicurrency in Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Cost rollup in project currency

Cost rollup calculation in projects and sub-projects with different currencies varies with the budget reference rate. The rate at which the amount is converted depends on the conversion rate.

## Convert amount entered in functional currency fields to project currency

When you create a project in functional currency of the Default view, you can manually enter or update the amount in the **Planned capital**, **Planned operating**, **Actual cost**, and **Planned benefit** fields. As you enter values in these fields, the amount is converted to project currency and stored in the corresponding project currency fields such as **Planned cost in project currency**, **Planned operating in project currency**, **Actual cost in project currency**, and **Planned benefit in project currency** fields.

**Note:** You can do so only if the project does not have a cost plan, benefit plan, or expense lines attached to it.

## Roll up project financials from sub-projects to parent projects

Use the **com.snc.project.multicurrency.rollup\_if\_different** property for financial rollups when the sub-projects and parent project have different project currencies.

<table id="table_y5y_tty_vjb"><thead><tr><th>

Property flag

</th><th>

Behavior

</th></tr></thead><tbody><tr><td>

True

</td><td>

If the property is set to True, then you can:1.  Associate a sub-project to a parent project, where both the projects have different project currencies.
2.  Roll up the sub-project amounts to the parent project amounts. However, the accuracy of the rolled up amount in the parent project varies because of the currency variation.
    -   If the project currencies of the parent project and the sub-project are the same, then the project currency amounts from the sub-projects to its parent and the top project are rolled up by adding up the amounts in the sub-project, and the rolled up amount is accurate.
    -   If the project currencies of the parent project and the sub-project are different, then all the costs of the sub-projects are converted to the project currency of the parent or the top project, referencing the Budget Reference Rate. The rate at which the amount is converted depends on the exchange rates between the project currencies, and the specified time period at which the conversion is made. Hence, the rolled up amount is only an estimate or an approximate value.

</td></tr><tr><td>

False

</td><td>

If the property is set to False, then you can:1.  Associate any number of sub-projects to a parent project, where the project currencies are same or different.
2.  Roll up only if the project currencies of the sub-project and the parent project match.

</td></tr></tbody>
</table>However, the behavior of **com.snc.project.multicurrency.rollup\_if\_different** property is different when flagged along with **com.snc.project.rollup.cost** property.

|Properties flag|Behavior|
|---------------|--------|
|**com.snc.project.rollup.cost** property is false|You can associate any sub-projects with parent project that have same or different project currency but the costs of sub-projects do not roll up to the parent project.|
|**com.snc.project.rollup.cost** property is true and **com.snc.project.multicurrency.rollup\_if\_different** property is false|You can associate sub-projects with parent project that has the same project currency.|
|**com.snc.project.rollup.cost** property is true and **com.snc.project.multicurrency.rollup\_if\_different** is true|You can associate any sub-project that has the same or different project currency with the parent project.|

## Illegal association of properties and possible errors

Following are the possible errors that may occur while making an illegal association:

<table id="table_or2_2zm_2kb"><thead><tr><th>

com.snc.project.rollup.cost

</th><th>

com.snc.project.multicurrency.rollup\_if\_different

</th><th>

Behavior

</th></tr></thead><tbody><tr><td>

False

</td><td>

Either true or false

</td><td>

Can associate sub-project to parent project even though project currency of sub-project and parent project is different but costs from sub-project to parent project cannot be rolled up.

</td></tr><tr><td>

True

</td><td>

False

</td><td>

Cannot associate sub-project to parent project if project currency of the sub-project and parent project is different.In such case of an association, an error message: `System policy does not allow parent and child projects to have different project currency` pops up.

</td></tr></tbody>
</table>