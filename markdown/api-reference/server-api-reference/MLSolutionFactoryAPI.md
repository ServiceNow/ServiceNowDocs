---
title: MLSolutionFactory - Global
description: The MLSolutionFactory API is a factory class to get an MLSolution scriptable object.Gets an MLSolution object for a specified solution name.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/server-api-reference/MLSolutionFactoryAPI.html
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

This API requires the Predictive Intelligence plugin \(com.glide.platform\_ml\) and is provided within the `sn_ml` namespace. For more information, see [Predictive Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictive-intelligence.md).

For usage guidelines, refer to [MLSolutionFactory scriptable objects](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/using-ml-apis-mlsolutionfactory.md).

**Parent Topic:**[Server API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/api-server.md)

**Related topics**  


[MLSolution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/MLSolutionAPI.md)

[MLSolutionUtil](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/MLSolutionUtilAPI.md)

[REST API: Get predictions for multiple solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/agent-intelligence-api.md)

## MLSolutionFactory - getSolution\(String solutionName, Object options\)

Gets an MLSolution object for a specified solution name.

|Name|Type|Description|
|----|----|-----------|
|solutionName|String|Name of the solution.|
|options|Object|Optional. options.version: If provided, creates MLSolution instance for provided version of solutionName.|

|Type|Description|
|----|-----------|
|Object|[MLSolution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/MLSolutionAPI.md) object of the specified solution.|

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

