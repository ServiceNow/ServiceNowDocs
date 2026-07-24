---
title: Extension point for custom name validation
description: The custom name validation extension point validates resolved names in the Inventory Template Overview tab. Administrators can register custom validation rules to enforce organization-specific naming conventions, replacing or extending the default check.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/extension-point-custom-naming-validation.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-07-24"
reading_time_minutes: 2
breadcrumb: [Inventory template naming patterns, Reference, Telecommunications Network Inventory]
---

# Extension point for custom name validation

The custom name validation extension point validates resolved names in the **Inventory Template Overview** tab. Administrators can register custom validation rules to enforce organization-specific naming conventions, replacing or extending the default check.

## Extension point identity

The extension point is registered under the Network Inventory Core application:

|Field|Description|
|-----|-----------|
|Name|`TNINamingValidationBase`|
|API name|`sn_ni_core.TNINamingValidationBase`|
|Application|Network Inventory Core \(`sn_ni_core`\)|

The extension point handles cross-sibling validation. It receives the set of related templates at one tree level and evaluates them as a group.

## Default validation rule

The TNI Naming Application includes a default validation rule registered against this extension point: the duplicate-name check described in [Name pattern validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/naming-pattern-validation.md). The default rule flags two or more siblings whose patterns resolve to the same name.

The default rule appears in the Implementations table on the extension point record alongside any custom rules you register. An administrator can deactivate the default rule, replace it with a different rule, or leave it active and add rules alongside it.

## Implementations

When the **Inventory Template Overview** tab refreshes, every active implementation of the extension point runs against the hierarchy. Each implementation receives an array of related templates at one tree level. It examines the siblings under a single parent template according to its own rule and writes validation results back to any related template that fails.

After all implementations have run, their outputs appear in the Overview as follows:

-   The error description of each implementation contributes to the **Validation failed** banner shown on the detail pane when a failed related template is selected. Descriptions from multiple implementations are concatenated in the banner, separated by `;`.
-   The **Error** badge on the tree node is set by the last implementation that flagged the related template. Only one badge displays per node.

**Parent Topic:**[Inventory template naming patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/naming-patterns-in-inventory-templates.md)

**Related topics**  


[Name pattern validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/naming-pattern-validation.md)

[Inventory template hierarchy view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/inventory-template-overview-tab.md)

