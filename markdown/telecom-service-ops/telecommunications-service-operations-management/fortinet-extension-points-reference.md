---
title: Fortinet extension points reference
description: The Service Graph Connector for Fortinet exposes nine scripted extension points that let you customize specific parts of the connector's behavior without modifying the shipped application. Use this reference to find which extension point controls the behavior you want to change.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/fortinet-extension-points-reference.html
release: brazil
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 7
keywords: [extension points fortinet scripted]
breadcrumb: [Reference, Telecommunications Service Operations Management]
---

# Fortinet extension points reference

The Service Graph Connector for Fortinet exposes nine scripted extension points that let you customize specific parts of the connector's behavior without modifying the shipped application. Use this reference to find which extension point controls the behavior you want to change.

Each extension point defines a contract — a set of functions — at a specific point in the connector's data-collection pipeline. The connector ships a default implementation for every extension point and picks up any active custom implementation automatically on its next scheduled run. For the steps to create a custom implementation, see [Customize scripted extension points](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/configure-extension-points.md).

|Extension point|Lets you customize|Enabled by default|
|---------------|------------------|------------------|
|`ActionRequestBody`|FortiManager request payloads|Yes|
|`FortinetCollectionPlan`|Which APIs are called, and how responses are processed|Yes|
|`FortinetFieldMappings`|Extra CI attributes populated from raw API fields|Yes|
|`FortinetCustomAttributes`|Extra `additional_attributes` computed in script, on devices, organizations, network sites, network service instances, and ports|Yes|
|`FortinetParserHooks`|Custom enrichment logic during data extraction|Yes|
|`FortinetCustomizedFirmwareVersion`|How a device's firmware version string is built|Yes|
|`FortinetCustomizedContractParsing`|How license contract data is parsed|Yes|
|`FortinetCustomizedAdomFilter`|Which ADOMs are collected at all|No|
|`FortinetCustomizedLifeCycleStageStatus`|The Life Cycle Stage Status value set on new CIs, per CI class|Yes|

## How the platform selects an implementation

At each extension seam, the connector retrieves every *active* implementation registered for that extension point, sorted by the extension instance's **Order** field in ascending order. The first implementation, in that order, that provides the required function is used.

Every default implementation shipped with the connector registers its extension instance with an **Order** of 100. Give your custom implementation a lower **Order** value \(for example, 20\) so it's evaluated first. If no active implementation is found, or a custom implementation throws an error, the connector's default behavior applies instead.

## Request payloads \(ActionRequestBody\)

The connector talks to FortiManager over a single shared JSON-RPC endpoint. This extension point lets you customize the request body sent for any of the connector's four API calls \(get ADOMs, get device contracts, get devices per ADOM, get interfaces per device\). For example, you can add or remove fields, change query parameters, or point at a different FortiManager URL pattern.

Default implementation: `ActionRequestBodyFortinetDefault`, matched to the `fortinet_alias` connection alias.

**Note:** The resolver matches by exact connection alias name. Your implementation's `getConnectionAlias()` function must exactly match the `name` field on the `sys_alias` record configured on the instance. If nothing matches, the connector has no request bodies and every FortiManager call fails.

## Collection steps \(FortinetCollectionPlan\)

Lets you add a FortiManager API call to the collection run — for example, a firmware-upgrade-status endpoint that doesn't exist in the out-of-box connector. You can also control the dependency order of collection steps and how each response is turned into stored data.

Default implementation: `FortinetCollectionPlan`, which declares the `contracts`, `adoms`, and `devices` steps.

**Note:** Your implementation must return all three existing steps plus any new one you add. Omitting `contracts`, `adoms`, or `devices` removes that built-in collection entirely; the connector doesn't merge your implementation with the default plan.

## CI attributes \(FortinetFieldMappings\)

Lets you expose additional fields from the FortiManager response as CI attributes on devices, ports, organizations, network sites, and network service instances, without writing custom enrichment logic.

Default implementation: `FortinetFieldMappings`.

**Note:** Add fields only to the `additional_attributes` list. Don't change core identity fields such as `key`, `name`, `serial_number`, `ip_address`, `class`, or `company` — doing so can break how the connector recognizes the same CI across runs.

## Additional attributes \(FortinetCustomAttributes\)

