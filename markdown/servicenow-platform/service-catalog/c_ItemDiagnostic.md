---
title: Item diagnostic report
description: For a catalog item data and configuration, you can identify possible violations from the ServiceNow recommended practices.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Debugging Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Item diagnostic report

For a catalog item data and configuration, you can identify possible violations from the ServiceNow recommended practices.

The item diagnostic report includes a score that measures the health of the item, and a list of diagnostic result entries. These entries consist of a rule, a document \(record that violates the rule\), and a count \(the number of violations in the record\).

Correct violations for best performance and to maintain expected behavior.

The lower the score, the better \(0 is ideal\). A higher score means that an item has more violations from the ServiceNow recommended practices. Each rule has a different weight and level of importance. For example, a violation of duplicate variables is more likely to result in user issues. An AJAX usage violation is less likely to cause issues since the result could simply cause a delay in the UI.

## Default diagnostic rules

These diagnostic rules are designed according to ServiceNow recommended practices.

<table id="table_zks_hbc_mv"><thead><tr><th>

Rule

</th><th>

Description

</th></tr></thead><tbody><tr><td>

checkUserCriteriaUsage

</td><td>

Identifies if the item is using entitlements instead of user criteria

</td></tr><tr><td>

checkBalancedContainers

</td><td>

Checks if the Container Start and Container End variables are balanced.

</td></tr><tr><td>

checkDuplicateVariables

</td><td>

Identifies variables with the same name associated to a catalog item \(or an associated variable set\).

</td></tr><tr><td>

checkDOMManipulation

</td><td>

Identifies any DOM violation in catalog client scripts. The DOM is not guaranteed to be the same between releases and can affect catalog client scripts during upgrades. Therefore, it is not recommended for customers to do any kind of DOM manipulation. You can view detailed information for each client script by clicking the information icon.

</td></tr><tr><td>

checkLookupVariableRowCount

</td><td>

Checks if the Lookup variable is run on tables with many records as it can lead to slower load times.

</td></tr><tr><td>

checkAJAX

</td><td>

Identifies all AJAX calls in catalog client scripts because, although AJAX calls in catalog client scripts are allowed, they must be asynchronous. All AJAX calls are listed because even asynchronous calls can cause some delay.You can view detailed information for each client script by clicking the information icon.

</td></tr><tr><td>

checkSelectBoxUnique

</td><td>

Identifies Select Box type variables that have the attribute enabled to show only unique entries in the select box.

</td></tr><tr><td>

checkOrderGuideRuleBaseCount

</td><td>

Checks for high number of active rule bases in an order guide as higher number of rule bases can lead to slower load times

</td></tr><tr><td>

checkFormatterVariablesUsage

</td><td>

Checks if the item has the following variable types:-   Macro
-   Macro with label
-   UI Page

 For information on the variable availability across various channels, see [Variable support in various channels](../reference/variables-availability.md).

</td></tr></tbody>
</table>-   **[Run the Item Diagnostic Results report](../task/run-item-diag-results.md)**  
Identify the catalog items that are not designed per ServiceNow recommended practices to run your catalog efficiently.

**Parent Topic:**[Debugging Service Catalog](debugging-service-catalog.md)

