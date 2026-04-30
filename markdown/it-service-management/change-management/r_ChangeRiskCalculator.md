---
title: Risk Calculator property
description: The Best Practice - Change Risk Calculator plugin enables dynamic calculations of the risk and impact of a change. The administrator specifies how and when risk and impact rules are applied.
locale: en-US
release: zurich
product: Change Management
classification: change-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Risk conditions and calculation, Analyze change request risk and impact rating, Reference, Change Management, IT Service Management]
---

# Risk Calculator property

The Best Practice - Change Risk Calculator plugin enables dynamic calculations of the risk and impact of a change. The administrator specifies how and when risk and impact rules are applied.

The Best Practice- Change Risk Calculator plugin bundles some risk calculations using configuration item \(CI\) attributes and time measures.

A change management system property determines the risk calculation method. In **Change** &gt; **Administration** &gt; **Risk Properties**, the administrator selects one of the following methods.

<table id="table_dyk_swl_wy"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

UI Action

</td><td>

Enables users to click the **Calculate Risk** related link to check condition rules on demand.This UI action applies matching conditions according to their order. Each time a rule is applied, an alert is displayed confirming the new values for risk and impact.

 The **Calculate Risk** related link appears on the Change Request form only if the following statements are true.

-   There are risk and impact conditions that apply to the current change record.
-   The user has the admin or the itil role.

</td></tr><tr><td>

Business Rule

</td><td>

Enables conditions to be evaluated and applied dynamically through a business rule on the Change Request table.The conditions are evaluated before a change request record is inserted or updated.

 Users with the admin or the itil role or both can execute this business rule.

 **Note:** The **Run Risk Calculation** business rule replaces the **Calculate Risk** business rule when the Change Management - Risk Assessment plugin is activated.

</td></tr><tr><td>

None

</td><td>

Disables the processing of risk and impact rules.

</td></tr></tbody>
</table>**Parent Topic:**[Risk conditions and calculation](../../../product/change-management/concept/change-risk-assess-detect-conflict.md)

**Related topics**  


[Add or modify risk and impact conditions](../../../product/change-management/task/define-risk-and-impact-conditions.md)