Lets you compute extra `additional_attributes` in script for devices, organizations, network sites, network service instances, and ports, for logic too involved to express as a `FortinetFieldMappings` entry. Your custom attributes are merged with the attributes the connector already computed for that entity, and win on any key conflict.

Default implementation: `FortinetDefaultCustomAttributes`, which returns no additional attributes.

**Note:** All five methods — `device`, `organization`, `network_site`, `network_service_instance`, and `port` — are required. If your implementation is missing any of them, the connector skips it entirely and logs a warning naming the missing methods. Return an empty object, `{}`, from a method you don't need to customize.

## Enrichment hooks \(FortinetParserHooks\)

Provides hooks into the extraction pipeline that run as each raw API item is turned into a CI or import-set payload. Use these hooks for customizations that a field mapping alone can't express, such as pulling in data collected earlier in the same run. Combined with a custom collection plan step, you can use this extension point to support an entirely new CI type.

Default implementation: `FortinetParserHooks`, which fetches each device's ports and license data before mapping, and creates network sites and service instances after.

|Handler|Runs|
|-------|----|
|`unwrapResponse`|Once per fetched API response, before any item is mapped. Normalizes the response into the array to iterate over.|
|`beforeExtract`|Once per raw item, before field mapping runs. The default implementation uses this to attach a device's ports and license data.|
|`afterExtract`|Once per item, after field mapping runs. The default implementation uses this to create network sites and service instances.|
|`postProcess`|Once per response, with the full array of items already mapped for that type.|
|`shouldStore`|Once per mapped item. Return `false` to exclude that item from the shared store entirely.|

**Note:** All five required handlers must be present in your implementation, or the connector rejects it entirely, logs an error naming the missing handlers, and falls back to the default implementation. Start your implementation from a copy of the default's device-handling logic rather than writing it from scratch — dropping that logic silently removes port attachment and site or service-instance creation for every device.

Three further handlers are optional, and only needed if a custom collection plan step introduces a new entity type. `getEntityTypes` registers the new type's key in the shared store. `getWriteKeyMap` controls the top-level key it's written under. `getDerivedWriteTypes` marks it as written automatically after collection finishes, for a type built entirely in `beforeExtract`/`afterExtract` rather than fetched from its own API call.

## Firmware version string \(FortinetCustomizedFirmwareVersion\)

Lets you change how the firmware version string stored on a device CI is built, for customers who display firmware versions differently than FortiManager's raw `os_ver`, `mr`, and `patch` fields.

Default implementation: `FortinetDefaultFirmwareVersion`, which joins the three fields with periods \(for example, `7.4.11`\).

## License contract parsing \(FortinetCustomizedContractParsing\)

Lets you change how a license contract item string is turned into a named license-expiration attribute. FortiManager returns license contract data as an opaque string \(for example, `COMP-1-20-20290503:0:1:1:0`\); customers with a different license format need a different parser.

Default implementation: `FortinetDefaultContractParsing`, which extracts the expiration date and service code from the standard Fortinet format.

For the steps to customize this extension point, see [Customize scripted extension points](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/configure-extension-points.md).

## ADOM filtering \(FortinetCustomizedAdomFilter\)

Lets you exclude entire ADOMs from collection based on business criteria beyond the standard IP, name, device model, or organization filters. For example, you can collect only ADOMs flagged for a specific service.

Default implementation: `FortinetDefaultAdomFilter`. This implementation is included but disabled by default; every ADOM is collected.

**Note:** This extension point fails closed, not open. If no implementation is active, all ADOMs pass through. But once an implementation is active and it throws an error, the connector collects zero ADOMs rather than falling back to collecting everything. Test any custom filter carefully before activating it.

## Life Cycle Stage Status \(FortinetCustomizedLifeCycleStageStatus\)

Lets you set a CI's **Life Cycle Stage Status** value differently per CI class — for example, a router might default to `In Use` while a decommissioned-looking interface should read `In Maintenance`.

Default implementation: returns `In Use` for every CI class.

**Note:** Unlike the other seven extension points, this one doesn't run during data collection. A business rule on `cmdb_ci` calls it when a CI record is created or updated, after the import set has already been transformed into a CI.

**Parent Topic:**[Telecommunications Service Operations Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/components-installed-with-tsom.md)

**Related topics**  


[Customize scripted extension points](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/configure-extension-points.md)

[Configure a Fortinet SD-WAN Service Graph Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/configure-fortinet-service-graph-connector.md)

