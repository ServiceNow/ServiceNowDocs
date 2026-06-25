---
title: Override default metric-to-CI binding
description: Replace the shipped logic that binds collected metrics to configuration items \(CIs\) for a Telecommunications Service Operations Management metric source by creating your own implementation of the EventFieldMapping extension point and wiring it into an event field mapping rule.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/override-metric-ci-binding-tsom-sgc.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-06-25"
reading_time_minutes: 6
breadcrumb: [Configure Telecom Assurance, Configure, Telecommunications Service Operations Management]
---

# Override default metric-to-CI binding

Replace the shipped logic that binds collected metrics to configuration items \(CIs\) for a Telecommunications Service Operations Management metric source by creating your own implementation of the `EventFieldMapping` extension point and wiring it into an event field mapping rule.

## Before you begin

-   Set your application scope to **Telecommunications Service Operations Management Event Management Connectors** \(`sn_tsom_em_conns`\) using the scope switcher. If you work in the Global scope, the implementation you create in step 1 is generated in the wrong scope and the resolver can't find it at run time.
-   Identify the source name as it appears on the metric and on the corresponding event. The source name is the value used to resolve which scripted extension handles the event.
-   Decide which rule name your custom implementation will own. Each implementation is identified by a unique combination of source name and rule name. You will use this same rule name in the script include's `getRuleName()` method and in the rule's **Name** field, and the two must match exactly.
-   Determine which CMDB class and field your implementation should match against, and which event fields contain the values to match.

Role required: `tsom_assurance_admin`

For an overview of how metric-to-CI binding works in Telecommunications Service Operations Management service graph connectors, see [Metric-to-CI binding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/metric-to-ci-binding-tsom-sgc.md).

## About this task

When a connector collects metric data, the metric framework stores it and creates a metric-to-CI mapping record. Because the record does not yet have a configuration item \(CI\), the framework automatically generates an event for it. That event triggers the event field mapping rules. A rule whose source matches the event runs a script that resolves the CI and sets the `cmdb_ci` field on the event, and the resolved CI is then reflected in the CI column of the Metric To CI Mappings table:

metric-to-CI mapping record → event created → event field mapping rule → `cmdb_ci` set on the event → configuration item shown in the Metric To CI Mappings table

The shipped behavior is provided by an `EventFieldMapping` implementation that the rule's script retrieves through a resolver. The resolver, `EventFieldMappingResolver.getByRule()`, returns the implementation whose `getVendor()` matches the source name you pass and whose `getRuleName()` matches the rule name. That implementation exposes a `mapCi()` method that performs the CI lookup. To override the shipped behavior for a connector source, create your own implementation under the same source name with a new rule name, set its `getVendor()`, `getRuleName()`, and `mapCi()` methods, and wire it into an event field mapping rule whose script delegates to the resolver.

**Important:** The resolver matches on names, and a mismatch fails silently: no error is thrown, the CI is simply never set. The source name returned by `getVendor()` must match the literal you pass to `getByRule()` in the rule script, and the rule name returned by `getRuleName()` must match the rule's **Name**. A typo, a case difference, or the wrong application scope all produce the same result: the resolver returns nothing and the CI is not set. The resolver itself doesn't log the mismatch; the “No EventFieldMapping implementation found” message is written by the fallback in the rule script you create in step 3.

## Procedure

1.  Create an implementation of the `sn_tsom_em_conns.EventFieldMapping` extension point.

    1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

    2.  Search for the API name `sn_tsom_em_conns.EventFieldMapping` and open it.

    3.  In the **Related Links** section, select **Create implementation**.

        The platform generates a script include and registers it as an extension instance automatically, so the resolver can find it. Creating the implementation from this link is what registers the instance; you don't register it as a separate step.

    4.  Set the script include name \(for example, `NokiaMPNMappingRule`\) and save it.

2.  Implement the extension point methods in the generated script include.

    1.  In `getVendor()`, return your source name \(for example, `return 'Nokia MPN';`\).

        The resolver matches this value, so it must be exact.

    2.  In `getRuleName()`, return your rule name \(for example, `return 'NokiaMPNMappingRule';`\).

        This value must match the **Name** of the rule you create in step 3.

    3.  In `mapCi(eventGr, origEventSysId, fieldMappingRuleName)`, read the values you need from the event \(for example, fields under `additional_info`\), look up the matching configuration item, and set the `cmdb_ci` and `ci_type` fields on the event.

    4.  Return `true` from `mapCi()` to continue event processing, or `false` to drop the event.

    5.  Save the script include.

    **Note:** For example, the shipped Nokia MPN implementation resolves the CI on the table named by `additional_info.ciClass` \(default `cmdb_ci`\), trying these event fields in order: `additional_info.name` \(direct name match\), `additional_info.pmDataSource.dn` \(bottom-up DN traversal, deepest matching component wins\), `serial_no`, `hw_id`, and `nhg_alias`. On a match, it sets `cmdb_ci` and `ci_type` on the event.

3.  Create an event field mapping rule that delegates to your implementation.

    1.  Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **Event Field Mapping**, and then select **New**.

    2.  In **Name**, enter your rule name.

        The value must match what `getRuleName()` returns. The platform passes this name to the rule script as `fieldMappingRuleName`, and the resolver uses it to find your implementation.

    3.  Set **Source** to your source name.

        This field filters which events the rule applies to.

    4.  Set **Mapping type** to **Advanced mapping using script**.

    5.  Set **Active** to true.

    6.  Set **Order** to a value lower than any existing rule for the same source that you want this rule to take priority over.

        Lower values run first. The default rule runs at order 100. To make your rule run first, set a value below 100, for example, 50.

    7.  In **Filter**, add the condition \[Source\] \[is\] \[your source name\].

    8.  In the **Script** field, retrieve your implementation through the resolver and call `mapCi()` on it:

        ```javascript
        (function eventFieldMappingScript(eventGr, origEventSysId, fieldMappingRuleName) {
            var impl = new sn_tsom_em_conns.EventFieldMappingResolver()
                .getByRule('<your source name>', fieldMappingRuleName);
            if (impl) {
                return impl.mapCi(eventGr, origEventSysId, fieldMappingRuleName);
            }
            gs.warn('No EventFieldMapping implementation found for rule: ' + fieldMappingRuleName);
            return true;
        })(eventGr, origEventSysId, fieldMappingRuleName);
        ```

        Replace `<your source name>` with the same value that `getVendor()` returns. If you reuse this script for another source, update it in both places.

    9.  Submit the rule.

4.  Confirm the override.

    1.  Trigger the connector to collect metrics for the source.

        The metric framework creates the metric record and its event automatically.

    2.  Navigate to **All** &gt; **Event Management** &gt; **Metrics** &gt; **Metric to CI**.

        In the **Configuration item** column, verify that new metrics for your source show the CI resolved by your implementation. To trace a binding, open the linked event and verify that the `cmdb_ci` field is set.

    3.  If the CI is not set, check the system logs for the message “No EventFieldMapping implementation found”.

        That message means the resolver could not match your `getVendor()` and `getRuleName()` values, or your implementation was created in the wrong application scope. Confirm the names match across the script include and the rule, and that the script include is in the `sn_tsom_em_conns` scope.


## Result

New metrics collected from the source are bound to configuration items by your custom implementation.

**Parent Topic:**[Configure Telecom Assurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/set-up-fault-management.md)

**Related topics**  


[Event field mapping configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/c_EMEventFieldMapping.md)

[Create event field mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/t_EMCreateEventFieldMapping2.md)

[MPN Formulas table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/nokia-mpn-formulas-table.md)

