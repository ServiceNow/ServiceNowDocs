---
title: Customizing TSOM connector behavior with extension points
description: Learn how to use extension points to extend ServiceNow Telecommunications Service Operations Management \(TSOM\) connector behavior without modifying any default code.The resolution chain, the order field, the three dispatch patterns, and the scope restrictions determine whether a registered implementation runs and which implementation's result is applied at runtime. Review these mechanisms before implementing an extension point.Four extension points—one each for the Meraki, Fortinet, VeloCloud, and Catalyst connectors—control the lifecycle stage status assigned to discovered CIs. All four share the same contract.Assign a lifecycle stage status that varies by CI class for CIs discovered by a TSOM vendor connector. This procedure uses the Meraki connector; the steps are identical for Fortinet, VeloCloud, and Catalyst.Apply one set of lifecycle stage status rules across the Meraki, Fortinet, VeloCloud, and Catalyst connectors by centralizing the logic in a helper Script Include and delegating to it from thin per-connector wrappers.The EventFieldMapping extension point binds an incoming event to a configuration item. Use it to change how an existing vendor's events resolve to CIs, or to add CI mapping for a new vendor.Contract methods and shipped implementations for the EventFieldMapping extension point.Provide CI binding for a vendor that TSOM does not ship an event-to-CI mapper for.Replace how TSOM binds a supported vendor's events to configuration items.WebhookFieldMapping maps a vendor webhook payload to TMF688 event fields. This extension point is same-scope only, so you can't implement it from a custom scope.Two extension points control metric behavior: MetricsAggrSEP customizes aggregation, and UplinkThroughputPercentage customizes uplink throughput calculation.Replace the OOB metric aggregation logic with your own using the MetricsAggrSEP extension point.Five extension points customize narrow, vendor-specific behaviors: firmware version formatting, contract parsing, tag transformation, Nokia MPN formula handling, and recovery handling.Format the Fortinet firmware version string differently from the OOB default.Three extension points let you add API endpoints to Fortinet discovery, register new entity types, and reshape discovered data, without editing default code.Add a FortiManager API endpoint to Fortinet discovery so the connector collects data it doesn't collect by default and stores it on configuration items.Map extra fields from a FortiManager response onto Fortinet configuration items, and register transform functions to reshape the values.Properties that define a step in a Fortinet collection plan: how the endpoint is called, which entity it iterates over, and when its data is written.The five handlers a FortinetParserHooks implementation must provide, the arguments each receives, and what each returns.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/developer-guides/customize-TSOM-connector-dev-guide.html
release: australia
product: Developer Guides
classification: developer-guides
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 30
breadcrumb: [Developer guides, API implementation and reference]
---

# Customizing TSOM connector behavior with extension points

Learn how to use extension points to extend ServiceNow Telecommunications Service Operations Management \(TSOM\) connector behavior without modifying any default code.

TSOM ships 16 extension points across 5 connector scopes.

Each TSOM extension point controls one aspect of connector behavior, from life cycle status assignment, to event-to-CI mapping, to metric aggregation. Implement an extension point when the default behavior doesn't match how your organization models or processes discovered data.

For the full attribute matrix, see the TSOM extension point quick reference. The extension points are grouped by function:

-   Lifecycle management \(4\)
-   Event-to-CI mapping \(1\)
-   Webhook field mapping \(1\)
-   Metrics customization \(2\)
-   Vendor-specific customizations \(5\)
-   Fortinet discovery extensibility \(3\)—see [Fortinet discovery extensibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/developer-guides/customize-TSOM-connector-dev-guide.md).

## Requirements

