---
title: Structure of a data collector
description: This section describes the structure of a PaCE data collector.
locale: en-US
release: australia
product: Policy as Code Engine \(PaCE\)
classification: policy-as-code-engine-pace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Passing parameters to PaCE policies, Administer PaCE policies, Policy as Code Engine \(PaCE\), Extend ServiceNow AI Platform capabilities]
---

# Structure of a data collector

This section describes the structure of a PaCE data collector.

When you create a data collector, you can add inputs and outputs in the Javascript code. In the Data sources tab, select **Add** to create the inputs and outputs you want to add to your data collector. The following images show the pop-up window that will show up when you select **Add** under the Input or Output tab.

![Add data collector input tab.](../image/pace-data-collector-add-input.jpg)

![Add data collector output tab.](../image/pace-data-collector-add-output.jpg)

The following image shows a sample data collector:

To debug the data collector script, select the Debugger script icon ![Debugger icon](../image/pace-debug-icon.jpg). For more information, see [Script Debugger API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/scriptdebugger-api.md).

The following table lists the data collector function parameters and how they can be used in the script.

|Variable name|Description|
|-------------|-----------|
|Input|Inputs are used as parameters that help collect the correct data to be used in the policy.|
|Output|The parameter is used to pass the output of the data collector. Outputs are used to specify output variables that can be used in the policy logic.|

Refer to the [Data type descriptions](../reference/pace-data-type-descriptions.md) topic to see a list of the supported data types for the inputs and outputs.

