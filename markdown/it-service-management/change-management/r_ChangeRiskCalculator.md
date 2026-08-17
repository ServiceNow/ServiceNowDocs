---
title: Risk Calculator property
description: The Change Management - Change Risk Calculator plugin enables dynamic calculations of the risk and impact of a change. The administrator specifies how and when risk and impact rules are applied.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/r\_ChangeRiskCalculator.html
release: australia
product: Change Management
classification: change-management
topic_type: reference
last_updated: "2026-07-17"
reading_time_minutes: 1
breadcrumb: [Risk conditions and calculation, Analyze change request risk and impact, Reference, Change Management, IT Service Management]
---

# Risk Calculator property

The Change Management - Change Risk Calculator plugin enables dynamic calculations of the risk and impact of a change. The administrator specifies how and when risk and impact rules are applied.

The Change Management- Change Risk Calculator plugin bundles some risk calculations using configuration item \(CI\) attributes and time measures.

A change management system property determines the risk calculation method. In **Change** &gt; **Administration** &gt; **Risk Properties**, the administrator selects one of the following methods.

<table id="table_dyk_swl_wy"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

UI Action

</td><td>

Enables users to select the **Calculate Risk** related link to check condition rules on demand.This UI action applies matching conditions according to their order. Each time a rule is applied, an alert is displayed confirming the new values for risk and impact.

 The **Calculate Risk** related link appears on the Change Request form only if the following statements are true.

-   There are risk and impact conditions that apply to the current change record.
-   The user has the admin or the itil role.

</td></tr><tr><td>

Business Rule

</td><td>

Enables evaluation of risk conditions automatically before a change request is saved \(insert or update\). The business rule doesn't run on every save. It is suppressed when a Risk Assessment is associated with the change request, because completing a Risk Assessment requires human interaction and the result can't be set automatically.When you select this option, most saves after the initial one — such as state transitions — don't trigger the business rule when a Risk Assessment is attached to the change.

 **Note:** The **Run Risk Calculation** business rule replaces the **Calculate Risk** business rule when the Change Management - Risk Assessment plugin is activated.

</td></tr><tr><td>

None

</td><td>

Disables the processing of risk and impact rules.

</td></tr></tbody>
</table>**Parent Topic:**[Risk conditions and calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/change-risk-assess-detect-conflict.md)

**Related topics**  


[Add or modify risk and impact conditions]()