This guide describes how to implement the extension points that TSOM offers. To define new extension points in your own application, see the platform documentation on [scripted extension points in server-side scripts](https://www.servicenow.com/docs/r/api-reference/web-services/scripted-extension-points.html).

Confirm the prerequisites: which plugin\(s\) / store apps deliver each connector scope \(sn\_sgc\_meraki, sn\_sgc\_fortinet, sn\_sgc\_vcloud, sn\_sgc\_catalyst, sn\_tsom\_em\_conns\), and the activation steps. The source Pocket Guide assumes the connectors are already installed.

⚠ Writer / dev verificationConfirm the role\(s\) required to create Script Includes and Extension Instance records \(admin, or a scoped-app developer role\). Not stated in the source material.

## Key terminology

The following table describes the key terms and tables that back them when you implement a TSOM extension point.

|Term|Table|Description|
|----|-----|-----------|
|Extension point|sys\_extension\_point|The contract definition. Declares the methods an implementation must provide.|
|Extension instance|sys\_extension\_instance|A registration record that links a Script Include to an extension point.|
|Script Include|sys\_script\_include|The code that implements the extension point contract.|
|Order|sys\_extension\_instance.order|Numeric priority. A lower number is a higher priority.|
|restrict\_scope|sys\_extension\_point.restrict\_scope|When `true`, only implementations from the same scope can register.|

## TSOM extension point resolution at runtime

The resolution chain, the order field, the three dispatch patterns, and the scope restrictions determine whether a registered implementation runs and which implementation's result is applied at runtime. Review these mechanisms before implementing an extension point.

When TSOM invokes an extension point, it calls `GlideScriptedExtensionPoint` to retrieve all active `sys_extension_instance` records linked to that extension point, each instantiated as a Script Include object. The calling code then selects one or more implementations from the returned array according to the extension point's dispatch pattern.

```
var ep = new GlideScriptedExtensionPoint();
var implementations = ep.getExtensions('scope.ExtensionPointName');
```

### The resolution chain

The resolution chain proceeds from contract to registration to implementation: `sys_extension_point` \(contract\) → `sys_extension_instance` \(registration, `active=true`\) → `sys_script_include` \(implementation\).

### The order field

Every `sys_extension_instance` has an integer `order` field. OOB implementations use `order = 100`. Lower numbers take priority.

|Order range|Reserved for|
|-----------|------------|
|`1–49`|ServiceNow emergency hotfixes. Do not use.|
|`50–99`|Customer overrides. Recommended: `order = 50`.|
|`100`|OOB default implementations.|
|`101+`|Fallback or lower-priority extensions.|

### Dispatch patterns

The dispatch pattern of an extension point determines how the framework selects among registered implementations and, in turn, how a custom implementation affects runtime behavior.

1.  Handler pattern \(all implementations invoked\): The framework iterates over all active implementations and invokes the handler method on each. A custom implementation's result takes precedence when it is registered at an `order` value below 100. Used by the four lifecycle status extension points and by the firmware-version and contract-parsing extension points.
2.  Vendor-dispatch pattern \(matched by vendor or rule name\): A resolver iterates over all implementations, calls `getVendor()` \(and, where applicable, `getRuleName()`\), and returns the first match. When more than one implementation matches, the implementation with the lowest `order` value is selected. Used by the event field mapping, webhook field mapping, and recovery handler extension points.
3.  Single-override pattern \(lowest order selected\): The framework uses only the implementation with the lowest `order` value; exactly one implementation runs. Used by the metrics aggregation, uplink throughput, Nokia MPN formula, and tag transformation extension points.
4.  Validated-contract pattern \(first complete implementation selected\): The framework uses the first implementation it finds that satisfies the entire contract, and exactly one implementation runs. An implementation that omits any required method is rejected in full rather than partially merged; an error names the missing method or key and the OOB implementation is used instead. Used by the three Fortinet discovery extension points: `sn_sgc_fortinet.FortinetCollectionPlan`, `sn_sgc_fortinet.FortinetParserHooks`, and `sn_sgc_fortinet.FortinetFieldMappings`. See [Fortinet discovery extensibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/developer-guides/customize-TSOM-connector-dev-guide.md).

**Note:**

Under the validated-contract pattern, `order` still governs the sequence in which implementations are examined, so register a custom implementation below 100 to have it considered before the OOB implementation. Selection then depends on whether that implementation is complete.

### Scope restrictions

The `restrict_scope` field on the extension point controls who can register an implementation.

|restrict\_scope|Meaning|Impact|
|---------------|-------|------|
|`false` \(14 of 16\)|Implementations from any scoped app are accepted.|Create a custom scoped app with your Script Include; it works cross-scope.|
|`true` \(2 of 16\)|Same scope only.|You can't override from your own scope. Contact ServiceNow support.|

**Important:**

The two extension points with `restrict_scope = true` are

`sn_tsom_em_conns.WebhookFieldMapping` and `sn_tsom_em_conns.RecoveryHandlerSEP`. An instance registered from a different scope is ignored silently; no error is raised.

## Lifecycle stage status extension points

Four extension points—one each for the Meraki, Fortinet, VeloCloud, and Catalyst connectors—control the lifecycle stage status assigned to discovered CIs. All four share the same contract.

By default, each connector assigns the status `In Use` to every discovered CI, regardless of class. Implement a lifecycle stage status extension point when the lifecycle status must vary by CI class. For example, to distinguish operational routers from interfaces undergoing maintenance.

These extension points use the handler dispatch pattern: a custom implementation runs alongside the out-of-the-box logic, and its returned value takes precedence when its extension instance is registered at a lower `order` value. All four extension points have `restrict_scope = false`, so implementations can be registered from a custom scoped application.

For the procedure to override a single connector, see Override the lifecycle stage status. To apply identical logic across all four connectors without duplication, see Share lifecycle logic across vendor connectors. For the contract and per-connector API names, see Lifecycle stage status contract.

### Lifecycle stage status contract

Reference the shared contract and per-connector API names for the four lifecycle stage status extension points.

|Attribute|Value|Description|
|---------|-----|-----------|
|Method|`handlers.getLifeCycleStageStatus(entityClass)`|Returns the lifecycle stage status for CIs of the given class.|
|Parameter|`entityClass` \(String\)|The CMDB class of the discovered CI, for example `cmdb_ci_ip_router`.|
|Returns|String|The lifecycle stage status to assign.|
|OOB default|`In Use`|Returned for all entity classes.|
|Dispatch|Handler|All active implementations are called.|

|Connector|API name|Scope|Since|
|---------|--------|-----|-----|
|Meraki|`sn_sgc_meraki.MerakiCustomizedLifeCycleStageStatus`|`sn_sgc_meraki`|v3.2|
|Fortinet|`sn_sgc_fortinet.FortinetCustomizedLifeCycleStageStatus`|`sn_sgc_fortinet`|v3.2|
|VeloCloud|`sn_sgc_vcloud.VeloCloudCustomizedLifeCycleStageStatus`|`sn_sgc_vcloud`|v3.2|
|Catalyst|`sn_sgc_catalyst.CatalystCustomizedLifeCycleStageStatus`|`sn_sgc_catalyst`|v3.4|

### Override the lifecycle stage status

Assign a lifecycle stage status that varies by CI class for CIs discovered by a TSOM vendor connector. This procedure uses the Meraki connector; the steps are identical for Fortinet, VeloCloud, and Catalyst.

#### Before you begin

Role required: XX.

Confirm the target connector \(for Meraki, `sn_sgc_meraki`\) is installed and active. Because this extension point has `restrict_scope = false`, you can register your implementation from a custom scoped application; you don't need to work inside the connector scope.

#### About this task

The extension point uses the handler pattern, so your implementation supplements rather than replaces default logic. Returning a value with an `order` below 100 makes your value win.

#### Procedure

1.  Create a Script Include in your scoped application that implements the contract method handlers.getLifeCycleStageStatus\(entityClass\).

2.  Return the status string for each CI class and fall through to `In Use` for unmatched classes.

    ```
    var MyMerakiLifeCycleOverride = Class.create();
    MyMerakiLifeCycleOverride.prototype = {
        initialize: function() {},
        handlers: {
            getLifeCycleStageStatus: function(entityClass) {
                // Routers -> Operational, interfaces -> In Maintenance
                if (entityClass == 'cmdb_ci_ip_router') return 'Operational';
                if (entityClass == 'cmdb_ci_ni_interface') return 'In Maintenance';
                return 'In Use';
            }
        },
        type: 'MyMerakiLifeCycleOverride'
    };
    ```

3.  Set the `type` value to exactly match the Script Include record name.

    **Note:** The resolver looks up `order` by `type`. A mismatch causes your order to be ignored and to default to 100.

4.  Navigate to **System Definition** &gt; **Extension Instances** and create a registration record.

    |Field|Value|
    |-----|-----|
    |Point|`sn_sgc_meraki.MerakiCustomizedLifeCycleStageStatus`|
    |Script Include|Your Script Include|
    |Order|`50` \(recommended customer-override range is 50–99\)|
    |Active|`true`|


#### Result

On the next Meraki discovery sync, discovered CIs receive the lifecycle status your implementation returns. Verify on a CI's `life_cycle_stage_status` field.

To confirm the override is loaded, see **Verify that an extension instance is active**. To reuse this logic across the other three connectors, see **Share lifecycle logic across vendor connectors**.

### Share lifecycle logic across vendor connectors

Apply one set of lifecycle stage status rules across the Meraki, Fortinet, VeloCloud, and Catalyst connectors by centralizing the logic in a helper Script Include and delegating to it from thin per-connector wrappers.

#### Before you begin

Role required: user role

#### About this task

Each connector has its own extension point, but all four share an identical contract. Rather than duplicate the mapping logic four times, put it in a shared helper and register one thin wrapper per connector extension point.

#### Procedure

1.  Create a shared helper Script Include that returns a status for a CI class.

    This is a plain helper, not an extension point implementation.

    ```
    var MyLifeCycleHelper = Class.create();
    MyLifeCycleHelper.prototype = {
        initialize: function() {},
        getStatus: function(entityClass) {
            var mapping = {
                'cmdb_ci_ip_router':    'Operational',
                'cmdb_ci_ip_switch':    'Operational',
                'cmdb_ci_ni_interface': 'In Maintenance'
            };
            return mapping[entityClass] || 'In Use';
        },
        type: 'MyLifeCycleHelper'
    };
    ```

2.  Create one thin wrapper Script Include per connector extension point that delegates to the helper.

    The example shows the Fortinet wrapper; repeat for Meraki, VeloCloud, and Catalyst.

    ```
    var MyFortinetLifeCycle = Class.create();
    MyFortinetLifeCycle.prototype = {
        initialize: function() {},
        handlers: {
            getLifeCycleStageStatus: function(entityClass) {
                return new MyLifeCycleHelper().getStatus(entityClass);
            }
        },
        type: 'MyFortinetLifeCycle'
    };
    ```

3.  Register each wrapper against its connector's extension point with `order = 50` and `active = true`.


#### Result

All four connectors apply the same lifecycle rules, and you maintain the logic in one place.

## event-to-CI mapping extension point

The EventFieldMapping extension point binds an incoming event to a configuration item. Use it to change how an existing vendor's events resolve to CIs, or to add CI mapping for a new vendor.

`sn_tsom_em_conns.EventFieldMapping` uses the **vendor-dispatch** pattern: a resolver matches on `getVendor()` and `getRuleName()`, and the lowest `order` wins among matches. The extension point has `restrict_scope = false` and is available since TSOM v3.4.

To replace mapping for a vendor that TSOM already supports, see **Override event-to-CI mapping for a vendor**. To add a vendor, see **Add event-to-CI mapping** for a new vendor. For the contract and OOB implementations, see **Event field mapping contract**.

**Note:**

In an EventFieldMapping implementation, set fields on the event and return `true` or `false` only. Calling `eventGr.update()` corrupts the event pipeline.

### Event field mapping contract

Contract methods and shipped implementations for the EventFieldMapping extension point.

|Attribute|Value|Description|
|---------|-----|-----------|
|API name|`sn_tsom_em_conns.EventFieldMapping`| |
|restrict\_scope|`false`| |
|Dispatch|Vendor-dispatch|Match vendor and rule name; lowest order wins.|
|Since|TSOM v3.4| |

|Method|Parameters|Returns|
|------|----------|-------|
|`getVendor()`|none|String, for example `Fortinet`|
|`getRuleName()`|none|String. Must match `em_mapping_rule.name` exactly.|
|`mapCi(eventGr, origEventSysId, fieldMappingRuleName)`|`eventGr` \(GlideRecord, temp\), `origEventSysId` \(String\), `fieldMappingRuleName` \(String\)|Boolean|

|Script Include|Vendor|Rule name|
|--------------|------|---------|
|`FortinetCIMapper`|Fortinet|Fortinet CI Mapper|
|`FortinetWebhookEventCIMapper`|Fortinet|Fortinet Webhook Event CI Mapper|
|`FortinetWebhookMetricCIMapper`|Fortinet|Fortinet Webhook Metric CI Mapper|
|`MerakiCIMapper`|Meraki|Meraki CI Mapper|
|`VelocloudCIMapper`|VeloCloud|VeloCloud CI Mapper|
|`VelocloudWebhookEventCIMapper`|VeloCloud|VeloCloud Webhook Event CI Mapper|

### Event field mapping contract

Contract methods and shipped implementations for the EventFieldMapping extension point.

|Attribute|Value|Description|
|---------|-----|-----------|
|API name|`sn_tsom_em_conns.EventFieldMapping`| |
|restrict\_scope|`false`| |
|Dispatch|Vendor-dispatch|Match vendor and rule name; lowest order wins.|
|Since|TSOM v3.4| |

|Method|Parameters|Returns|
|------|----------|-------|
|`getVendor()`|none|String, for example `Fortinet`|
|`getRuleName()`|none|String. Must match `em_mapping_rule.name` exactly.|
|`mapCi(eventGr, origEventSysId, fieldMappingRuleName)`|`eventGr` \(GlideRecord, temp\), `origEventSysId` \(String\), `fieldMappingRuleName` \(String\)|Boolean|

|Script Include|Vendor|Rule name|
|--------------|------|---------|
|`FortinetCIMapper`|Fortinet|Fortinet CI Mapper|
|`FortinetWebhookEventCIMapper`|Fortinet|Fortinet Webhook Event CI Mapper|
|`FortinetWebhookMetricCIMapper`|Fortinet|Fortinet Webhook Metric CI Mapper|
|`MerakiCIMapper`|Meraki|Meraki CI Mapper|
|`VelocloudCIMapper`|VeloCloud|VeloCloud CI Mapper|
|`VelocloudWebhookEventCIMapper`|VeloCloud|VeloCloud Webhook Event CI Mapper|

### Add event-to-CI mapping for a vendor

Provide CI binding for a vendor that TSOM does not ship an event-to-CI mapper for.

#### Before you begin

Role required: xxx

#### About this task

Return a new vendor and rule name that no OOB implementation matches, then implement your binding logic in `mapCi()`.

#### Procedure

1.  Create a Script Include for the new vendor.

    ```
    var PaloAltoCIMapper = Class.create();
    PaloAltoCIMapper.prototype = {
        initialize: function() {},
        getVendor:   function() { return 'PaloAlto'; },
        getRuleName: function() { return 'PaloAlto CI Mapper'; },
        mapCi: function(eventGr, origEventSysId, ruleName) {
            // Your Palo Alto CI binding logic here
            return true;
        },
        type: 'PaloAltoCIMapper'
    };
    ```

2.  Register the extension instance against `sn_tsom_em_conns.EventFieldMapping`, `active = true`.


#### Result

Events from the new vendor resolve to CIs through your mapper.

### Override event-to-CI mapping for a vendor

Replace how TSOM binds a supported vendor's events to configuration items.

#### Before you begin

Identify the OOB rule you are replacing—its name must match an `em_mapping_rule.name` value exactly.Tell the writer/developer where to find valid em\_mapping\_rule.name values \(list view or navigation path\). Not specified in the source.

Role required: xxx

#### About this task

Match the vendor and rule name of the OOB implementation, and register with a lower `order` so your implementation wins.

#### Procedure

1.  Create a Script Include that returns the target vendor and rule name and binds the CI in `mapCi()`.

    ```
    var MyFortinetCIMapper = Class.create();
    MyFortinetCIMapper.prototype = {
        initialize: function() {},
        getVendor:   function() { return 'Fortinet'; },
        getRuleName: function() { return 'Fortinet CI Mapper'; },
        mapCi: function(eventGr, origEventSysId, fieldMappingRuleName) {
            var deviceName = eventGr.getValue('node');
            if (!deviceName) return false;
            var ciGr = new GlideRecord('cmdb_ci_ip_firewall');
            ciGr.addQuery('name', deviceName);
            ciGr.query();
            if (ciGr.next()) {
                eventGr.cmdb_ci = ciGr.getUniqueValue();
                eventGr.ci_type = 'cmdb_ci_ip_firewall';
                return true;
            }
            return false;
        },
        type: 'MyFortinetCIMapper'
    };
    ```

2.  Set `type` to exactly match the Script Include record name.

    The resolver uses `impl.type` to look up the order. A mismatch means your order is ignored and defaults to 100.

3.  Register the extension instance against `sn_tsom_em_conns.EventFieldMapping` with `order = 50` and `active = true`.


#### Result

Create a test event and confirm the `em_event.cmdb_ci` and `ci_type` values resolve through your implementation.

## About the webhook field mapping extension point

WebhookFieldMapping maps a vendor webhook payload to TMF688 event fields. This extension point is same-scope only, so you can't implement it from a custom scope.

`sn_tsom_em_conns.WebhookFieldMapping` uses the vendor-dispatch pattern \(matched by `getVendor()`\) and is available since TSOM v3.2. It ships implementations for Fortinet, Meraki, VeloCloud, and Elastic.

Restriction: This extension point has `restrict_scope = true`. You cannot register an implementation from your own scoped app. To customize webhook field mapping for a new vendor, contact ServiceNow support.

For the contract, see **Webhook field mapping contract**.

OOB implementations: Fortinet, Meraki, VeloCloud, Elastic.

### Webook field mapping contract

Contract methods for the WebhookFieldMapping extension point \(same-scope only\).

|Attribute|Value|Description|
|---------|-----|-----------|
|API name|`sn_tsom_em_conns.WebhookFieldMapping`| |
|Scope|`sn_tsom_em_conns`| |
|restrict\_scope|`true`|Same scope only.|
|Dispatch|Vendor-dispatch|Match `getVendor()`.|
|Since|TSOM v3.2| |

|Method|Returns|Description|
|------|-------|-----------|
|`getVendor()`|String|Vendor identifier.|
|`getFieldMapping()`|Object \(TMF688 structure\)|Maps the vendor webhook payload to TMF688 event fields.|
|`getDetectionRules()`|Object|Rules for detecting event type from the payload.|

## Metrics customization extension points

Two extension points control metric behavior: MetricsAggrSEP customizes aggregation, and UplinkThroughputPercentage customizes uplink throughput calculation.

Both extension points have `restrict_scope = false` and use the **single-override pattern**. Only the lowest-order implementation runs.

-   `sn_tsom_em_conns.MetricsAggrSEP` \(since v3.1\) customizes how a metric is aggregated. The OOB default aggregates `meraki_uplink_status` from `cmdb_ci_ni_interface` child CIs using Decision Table rules and Clotho time-series data.
-   `sn_tsom_em_conns.UplinkThroughputPercentage` \(since v3.3\) processes and aggregates uplink throughput data.

To customize aggregation, see Override metric aggregation. For contracts, see Metrics aggregation contract and Uplink throughput contract.

### Metrics aggregation contract

Contract methods for the MetricsAggrSEP extension point.

|Attribute|Value|Description|
|---------|-----|-----------|
|API name|`sn_tsom_em_conns.MetricsAggrSEP`| |
|restrict\_scope|`false`| |
|Dispatch|Single-override|Lowest order wins.|
|Since|TSOM v3.1| |

|Method|Parameters|Returns|
|------|----------|-------|
|`aggrMetric(period)`|`period` \(String\)|void|
|`metricData()`|none|Object: `{ metricName, childClassName }`|

Default behavior: aggregates `meraki_uplink_status` from `cmdb_ci_ni_interface` child CIs using Decision Table rules and Clotho time-series data.

### Uplink throughput contract

Contract methods for the UplinkThroughputPercentage extension point.

|Attribute|Value|Description|
|---------|-----|-----------|
|API name|`sn_tsom_em_conns.UplinkThroughputPercentage`| |
|restrict\_scope|`false`| |
|Dispatch|Single-override| |
|Since|TSOM v3.3| |

|Method|Parameters|Returns|
|------|----------|-------|
|`process(data)`|`data` \(Array\)|Array \(modified data\)|
|`aggrMetric(period)`|`period` \(String\)|void|
|`metricData()`|none|Object|

### Override metric aggregation

Replace the OOB metric aggregation logic with your own using the MetricsAggrSEP extension point.

#### Before you begin

Role required: xcdfsa

#### About this task

Because this extension point uses the single-override pattern, only your lowest-order implementation runs. Implement both metricData\(\) \(to declare the metric and child class\) and aggrMetric\(period\) \(your aggregation logic\).

#### Procedure

1.  Create a Script Include implementing both contract methods.

    ```
    var MyMetricsAggr = Class.create();
    MyMetricsAggr.prototype = {
        initialize: function() {},
        aggrMetric: function(period) {
            var inputs = this.metricData();
            gs.info('Custom agg: ' + inputs.metricName);
            // Your custom aggregation logic
        },
        metricData: function() {
            return {
                metricName: 'my_custom_metric',
                childClassName: 'cmdb_ci_ni_interface'
            };
        },
        type: 'MyMetricsAggr'
    };
    ```

2.  Register the extension instance against `sn_tsom_em_conns.MetricsAggrSEP` with the lowest active `order` \(for example `50`\).


#### Result

After the scheduled aggregation job runs, confirm the results on `sa_metric_instance`.

## Vendor-specific extension points

Five extension points customize narrow, vendor-specific behaviors: firmware version formatting, contract parsing, tag transformation, Nokia MPN formula handling, and recovery handling.

-   `sn_sgc_fortinet.FortinetCustomizedFirmwareVersion` \(handler\)—format the firmware version string. See *Override firmware version formatting*.
-   `sn_sgc_fortinet.FortinetCustomizedContractParsing`—parse contract items into license attributes. See *Contract parsing contract*.
-   `sn_sgc_meraki.TagTransformationExtensionPoint` \(single-override, filtered by `handles()`\)—transform discovered tags. See *Transform discovered tags*.
-   `sn_tsom_em_conns.NokiaMpnFormulaEngineSEP` \(single-override\)—clean and validate MPN formulas. See *Clean and validate Nokia MPN formulas*.
-   `sn_tsom_em_conns.RecoveryHandlerSEP` \(vendor-dispatch, same-scope only\)—handle recovery queue records. See *About the recovery handler extension point*.

All except the recovery handler have `restrict_scope = false`.

### Override firmware version formatting

Format the Fortinet firmware version string differently from the OOB default.

#### Before you begin

Role required: xxcxcx

#### About this task

Return a formatted string from the handler. The handler's return value is used exactly as returned, including an empty or `null` result — the built-in default format \(`[device.os_ver, device.mr, device.patch].join('.')`, for example `7.4.11`\) is used only when no custom handler is active. This extension point uses the handler pattern.

#### Procedure

1.  Create a Script Include implementing `handlers.formatFirmwareVersion(device)`.

    ```
    var MyFirmwareVersion = Class.create();
    MyFirmwareVersion.prototype = {
        initialize: function() {},
        handlers: {
            formatFirmwareVersion: function(device) {
                if (device.os_ver && device.mr && device.patch) {
                    return 'FortiOS v' + device.os_ver + '.'
                        + device.mr + ' Patch ' + device.patch;
                }
                return null; // results in an empty firmware value (no fallback)
            }
        },
        type: 'MyFirmwareVersion'
    };
    ```

2.  Register the extension instance against `sn_sgc_fortinet.FortinetCustomizedFirmwareVersion` with `order = 50` and `active = true`.


#### Result

Discovered Fortinet devices display the formatted firmware version.

## Fortinet discovery extensibility

Three extension points let you add API endpoints to Fortinet discovery, register new entity types, and reshape discovered data, without editing default code.

Before these extension points, adding an endpoint to Fortinet discovery meant rebuilding the discovery configuration from the start. You can now augment discovery incrementally: declare a new endpoint, describe how its response is parsed, and map the result onto configuration item attributes.

### The three extension points

Each extension point covers one stage of the discovery pipeline. All three are in the `sn_sgc_fortinet` scope, have `restrict_scope = false`, and are available starting with TSOM v3.5. Each ships a default implementation registered at `order = 100`.

|Extension point|Controls|Required methods|
|---------------|--------|----------------|
|`sn_sgc_fortinet.FortinetCollectionPlan`|Which API calls the connector makes, in what order, and how each response is routed.|`getCollectionPlan(parser)`. `getConstants()` is optional.|
|`sn_sgc_fortinet.FortinetParserHooks`|How a raw response is unwrapped, enriched, filtered, and stored. Registers additional entity types.|All five of `unwrapResponse`, `beforeExtract`, `afterExtract`, `postProcess`, and `shouldStore`. `getEntityTypes(constants)` is optional.|
|`sn_sgc_fortinet.FortinetFieldMappings`|The declarative field mappings that shape an API response into a configuration item payload.|`getFieldMappings()`. `getTransforms()` is optional.|

### How a discovery run uses the extension points

A discovery run reads the collection plan first, then processes each response through the parser hooks and the field mappings:

1.  The active `FortinetCollectionPlan` returns the plan. The connector sorts the steps by their `dependsOn` declarations into execution levels. A circular dependency stops collection.
2.  Each step calls the shared Data Fetch action. The step's `url` function returns a request-body template key and the values substituted into that template.
3.  If the step defines `onResponse`, that function handles the response and nothing else runs for it. Otherwise the response goes to `parser.parseData()`.
4.  Responses that reach `parser.parseData()` pass through the `FortinetParserHooks` handlers, and each item is mapped by `FortinetFieldMappings`.
5.  Steps marked `write: 'deferred'` are written after every step and post-collection hook finishes.

**Note:**

In the default collection plan, only the `devices` step reaches the parser hooks. The `contracts` and `adoms` steps handle their own responses in `onResponse` and populate parser state for later steps to read.

### Contract validation and fallback

These three extension points don't resolve by `order` alone. The connector uses the first implementation it finds that satisfies the whole contract, and it uses only one implementation per extension point.

**Important:**

Validation is all or nothing. A `FortinetParserHooks` implementation missing any of the five handlers is rejected in full, and a `FortinetFieldMappings` implementation that doesn't return all five resource types is rejected in full. The connector logs an error naming the missing handlers or keys and falls back to the default implementation.

Because a partial implementation is discarded rather than merged, start from a copy of the default implementation and add to it. Omitting the `contracts`, `adoms`, or `devices` steps from a custom collection plan silently drops license, ADOM, and device collection.

For how this compares with the other TSOM dispatch patterns, see [TSOM extension point resolution at runtime](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/developer-guides/customize-TSOM-connector-dev-guide.md).

### Attributes you can't remap

Custom field mappings and custom transforms are for `additional_attributes` entries. Changing the mapping of a core configuration item attribute can break identity resolution, deduplication, and downstream processing.

**Warning:**

Don't remap `key`, `name`, `serial_number`, `ip_address`, `model_name`, `class`, `company`, `devices`, or `net_mask`.

A custom transform whose name matches a built-in transform is skipped and a warning is logged. The built-in transform is used instead.

### Retired extension point

The `sn_sgc_fortinet.FortinetCustomAttributes` extension point is retired. Its registration record and its default implementation, `FortinetDefaultCustomAttributes`, are removed during upgrade.

**Warning:**

If you implemented `FortinetCustomAttributes` to enrich Fortinet configuration items with custom attributes, move that logic to `FortinetFieldMappings`. The retired extension point isn't invoked after upgrade.

### Requirements

Role required:

Plugin:

Navigation path:

### Related tasks

-   [Add an API endpoint to Fortinet discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/developer-guides/customize-TSOM-connector-dev-guide.md)
-   [Extend Fortinet field mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/developer-guides/customize-TSOM-connector-dev-guide.md)

### Add an API endpoint to Fortinet discovery

Add a FortiManager API endpoint to Fortinet discovery so the connector collects data it doesn't collect by default and stores it on configuration items.

#### Before you begin

-   Identify the FortiManager JSON-RPC call you want to add and the parameters it takes.
-   Decide whether the endpoint is fetched once per run or once per ADOM.
-   Open the default `FortinetCollectionPlan`, `FortinetParserHooks`, and `FortinetFieldMappings` script includes so you can copy their contents.

Role required:

#### About this task

Adding an endpoint touches four things: the collection plan declares the call, a request-body template defines the payload, a parser hook shapes the response, and a field mapping turns each item into a configuration item payload. You must configure all four components. Skipping any component means the endpoint either isn't called or its data isn't stored.

**Important:**

Each of these extension points accepts one implementation only, and rejects an implementation that doesn't satisfy its whole contract. Copy the default implementation and add to the copy rather than writing a new implementation that returns only your additions.

For background on how the three extension points work together, see [Fortinet discovery extensibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/developer-guides/customize-TSOM-connector-dev-guide.md).

#### Procedure

1.  Create a script include in your own scoped application that implements `sn_sgc_fortinet.FortinetCollectionPlan`, and copy the default collection plan into its `getCollectionPlan(parser)` method.

    **Warning:**

    Return the complete plan. Omitting the `contracts`, `adoms`, or `devices` steps drops license, ADOM, and device collection with no error.

2.  Add your entity type key and request-body template key to `getConstants()`.

    Custom constants are merged into a per-run constants object rather than written to the global `FortinetConstants` object. Read them as `parser.constants.YOUR_KEY`, never as `FortinetConstants.YOUR_KEY`. Default constants win on a name collision, so you can't redefine an existing constant.

    ```
    getConstants: function() {
        return {
            FIRMWARE_UPGRADES: 'firmware_upgrades',
            GET_FIRMWARE_UPGRADES: 'sgfortinet_get_firmware_upgrades'
        };
    }
    ```

3.  Add a step for your endpoint to the plan you copied.

    Name the step after the entity type it collects. The `url` property is always a function that returns the request-body template key and the values substituted into it. For a step fetched once per ADOM, the function receives the ADOM name.

    ```
    firmware_upgrades: {
        dependsOn: ['adoms'],
        fetch: { scope: 'per_parent', parentEntity: 'adoms', strategy: 'single' },
        write: 'deferred',
        url: function(adomName) {
            return { apiName: parser.constants.GET_FIRMWARE_UPGRADES, inputs: { adom_name: adomName } };
        }
    }
    ```

    For every step property and its accepted values, see [Fortinet collection plan step properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/developer-guides/customize-TSOM-connector-dev-guide.md).

4.  Register the request-body template for your `apiName` key.

    Every Fortinet API call goes through one shared Data Fetch action. The `apiName` returned by your `url` function selects which FortiManager JSON-RPC call is made by looking up a template in the active request-body extension. The default templates are in `ActionRequestBodyFortinetDefault`.

5.  Create a script include that implements `sn_sgc_fortinet.FortinetParserHooks`, copy all five default handlers into it, and add a branch for your entity type.

    At minimum, add a branch to `unwrapResponse` that returns the array your endpoint nests its items under. Keep every existing `devices` branch, or you lose port attachment, license attribute lookup, and network site creation.

    ```
    unwrapResponse: function(responseJson, type, parser) {
        if (type === parser.constants.FIRMWARE_UPGRADES) {
            return responseJson?.result?.[0]?.data ?? [];
        }
        return responseJson;
    }
    ```

6.  Return your entity type from `getEntityTypes(constants)` so it's registered in the shared store.

    This optional handler receives the merged constants object and returns an array of entity type keys. Add it when your collection plan step introduces a type that isn't in the default plan.

    ```
    getEntityTypes: function(constants) {
        return [constants.FIRMWARE_UPGRADES];
    }
    ```

7.  Create a script include that implements `sn_sgc_fortinet.FortinetFieldMappings`, copy the default mappings into `getFieldMappings()`, and add an entry for your entity type.

    Return mappings for all five default resource types and your own: `port`, `network_site`, `network_service_instance`, `organization`, and `devices`. Add your custom fields inside an `additional_attributes` block and leave core configuration item attributes as they are.

    For field mapping syntax and transform registration, see [Extend Fortinet field mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/developer-guides/customize-TSOM-connector-dev-guide.md).

8.  Register each script include by creating an extension instance record that points to its extension point.

    Set `order` to a value between 50 and 99 so your implementation is found before the default implementation at `order = 100`, and set `active` to true.

9.  Run Fortinet discovery and confirm your endpoint's data appears on the expected configuration items.

    Because nothing is cached between runs, a change to your implementation takes effect on the next run.


#### Result

The connector calls your endpoint on every discovery run, and the data it returns is stored as additional attributes on the configuration items you mapped.

#### What to do next

If discovery runs but your data is missing, check the connector logs for a rejection message naming a missing handler or resource type. A rejected implementation is replaced by the default implementation for that extension point, and the rest of discovery continues normally.

### Extend Fortinet field mappings

Map extra fields from a FortiManager response onto Fortinet configuration items, and register transform functions to reshape the values.

#### Before you begin

-   Identify the field in the FortiManager response you want to capture, and its path within the response object.
-   Open the default `FortinetFieldMappings` script include so you can copy the default mappings.

Role required:

#### About this task

Use this procedure when the data you want is already in a response the connector collects, but isn't mapped onto a configuration item. This is also the replacement path for the retired `sn_sgc_fortinet.FortinetCustomAttributes` extension point, described in [Fortinet discovery extensibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/developer-guides/customize-TSOM-connector-dev-guide.md).

#### Procedure

1.  Create a script include in your own scoped application that implements `sn_sgc_fortinet.FortinetFieldMappings`.

2.  Copy the default mappings into `getFieldMappings()`.

    **Important:**

    Return mappings for all five resource types: `port`, `network_site`, `network_service_instance`, `organization`, and `devices`. If any key is missing, the whole implementation is rejected, an error names the missing keys, and the default mappings are used instead.

3.  Add your fields to the `additional_attributes` block of the resource type you're extending.

    Each entry names the attribute and where its value comes from. Use `source` for a path into the raw response object, `value` for a fixed value, and `transform` to name a function that post-processes the resolved value.

    ```
    additional_attributes: {
        additional_attributes: [
            { status:    { source: 'conn_status' } },
            { hostname:  { source: 'hostname' } },
            { site_code: { source: 'meta fields.SiteCode' } },
            { region:    { source: 'adomName', transform: 'prefixRegion' } }
        ]
    }
    ```

    **Warning:**

    Add fields only inside `additional_attributes`. Changing the mapping of `key`, `name`, `serial_number`, `ip_address`, `model_name`, `class`, `company`, `devices`, or `net_mask` can break configuration item identity resolution and deduplication.

4.  If a value needs reshaping, add a transform function to `getTransforms()` and reference it by name from your mapping.

    A transform receives the resolved source value as its first argument. When a mapping lists several sources, the resolved values are passed in the order they're listed. Inside a transform, `this` gives access to the active parser and to the built-in transforms.

    ```
    getTransforms: function() {
        return {
            prefixRegion: function(adomName) {
                return 'Region-' + adomName;
            },
            buildDisplayName: function(value1, value2) {
                return value1 + ' (' + value2 + ')';
            }
        };
    }
    ```

    Return `null` if you have no custom transforms.

    **Note:**

    A custom transform whose name matches a built-in transform is skipped and a warning is logged. Pick a name that isn't already in use.

5.  Read multiple source values into one transform by passing an array to `source`.

    To read from the parent context object rather than the raw item, prefix the path with `$parent.`. Use `defaultValue` for a fallback when the source resolves to null or is absent.

    **Note:**

    `defaultValue` doesn't catch an empty string. When the API can return an empty string instead of omitting the key, handle it in a transform.

6.  Create an extension instance record that points your script include at `sn_sgc_fortinet.FortinetFieldMappings`, and set `order` to a value between 50 and 99.

7.  Run Fortinet discovery and confirm your attributes appear on the configuration items.


#### Result

Your fields are written as additional attributes on the mapped configuration items on every discovery run.

#### What to do next

If an `additional_attributes` list resolves to nothing because every entry was excluded, it resolves to `null` rather than an empty array. An empty array is rejected during load, so don't replace this behavior with one that returns an empty array.

### Fortinet collection plan step properties

Properties that define a step in a Fortinet collection plan: how the endpoint is called, which entity it iterates over, and when its data is written.

A collection plan is an object keyed by step name. The step name is also the entity type passed to the parser hooks. The following properties are available on each step.

|Property|Type|Description|
|--------|----|-----------|
|`url`|Function|Required. Returns an object with `apiName` and `inputs`. `apiName` is a request-body template key that selects which FortiManager call is made. `inputs` supplies the values substituted into that template. For a step whose scope is `per_parent`, the function receives the parent ID.|
|`fetch.scope`|String|`root` fetches once per run with no iteration. `per_parent` fetches once per ID of another entity type.|
|`fetch.strategy`|String|`single` sends exactly one request per parent ID. This is the only strategy Fortinet supports.|
|`fetch.parentEntity`|String|Required when `fetch.scope` is `per_parent`. The entity type whose IDs are iterated over. For `adoms`, the IDs are the ADOM names.|
|`dependsOn`|Array of strings|Step names in the same plan that must finish first. Used to sort steps into execution levels. A circular dependency stops collection. A dependency on a name that isn't in the plan is ignored.|
|`write`|String|`deferred` writes after every step and post-collection hook finishes. `immediate` with `writeKeys` writes as soon as a response is parsed. Omit the property for a step that only populates parser state and produces no configuration items of its own.|
|`onResponse`|Function|Receives the entity ID, the result, and the active parser. When present, no other processing happens for that response unless this function triggers it. Omit it to send the response through the standard parser hooks and field mappings.|

**Note:**

The `immediate` value for `write` is supported by the underlying orchestrator but isn't used by the default plan.

#### Default steps

The default collection plan contains three steps. A custom plan must return all three and any steps you add.

|Step|Behavior|
|----|--------|
|`contracts`|Populates the license expiration map. Parses its own response in `onResponse` and produces no configuration items directly.|
|`adoms`|Builds the filtered ADOM list that later steps iterate over. Parses its own response in `onResponse` and produces no configuration items directly.|
|`devices`|Collects devices per ADOM and writes with `deferred`. Defines `onResponse` to unwrap the response, then calls the parser explicitly so the response passes through the parser hooks and field mappings.|

**Warning:**

Omitting `contracts`, `adoms`, or `devices` from a custom plan drops license, ADOM, and device collection without raising an error.

### Fortinet parser hook handlers

The five handlers a FortinetParserHooks implementation must provide, the arguments each receives, and what each returns.

An implementation of `sn_sgc_fortinet.FortinetParserHooks` must provide all five handlers. An implementation missing any handler is rejected in full and the default implementation is used instead. In every handler, `type` is the step name from the active collection plan.

|Handler|Arguments|Called and returns|
|-------|---------|------------------|
|`unwrapResponse`|`responseJson`, `type`, `parser`|Once per fetched response, before any item is mapped. Returns the value to iterate over, usually an array.|
|`beforeExtract`|`rawItem`, `type`, `store`, `parser`|Once per raw item, before field mapping. Mutates `rawItem` in place so a mapping can reference the added data as a normal source path. Returns nothing.|
|`afterExtract`|`mappedItem`, `type`, `store`, `rawItem`, `parser`|Once per item, after field mapping. Mutates `mappedItem` in place to add attributes or relationships that depend on the mapped shape. Returns nothing.|
|`postProcess`|`results`, `type`, `parser`|Once per response, with every item already mapped for that type. Returns the items to store or write, optionally filtered or transformed.|
|`shouldStore`|`mappedItem`, `type`, `parser`|Per item. Returns `false` to exclude the item from the shared store.|

#### Default handler behavior for devices

In the default collection plan, only the `devices` step reaches these handlers. Keep the following default behavior in any copy you customize.

-   `beforeExtract` fetches the device's ports and stamps them onto the raw item, and stamps the device's license attributes from the map built by the `contracts` step.
-   `afterExtract` stores the port relationships, merges the response's own metadata fields into `additional_attributes`, and creates the network site and network service instance for the device.
-   `shouldStore` excludes any mapped item without a `key`.

**Warning:**

Removing the `devices` branches from a custom implementation silently drops port attachment, port relationships, license attributes, and network site and network service instance creation.

#### Registering additional entity types

The optional `getEntityTypes(constants)` handler registers extra entity type keys in the shared store. It receives the merged constants object and returns an array of keys. Add it when a custom collection plan step introduces an entity type that isn't in the default plan.

```
getEntityTypes: function(constants) {
    return [constants.FIRMWARE_UPGRADES];
}
```

