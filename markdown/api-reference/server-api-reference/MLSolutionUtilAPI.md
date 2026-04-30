---
title: MLSolutionUtil - Global
description: The MLSolutionUtil script include provides methods for getting Predictive Intelligence predictions.Instantiates a new MLSolutionUtil object.Gets predictions for one or more specified solutions.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# MLSolutionUtil- Global

The MLSolutionUtil script include provides methods for getting Predictive Intelligence predictions.

This script include requires the Predictive Intelligence plugin \(com.glide.platform\_ml\) and is provided within the `sn_ml` namespace.

For more information, see [Using ML APIs](https://www.servicenow.com/docs/access?context=using-ml-apis&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

**Related topics**  


[MLSolution](../../MLSolution/concept/MLSolutionAPI.md#)

[MLSolutionFactory](../../MLSolutionFactory/concept/MLSolutionFactoryAPI.md#)

## MLSolutionUtil - MLSolutionUtil\(\)

Instantiates a new MLSolutionUtil object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

```

var mlSolutionUtil = new MLSolutionUtil();

```

## MLSolutionUtil - getPredictions\(Object input, Array solutionNames, Object options\)

Gets predictions for one or more specified solutions.

<table id="table_hqw_pbm_yfb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

input

</td><td>

Object

</td><td>

GlideRecord or array of JSON objects as key-value pairs.

</td></tr><tr><td>

solutionNames

</td><td>

Array

</td><td>

Array of solution names to retrieve predictions from.

</td></tr><tr><td>

options

</td><td>

Object

</td><td>

Optional. JSON object key-value pair with the following properties:-   top\_n: Number. If provided, returns the top results, up to the specified number of predictions.
-   apply\_threshold: Boolean. Checks the threshold value for the solution and applies it to the result set. The threshold value is solution threshold for similarity or class-level threshold for classification. Default value is true.
-   custom\_results\_filter: String. Similarity solutions only. Specifies the allowed set from which results are returned using an encoded query.

</td></tr></tbody>
</table><table id="table_iqw_pbm_yfb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array

</td><td>

JSON key-value pair containing the prediction result grouped by solution name and sorted by sys\_id or record\_number.-   predictedValue: String. Value representing the prediction result.
-   predictedSysId: String. The sys\_id of the predicted value. Results can be from any table on which information is being predicted.
-   confidence: Number. Value of the confidence associated with the prediction. For example, 53.84.
-   threshold: Number. Value of the configured threshold associated with the prediction.

</td></tr></tbody>
</table>```
var solutionNames = ['soluton1', 'solution2'];

var input = new GlideRecord("incident");
input.get("0ef47232db801300864adfea5e961912");

// configure optional parameters
var options = {};
options.top_n = 3;
options.apply_threshold = false;

var mlSolutionUtil = new MLSolutionUtil();
var results = mlSolutionUtil.getPredictions(input, solutionNames, options);

// pretty print JSON results
gs.print(JSON.stringify(JSON.parse(results), null, 2));
```

Output:

```
{
  solution1:  {
    input_gr_sys_id1: [
                {
                    predictedValue : xxx,
                    predictedSysId : xx0,
                    confidence : xxx,
                    threshold : xxx

                }, 
                {
                    predictedValue : yyy,
                    predictedSysId : xx1,
                    confidence : xxx,
                    threshold : xxx
                }
        ],
    input_gr_sys_id2 : [
                {
                    predictedValue : xxx,
                    predictedSysId : xx0,
                    confidence : xxx,
                    threshold : xxx

                }, 
            ...
        ]
  }

  solution2:  {
      ...
}
```

