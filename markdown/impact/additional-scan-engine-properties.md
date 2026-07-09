---
title: Configure definition properties
description: You can configure additional capabilities and configuration options for the definition ruleset.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/additional-scan-engine-properties.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Scan Engine properties, Activate Scan Engine and review settings, Run Impact Guided Setup, Configuring Impact, Impact]
---

# Configure definition properties

You can configure additional capabilities and configuration options for the definition ruleset.

## Deactivate a base system definition

Scan Engine admins can remove the checkbox on the active field, or, change the value of the boolean Active field to false without requiring an override.

<table id="table_deactivation_behavior"><thead><tr><th>

Scenario

</th><th>

Behavior

</th></tr></thead><tbody><tr><td>

Direct deactivation of base system definition

</td><td>

-   The definition is deactivated via UI or API without creating an override record.
-   No override is recorded in the system.

</td></tr><tr><td>

Quota impact check after deactivation

</td><td>

-   Deactivated base system definitions are excluded from active definition counts.
-   They do not count toward custom definition quotas.
-   System recalculates entitlements accurately when definitions change status.

</td></tr><tr><td>

Override-then-deactivate existing workflow

</td><td>

-   When a base system definition is overridden and then deactivated, the behavior remains unchanged.
-   The deactivated override does not count as a custom definition.

</td></tr><tr><td>

Entitlement hashing integrity

</td><td>

-   All combinations of base system and overridden definitions in active or inactive states produce consistent entitlement hash results.
-   No regressions occur for states that existed before this feature was introduced.

</td></tr></tbody>
</table>**Note:** Deactivating a definition does not remove it from the system. It only changes the active status. If you need to completely remove a definition, contact your system administrator.

**Parent Topic:**[Configure Scan Engine properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-scan-engine-properties.md)

