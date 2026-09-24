---
title: Cisco Meraki extension points
description: Each Meraki extension point controls one part of the connector's data collection. Use these tables to find the handler that governs the behavior you want to change and the arguments it receives.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/meraki-extension-points-reference.html
release: brazil
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 5
keywords: [meraki extension points collection plan parser hooks field mappings tag transformation lifecycle stage status handlers reference]
breadcrumb: [Reference, Telecommunications Service Operations Management]
---

# Cisco Meraki extension points

Each Meraki extension point controls one part of the connector's data collection. Use these tables to find the handler that governs the behavior you want to change and the arguments it receives.

## Extension points

The Meraki connector exposes five scripted extension points, each registered in the connector's own `sn_sgc_meraki` scope: `MerakiCollectionPlan`, `MerakiParserHooks`, `MerakiFieldMappings`, `TagTransformationExtensionPoint`, and `MerakiCustomizedLifeCycleStageStatus`. A default implementation of each ships with the connector and is registered out of the box.

## MerakiCollectionPlan

Controls which API calls the connector makes, in what order, and how each response is routed. Before any data is fetched, the connector reads the active implementation's collection plan and sorts its steps by their `dependsOn` declarations into execution levels. A circular dependency stops collection.

|Handler|Required|Controls|
|-------|--------|--------|
|getCollectionPlan\(constants\)|Yes|Returns the collection plan object, keyed by step name. Each step's **url** function returns the endpoint path. **fetch.scope** and **fetch.strategy** control whether the step is fetched once or once per parent entity. **dependsOn** lists step names that must finish first. **write** is `deferred` or `immediate` with **writeKeys**. A step that defines **onResponse** handles its own response directly, bypassing MerakiParserHooks and MerakiFieldMappings for that step.|
|getConstants\(\)|No|Returns additional named constants available to step definitions, merged over the connector's built-in constants.|

**Warning:**

An implementation must return the `organization`, `networks`, and `devices` steps in addition to any step you add. Omitting one of these from a custom plan silently drops that collection — the connector doesn't merge your implementation with the default plan.

## MerakiParserHooks

Controls how a raw API response is unwrapped, enriched, filtered, and stored. An implementation can also register additional entity types for a collection plan step that introduces a brand-new type. In every handler, `type` is the step name from the active collection plan.

|Handler|Arguments|Controls|
|-------|---------|--------|
|unwrapResponse|`responseJson`, `type`, `parser`|Once per fetched response, before any item is mapped. Returns the value to iterate over, usually an array.|
|beforeMapping|`rawItem`, `type`, `store`, `parser`|Once per raw item, before field mapping. Mutates `rawItem` in place so a mapping can reference the added data as a normal source path. Returns nothing.|
|afterMapping|`mappedItem`, `type`, `store`, `rawItem`, `parser`|Once per item, after field mapping. Mutates `mappedItem` in place to add attributes or relationships that depend on the mapped shape. Returns nothing.|
|postProcess|`results`, `type`, `parser`|Once per response, with every item already mapped for that type. Returns the items to store or write, optionally filtered or transformed.|
|shouldStore|`mappedItem`, `type`, `parser`|Per item. Returns **false** to exclude the item from the shared store.|

**Note:**

An implementation missing any of the five required handlers is rejected in full, not partially merged. The connector logs an error naming the missing handlers and falls back to the default implementation.

beforeMapping and afterMapping were previously named beforeExtract and afterExtract. Rename the handlers in a custom implementation to the current names.

|Handler|Controls|
|-------|--------|
|getEntityTypes\(constants\)|Registers extra entity type keys in the shared store. Required if a custom `MerakiCollectionPlan` step introduces a brand-new type.|
|getWriteKeyMap\(constants\)|Returns extra `{ entityType: outputKey }` entries merged over the out-of-box write key map. Use this when a deferred-write entity type should be emitted under a different top-level key than its store key.|
|getDerivedWriteTypes\(\)|Returns extra entity type keys whose entities are built during parsing, such as inside afterMapping, rather than fetched from their own collection plan step. The connector writes these types automatically after deferred writes complete.|

## MerakiFieldMappings

Controls how raw Meraki API data is mapped into CI fields. The connector uses the first registered implementation whose getFieldMappings handler returns every required resource-type key. An implementation that's missing a required key is skipped, an error naming the missing keys is logged, and the connector tries the next registered implementation. If no implementation is valid, the connector falls back to its default field mappings.

|Handler|Required|Controls|
|-------|--------|--------|
|getFieldMappings|Yes|Returns the field mappings object, keyed by resource type. The returned object must include an entry for every required resource type: `networks`, `organization`, `devices`, `device_statuses`, `networkSites`, `uplink_status`, `switch_ports`, and `device_inventory`. Add or change fields only inside a resource type's `additional_attributes` block — changing a core CI attribute such as **key**, **name**, **serial\_number**, or **company** can break CI identity resolution and deduplication.|
|getTransforms|No|Returns an object mapping custom transform names to functions, for use with the `transform` property in a field mapping entry. Each transform function runs with the active parser instance as `this`, giving access to `this.store` and `this.log`. Return `null` if you have no custom transforms. Custom transform names can't reuse a built-in transform name.|

|Property|Description|
|--------|-----------|
|**source**|Dot-path into the raw API object, for example `deviceStatus.ip_address`. Pass an array of paths to forward multiple values to a **transform**.|
|**value**|A hardcoded value, used when no source field exists.|
|**transform**|Name of a transform function, built-in or from getTransforms, that post-processes the resolved source value.|
|**defaultValue**|Fallback value used when the source resolves to `null` or `undefined`.|
|**isArray**|Marks the field as an array placeholder with no source mapping.|
|**expandArray**|Flattens an array value into individual entries.|
|**mapArray**|A nested mapping applied to each element of a source array.|
|**$parent**|In a **mapArray** context, a prefix used to access the parent record's fields.|

**Note:**

The following transform names are built in and can't be overridden from getTransforms: lookupOrgName, lookupNetworkCompany, transformTags, defaultIfNull, defaultIfNullOrEmpty, roundNumberToTwoDecimalPlaces, getNetworkSiteKey, getSiteName, getSiteAddress, getOrgIdFromNetwork, getInterfaceKey, getInterfaceModel, getInterfacePosition, getInterfaceBandwidth, getInterfaceBandwidthName, getInterfaceBandwidthGroup, getPortName, and getPortPosition.

## TagTransformationExtensionPoint

Controls how an array of Meraki tag strings is converted into key/value pairs for CMDB attribute mapping. The connector uses the first registered implementation whose handles handler returns **true** for the Meraki source identifier.

|Handler|Arguments|Controls|
|-------|---------|--------|
|handles|`sourceSystem`|Whether this implementation applies to the given source system. The connector calls this handler with the source identifier `meraki-SDWAN`; return **true** to have this implementation used.|
|transform|`tags`|Converts an array of tag strings into an array of `{key, value}` pairs used for CMDB attribute mapping. Only called on the implementation selected by handles.|

## MerakiCustomizedLifeCycleStageStatus

Controls the life cycle stage status value assigned to a CI, per CI class. The connector uses the first registered implementation that defines the getLifeCycleStageStatus handler, and uses its returned value directly. This handler only runs when a CI doesn't already have a life cycle stage status set.

|Handler|Arguments|Controls|
|-------|---------|--------|
|getLifeCycleStageStatus|`entityClass`|Returns the life cycle stage status string for a given CI class, such as `cmdb_ci_ip_router`. The default implementation returns `In Use` for every CI class.|

**Parent Topic:**[Telecommunications Service Operations Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/components-installed-with-tsom.md)

