---
title: Counter connector methods
description: The Counter connector methods increment, decrement, or reset integers as part of an automation Workflow in RPA Desktop Design Studio. All methods have properties that you can update.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/counter-connector-methods.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Counter, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Counter connector methods

The Counter connector methods increment, decrement, or reset integers as part of an automation Workflow in RPA Desktop Design Studio. All methods have properties that you can update.

## Up

Increments an integer by the value that you specify.

To provide input, see [Configure port properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Value|Custom integer value|Data In|Integer|1|Yes|

To view or update the properties, see [Counter method properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/counter-method-properties.md).

## Down

Decrements an integer by the value that you specify. The default integer is 1.

To provide input, see [Configure port properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory|
|---------|-----------|--------------|---------|-------------|---------|
|Value|Custom integer value|Data In|Integer|1|Yes|

To view or update the properties, see [Counter method properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/counter-method-properties.md).

## Value

Returns the value after incrementing or decrementing an integer in the Up or Down methods.

**Note:** You must execute the Up or Down method before executing the Value method.

|Parameter|Description|Data port type|Data type|Default value|Mandatory|
|---------|-----------|--------------|---------|-------------|---------|
|Return|Incremented or decremented value|Data Out|Integer|0|Yes|

To update the properties, see [Counter method properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/counter-method-properties.md).

## Reset

Resets the current value in the Value method to `null`.

**Note:** You must execute the Reset method after executing the Value method.

To view or update the properties, see [Counter method properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/counter-method-properties.md).

## Example

The following example shows the use of the Counter connector methods.\[Omitted image "counter-connector-illustration.png"\] Alt text: Counter connector methods.

**Parent Topic:**[Counter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/counter.md)

