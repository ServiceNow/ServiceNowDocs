---
title: Metric-to-CI binding
description: Metric-to-CI binding associates metrics collected by a pull connector with configuration items \(CIs\) in the Configuration Management Database \(CMDB\). Default binding logic is used for each supported connector, which you can override with a custom implementation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/metric-to-ci-binding-tsom-sgc.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-06-25"
reading_time_minutes: 2
breadcrumb: [Performance management: Metric collection, Telecom Assurance, Explore, Telecommunications Service Operations Management]
---

# Metric-to-CI binding

Metric-to-CI binding associates metrics collected by a pull connector with configuration items \(CIs\) in the Configuration Management Database \(CMDB\). Default binding logic is used for each supported connector, which you can override with a custom implementation.

## How metric-to-CI binding works

When a metric is collected, the platform runs the following sequence to associate each metric with a CMDB CI:

1.  The connector pulls metric data from the vendor and stores it in the metric base \(Clotho\).
2.  If the metric is not yet bound to a CI, the metric base framework automatically creates an event to record the request for a binding.
3.  An event field mapping rule fires on the new event. Telecommunications Service Operations Management ships pre-configured event field mapping rules for each supported connector source.
4.  The rule delegates to a scripted extension that resolves the appropriate CI for the event. The script updates the `cmdb_ci` field on the event with the resolved CI.
5.  The binding appears in the Metric to CI mappings table. From that point on, all subsequent metric data for that source-resource pair is associated with the bound CI directly, without creating another event.

If the scripted extension can't resolve a CI, the event's `cmdb_ci` field is left empty and the metric data is stored in the metric base unbound.

## Default behavior for MPN metrics

No additional configuration is required for CI binding. A scripted extension named `NokiaMPNMetricCIMapper` handles metric-to-CI binding for the MPN pull connector by firing on matching events through an event field mapping rule.

The extension tries the following event fields in order, stopping at the first match. The first lookup uses the CMDB table named in `additional_info.ciClass` on the event \(defaulting to `cmdb_ci`\); the remaining lookups always run against `cmdb_ci`:

|Order|Event field|Lookup behavior|
|-----|-----------|---------------|
|1|`additional_info.name`|Matched against `name` on the class specified by `additional_info.ciClass`|
|2|`additional_info.pmDataSource.dn`|Distinguished name traversal in `cmdb_ci`. The deepest matching component wins|
|3|`additional_info.pmDataSource.serial_no`|Matched against `serial_number` in `cmdb_ci`|
|4|`additional_info.pmDataSource.hw_id`|Matched against `name` in `cmdb_ci`|
|5|`additional_info.pmDataSource.nhg_alias`|Matched against `name` in `cmdb_ci`|

The `additional_info.name` and `additional_info.pmDataSource.dn` fields can each hold a comma-separated list of values. The extension tries the values from right to left, and the first value that resolves to a CI wins.

On a match, the extension sets the `cmdb_ci` and `ci_type` fields on the event.

## Override the default binding behavior

If the shipped lookup logic does not match how your CMDB models the source data, you can override it by providing your own implementation of the `EventFieldMapping` extension point. The platform resolves the implementation at runtime by source name and rule name, so you can substitute your own logic without modifying product code.

For the procedure, see [Override default metric-to-CI binding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/override-metric-ci-binding-tsom-sgc.md).

**Related topics**  


[View metric to CI and resource binding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/view-metric-to-CI-binding.md)

[Event field mapping configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/c_EMEventFieldMapping.md)

[Create an event rule to bind metric events to host CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-rule-bind-metrics-to-host.md)

[Configure elastic event pull connectors for MPN](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/configure-mpn-connectors-for-events-and-metrics.md)

[View metric values in the Insights Explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/view-metrics-explorer.md)

[Create an Insights Explorer view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/create-metric-explorer-view.md)

[Resource binding](https://www.servicenow.com/docs/r/it-operations-management/metric-intelligence/resource-binding.html)

