---
title: Extension point for custom naming validation
description: The TNI Naming Application validates resolved names in the Inventory Template Overview tab through a pluggable extension point. Customer administrators can register their own validation rules against the extension point to enforce organization-specific naming conventions, alongside or instead of the default check that ships with the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/extension-point-custom-naming-validation.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-06-25"
reading_time_minutes: 2
breadcrumb: [Naming patterns in inventory templates, Network inventory templates, Modeling your workflow, Explore, Telecommunications Network Inventory]
---

# Extension point for custom naming validation

The TNI Naming Application validates resolved names in the Inventory Template Overview tab through a pluggable extension point. Customer administrators can register their own validation rules against the extension point to enforce organization-specific naming conventions, alongside or instead of the default check that ships with the application.

## The extension point identity

The extension point is registered under the Network Inventory Core application:

-   Name: `TNINamingValidationBase`

-   API name: `sn_ni_core.TNINamingValidationBase`

-   Application: Network Inventory Core \(`sn_ni_core`\)


The extension point handles cross-sibling validation — it receives the set of related templates at one tree level and evaluates them as a group.

## The default validation rule

The TNI Naming Application includes a default validation rule registered against this extension point: the duplicate-name check described in [Naming pattern validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/naming-pattern-validation.md). The default rule flags two or more siblings whose patterns resolve to the same name.

The default rule appears in the Implementations table on the extension point record alongside any custom rules you register. A customer administrator can deactivate the default rule, replace it with a different rule, or leave it active and add additional rules alongside it.

## Implementations

When the Inventory Template Overview tab refreshes, every active implementation of the extension point runs against the hierarchy. Each implementation receives an array of the related templates at one tree level — the siblings under a single parent template — examines them according to its own rule, and writes validation outputs back to any related template that fails the rule.

After all implementations have run, their outputs appear in the Overview as follows:

-   Each implementation's error description contributes to the **Validation failed** banner shown on the detail pane when a failed related template is selected. Multiple implementations' descriptions are concatenated in the banner, separated by `;`.

-   The **Error** badge on the tree node is set by the last implementation that flagged the related template — only one badge displays per node.


The order in which implementations run is configurable. Because order determines which implementation's badge label appears on the tree, customer administrators that introduce custom implementations choose order deliberately when the visible badge matters to the audience reading the Overview.

**Related topics**  


[Naming pattern validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/naming-pattern-validation.md)

[The Inventory Template Overview tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/inventory-template-overview-tab.md)

