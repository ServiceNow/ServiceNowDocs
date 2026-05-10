---
title: MLSolutionFactory - Global
description: The MLSolutionFactory API is a factory class to get an MLSolution scriptable object.Gets an MLSolution object for a specified solution name.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# MLSolutionFactory - Global

The MLSolutionFactory API is a factory class to get an MLSolution scriptable object.

This API requires the Predictive Intelligence plugin \(com.glide.platform\_ml\) and is provided within the `sn_ml` namespace. For more information, see [Predictive Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictive-intelligence/predictive-intelligence.md).

For usage guidelines, refer to [MLSolutionFactory scriptable objects](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictive-intelligence/using-ml-apis-mlsolutionfactory.md).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

**Related topics**  


[MLSolution](../../MLSolution/concept/MLSolutionAPI.md#)

[MLSolutionUtil](../../MLSolutionUtil/concept/MLSolutionUtilAPI.md#)

[REST API: Get predictions for multiple solutions](../../../../../integrate/inbound-rest/concept/agent-intelligence-api.md#)

## MLSolutionFactory - getSolution\(String solutionName, Object options\)

Gets an MLSolution object for a specified solution name.

|Name|Type|Description|
|----|----|-----------|
|solutionName|String|Name of the solution.|
|options|Object|Optional. options.version: If provided, creates MLSolution instance for provided version of solutionName.|

|Type|Description|
|----|-----------|
|Object|[MLSolution](../../MLSolution/concept/MLSolutionAPI.md#) object of the specified solution.|

```
// basic usage
var mlSolution = sn_ml.MLSolutionFactory.getSolution("ml_incident_categorization");
        
```

```
// using options.version parameter
var options = {};
options.version = 1;
var mlSolution = sn_ml.MLSolutionFactory.getSolution("ml_incident_categorization", options);
```

