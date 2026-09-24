---
title: Extensibility in Meraki discovery
description: The Meraki connector defines its own scripted extension points. Use them to customize API call sequencing, response parsing, field mappings, tag transformation, and CI lifecycle stage status without modifying the connector's core scripts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/meraki-discovery-extensibility.html
release: brazil
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [meraki extensibility extension points collection plan parser hooks field mappings tag transformation lifecycle stage status]
breadcrumb: [Telecom Discovery via Cisco Meraki SD-WAN, Indirect Discovery with SGCs, Telecom Discovery, Telecom Visibility, Explore, Telecommunications Service Operations Management]
---

# Extensibility in Meraki discovery

The Meraki connector defines its own scripted extension points. Use them to customize API call sequencing, response parsing, field mappings, tag transformation, and CI lifecycle stage status without modifying the connector's core scripts.

The Meraki connector exposes five scripted extension points, each registered in the connector's own **sn\_sgc\_meraki** scope. Each extension point is a separate customization surface: you can implement one, several, or none, and each is evaluated independently at runtime.

## What you can customize

The MerakiCollectionPlan extension point controls which API calls the connector makes, in what order, and how each response is routed. Use it to add, remove, or reorder collection steps, or to change how a step's response is fetched and written.

The MerakiParserHooks extension point controls how a raw API response is unwrapped, enriched, filtered, and stored before it reaches field mapping. Use it to register additional entity types and to customize the five required handlers: unwrapResponse, beforeMapping, afterMapping, postProcess, and shouldStore.

**Note:**

The MerakiParserHooks handlers beforeMapping and afterMapping were previously named beforeExtract and afterExtract. Rename the handlers in a custom implementation to the current names.

The MerakiFieldMappings extension point controls how raw Meraki API data is mapped into CI fields. Use it to add or change entries inside a resource type's **additional\_attributes** block. Core CI identity fields such as **key**, **name**, and **serial\_number** can't be changed this way.

The TagTransformationExtensionPoint extension point controls how an array of Meraki tag strings is converted into key/value pairs for CMDB attribute mapping.

The MerakiCustomizedLifeCycleStageStatus extension point controls the life cycle stage status value assigned to a CI, per CI class.

For the full handler contract for each extension point, see the [Meraki extension points reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/meraki-extension-points-reference.md).

## How implementations are selected

For MerakiCollectionPlan, the connector uses the first registered implementation whose getCollectionPlan handler is defined. An implementation missing getCollectionPlan is skipped and an error naming the missing handler is logged. If no registered implementation is valid, the connector falls back to its default collection plan.

For MerakiParserHooks, the connector uses the first registered implementation that defines all five required handlers: unwrapResponse, beforeMapping, afterMapping, postProcess, and shouldStore. An implementation missing any of the five is rejected in full rather than partially merged, and an error naming the missing handlers is logged. If no registered implementation is valid, the connector falls back to its default parser hooks.

For MerakiFieldMappings, the connector uses the first registered implementation whose getFieldMappings handler returns every required resource-type key. An implementation that's missing a required key is skipped and an error naming the missing keys is logged. If no registered implementation is valid, the connector falls back to its default field mappings.

For TagTransformationExtensionPoint, the connector uses the first registered implementation whose handles handler returns **true** for the Meraki source identifier.

For MerakiCustomizedLifeCycleStageStatus, the connector uses the first registered implementation that defines the getLifeCycleStageStatus handler, and uses its returned value directly.

**Note:**

A default implementation of each extension point ships with the connector and is registered out of the box at **order** **100**. Adding a custom implementation doesn't replace the default one automatically — give your implementation's extension instance a lower **order** value so it's evaluated first. You don't need to deactivate the default extension instance.

