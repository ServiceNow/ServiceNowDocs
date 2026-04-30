---
title: MLPredictor - Global \(deprecated\)
description: The MLPredictor API provides utility methods for Predictive Intelligence predictions.Instantiates a new MLPredictor object.Sets predicted values from an array of specified solutions to a specified record.Applies a predicted value from a specified classification solution to the specified GlideRecord.Gets the solution object.Gets active solutions for a table in a specified GlideRecord.Gets the predicted value for a specified solution based on the specified prediction outcome.Gets predictions for a specified solution.Identifies if a solution object is a classification type.Identifies if a solution object is a similarity type.Gets the confidence of the predicted value.Gets the predicted value from the MLPredictor outcome object.Gets the sys\_id of the predicted value.Sets final prediction result values to a specified GlideRecord with an optionally specified reason.Gets the capability information of a trained solution.Gets the name of the solution used for prediction.Gets the predicted value of a solution.Gets the solution threshold.Gets the version of the active solution.Determines if the specified solution is active.Gets solution prediction results as an Outcome object.Returns a list of outcome objects up to the expected number of predictions. Maximum number 1000 predictions.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 10
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# MLPredictor- Global \(deprecated\)

The MLPredictor API provides utility methods for Predictive Intelligence predictions.

**Note:** This API has been deprecated and is intended to be removed in a future release. Refer to [Using ML APIs](https://www.servicenow.com/docs/access?context=using-ml-apis&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for the most recent guidelines.

The MLPredictor API requires the Predictive Intelligence plugin \(com.glide.platform\_ml\) and is provided within the `sn_ml` namespace.

This class contains all methods necessary to get prediction results from input data.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## MLPredictor - MLPredictor\(\)

Instantiates a new MLPredictor object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

The following example shows how to use an MLPredictor object in a business rule to record final values after a prediction.

```
function executeRule(current, previous /*null when async*/) {
	var predictor = new MLPredictor();
	predictor.recordFinalValuesInPredictionResults(current, "On close");

}(current, previous);
```

## MLPredictor - applyPrediction\(GlideRecord now\_GR, Array solutions\)

Sets predicted values from an array of specified solutions to a specified record.

|Name|Type|Description|
|----|----|-----------|
|now\_GR|GlideRecord|The record on which to apply the array of predicted solutions.|
|solutions|Array|Specified solution objects associated with the GlideRecord.|

|Type|Description|
|----|-----------|
|void| |

The following example demonstrates using the applyPrediction\(\) method in a business rule.

```
(function executeRule(current, previous /*null when async*/) {
    var mlPredictor = new MLPredictor();
    //Get the list of active solutions for the glide record table
    var solutions = mlPredictor.findActiveSolutionsForRecord(current);
    //Run prediction and apply predicted value to the record
    mlPredictor.applyPrediction(current, solution);

})(current, previous);
```

## MLPredictor - applyPredictionForSolution\(GlideRecord now\_GR, Object solution\)

Applies a predicted value from a specified classification solution to the specified GlideRecord.

For each solution in the GlideRecord, call this method to predict the results and set the field value on the incident to those results.

|Name|Type|Description|
|----|----|-----------|
|now\_GR|GlideRecord|GlideRecord object containing values on which to run a prediction and apply the results.|
|solution|Object|Classification solution object to be executed.|

|Type|Description|
|----|-----------|
|Boolean|True upon prediction success, error otherwise.|

To use this template, copy the Incident Based Prediction \(Template\) business rule, make the new record Active, and follow the commented instructions to initialize the solutionNames variable.

```
(function executeRule(current, previous /*null when async*/) {
	var solutionNames = ["solution1", "solution2", ...];

	/* For domain separation (MSP) use case */
//	var solutionNames;
//	if (current.sys_domain == "A")
//		solutionNames = ["solution_A1", "solution_A2", ...];
//	else if (current.sys_domain == "B")
//		solutionNames = ["solution_B1", "solution_B2", ...];
//	else
//		...

	var predictor = new MLPredictor();
	var info = "";
	solutionNames.forEach(function(solutionName) {
		var solution = predictor.findActiveSolution(solutionName);
		if (!solution)
			return;

		/* The next line of code does the prediction and updates the current record. */
		predictor.applyPredictionForSolution(current, solution);

		/* If no prediction is done, do not build the prediction info message. */
		if (!predictor.applyPredictionForSolution(current, solution))
			return;

		/* If user doesn't have 'itil' role, we don't build prediction info message. */
		if (!gs.hasRole('itil'))
			return;

		/* Building prediction info message */
		var fieldName = solution.getPredictedField();
		var fieldLabel = current.getElement(fieldName).getED().getLabel();
		var predictedDisplayValue = current.getDisplayValue(fieldName);
		var msg = gs.getMessage("Predicted {0} for {1}.", [predictedDisplayValue, fieldLabel]);
		if (info.length > 0)
			info += " ";
		info += msg;
	});
	/* Print out prediction info message on screen. */
	if (info.length > 0) {
		var incidentUrl = "<a href='"+current.getLink()+"'>"+current.number+":</a>";
		gs.addInfoMessage(incidentUrl + " " + info);
	}
})(current, previous);
```

## MLPredictor - findActiveSolution\(String solutionName\)

Gets the solution object.

This method only returns the solutions if the ml\_solution definition and solution are active.

|Name|Type|Description|
|----|----|-----------|
|solutionName|String|Name of the ml\_solution record.|

|Type|Description|
|----|-----------|
|Object|Solution object for the specified `solutionName` if the ml\_solution definition and solution is active, null otherwise.|

This example takes a hard-coded value and passes it to a specified Machine Learning model. You can use the outcome and confidence variables to set values or other business logic.

```
var solutionName = 'ml_incident_assignment';
  var shortDescriptionValue = "Unable to connect!"
  var input = {
  short_description : shortDescriptionValue
  };
  var MLP = new MLPredictor();
  var solution = MLP.findActiveSolution(solutionName);
  var predictedOutcome = solution.predictText(input);
  var outcome = predictedOutcome.predictedValue();
  var confidence = predictedOutcome.confidence();
  gs.info("Predicted value: " + outcome)
  gs.info("Confidence: " + confidence)
        
```

Output:

```
DxC_ML:
        ******* Finished Prediction********* *** Script: Predicted value: Software *** Script:
        Confidence: 80.78079080096245
```

## MLPredictor - findActiveSolutionsForRecord\(GlideRecord now\_GR\)

Gets active solutions for a table in a specified GlideRecord.

|Name|Type|Description|
|----|----|-----------|
|now\_GR|GlideRecord|GlideRecord from which to collect active solution objects.|

|Type|Description|
|----|-----------|
|Array|Array of active solution objects associated with the table that the specified record is for.|

This script passes a GlideRecord \(such as an incident\), and processes all solutions for the GlideRecord, returning the values for each.

```
/* This is only to get a hard-coded GR */
     var current = new GlideRecord('incident');
     current.get('965c9e5347c12200e0ef563dbb9a7156');
     var predictor = new MLPredictor();
     var solutions = predictor.findActiveSolutionsForRecord(current);
     solutions.forEach(function(solution) {
         var outcome = solution.predict(current);
         /* Use this to set the field to the predicted value in the GlideRecord */
         var fieldName = solution.getPredictedField();
         current[fieldName] = outcome.predictedValue();
         current.update();

         gs.info("Predicted value: " + outcome.predictedValue())
         gs.info("Confidence: " + outcome.confidence())
});
```

Output \(Assignment Group prediction\):

```
DxC_ML: ******* Finished Prediction*********
        *** Script: Predicted value: Software *** Script: Confidence:
        99.74530683715315
```

Output \(Category prediction\):

```
DxC_ML:
        ******* Finished Prediction********* *** Script: Predicted value: Software *** Script:
        Confidence: 98.7172805135524
```

## MLPredictor - getPredictedValue\(Object solution, Object outcome\)

Gets the predicted value for a specified solution based on the specified prediction outcome.

|Name|Type|Description|
|----|----|-----------|
|solution|Object|Solution from which to get the predicted value.|
|outcome|Object|Prediction outcome results for the specified solution \(var outcome = solution.predict\(now\_GR\)\).|

|Type|Description|
|----|-----------|
|String|Predicted value for specified solution based on the specified outcome of the prediction.|
|Null|Returns null if the prediction confidence does not satisfy thresholds.|

## MLPredictor - getPredictions\(GlideRecord now\_GR, Object solution, Object options\)

Gets predictions for a specified solution.

<table id="table_hqw_pbm_yfb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

now\_GR

</td><td>

GlideRecord

</td><td>

GlideRecord to be predicted.

</td></tr><tr><td>

solution

</td><td>

Object

</td><td>

Solution object to be executed.

</td></tr><tr><td>

options

</td><td>

Object

</td><td>

Optional JSON object key value pair with the following properties:-   options.top\_n: If provided, returns results up to the expected number of predictions, otherwise default is read from the `glide.platform_ml.max_num_predictions` system property.
-   options.apply\_threshold: Checks the threshold value \(solution threshold for similarity, class level threshold for classification\) for the solution and applies it to the result set. Default value is true.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Array|Array of predicted outcome objects|

The following example calls a specified solution and executes predictions on it.

```
function printOutcomeArr(outcomeArr) {
gs.print('################## Results ##################');
for (var i=0; i<outcomeArr.length; i++) {
    var outcome = outcomeArr[i];
    gs.print((i+1) + ' : ' + outcome.predictedValue() + ', ' + outcome.predictedValueSysId() + ', ' + outcome.confidence());
}
}

var solutionName = 'ml_x_snc_global_prop_flip_test';
var predictor = new MLPredictor();
var solution = predictor.findActiveSolution(solutionName);

var now_GR = new GlideRecord('incident');
now_GR.get('1c741bd70b2322007518478d83673af3');

var options = {};
options.top_n = '10';            // top_n is an integer between 1 and 1000
options.apply_threshold = false; // Value can be set to true or false

printOutcomeArr(predictor.getPredictions(now_GR, solution, options));
```

## MLPredictor - isClassificationSolution\(Object solution\)

Identifies if a solution object is a classification type.

|Name|Type|Description|
|----|----|-----------|
|solution|Object|Name of the ML solution.|

|Type|Description|
|----|-----------|
|Boolean|Returns true if the input solution is a classification type, false otherwise.|

```
var isClassificationSolution = this.isClassificationSolution(solution);
 
	//classification solution each class has different threshold
	//therefore needs to get all the results from ml engine
	if (applyThreshold && isClassificationSolution) {
		var maxClassificationTopN = 50;
		outcomeArr = solution.predictTopN(now_GR, maxClassificationTopN);
	}
	else  {
	outcomeArr = solution.predictTopN(now_GR, topN);
	}
 
	if (outcomeArr === null) {
		//instead of returning null returning empty array
		return [];
	}
```

## MLPredictor - isSimilaritySolution\(Object solution\)

Identifies if a solution object is a similarity type.

|Name|Type|Description|
|----|----|-----------|
|solution|Object|Name of the ML solution; for example, ml\_incident\_categorization.|

|Type|Description|
|----|-----------|
|Boolean|Returns true if the input solution is a similarity type, false otherwise.|

## MLPredictor - outcome.confidence\(\)

Gets the confidence of the predicted value.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The estimated precision of the prediction as a percentage. For example, **53.84615375762915**.|

```
var MLP = new MLPredictor();
  var solution = MLP.findActiveSolution(solutionName);
  var predictedOutcome = solution.predictText(input);
  var outcome = predictedOutcome.predictedValue();
  var confidence = predictedOutcome.confidence();
  gs.info("Predicted value: " + outcome)
  gs.info("Confidence: " + confidence)
```

## MLPredictor - outcome.predictedValue\(\)

Gets the predicted value from the MLPredictor outcome object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Predicted value from the Outcome object.|

```
var MLP = new MLPredictor();
  var solution = MLP.findActiveSolution(solutionName);
  var predictedOutcome = solution.predictText(input);
  var outcome = predictedOutcome.predictedValue();
  var confidence = predictedOutcome.confidence();
  gs.info("Predicted value: " + outcome)
  gs.info("Confidence: " + confidence)
```

## MLPredictor - outcome.predictedValueSysId\(\)

Gets the sys\_id of the predicted value.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Predicted value sys\_id.|

```
function printOutcomeArr(outcomeArr) {
gs.print('################## Results ##################');
for (var i=0; i<outcomeArr.length; i++) {
    var outcome = outcomeArr[i];
    gs.print((i+1) + ' : ' + outcome.predictedValue() + ', ' + outcome.predictedValueSysId() + ', ' + outcome.confidence());
}
```

## MLPredictor - recordFinalValuesInPredictionResults\(GlideRecord now\_GR, String reason\)

Sets final prediction result values to a specified GlideRecord with an optionally specified reason.

|Name|Type|Description|
|----|----|-----------|
|now\_GR|GlideRecord|GlideRecord on which to set the final prediction result values.|
|reason|String|Optional. Reason for applying results.|

|Type|Description|
|----|-----------|
|void| |

In following example, the recordFinalValuesInPredictionResults\(\) method is called when the incident is closed.

```
(function executeRule(current, previous /*null when async*/) {
	var predictor = new MLPredictor();
	predictor.recordFinalValuesInPredictionResults(current, "On close");

})(current, previous);
```

## MLPredictor - solution.getCapability\(\)

Gets the capability information of a trained solution.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Definition ID and version of the trained solution, error message otherwise|

## MLPredictor - solution.getName\(\)

Gets the name of the solution used for prediction.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The name of the solution to use for predictions; for example, `ml_incident_categorization`|

## MLPredictor - solution.getPredictedField\(\)

Gets the predicted value of a solution.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Value of a solution's predicted output field|

```
/* Get a hard-coded GR */
     var current = new GlideRecord('incident');
     current.get('965c9e5347c12200e0ef563dbb9a7156');
     var predictor = new MLPredictor();
     var solutions = predictor.findActiveSolutionsForRecord(current);
     solutions.forEach(function(solution) {
         var outcome = solution.predict(current);
         /* Use this to set the field to the predicted value in the GlideRecord */

         var fieldName = solution.getPredictedField();
         current[fieldName] = outcome.predictedValue();
         current.update();
         gs.info("Predicted value: " + outcome.predictedValue())
         gs.info("Confidence: " + outcome.confidence())
});
```

## MLPredictor - solution.getThreshold\(String className\)

Gets the solution threshold.

The threshold represents a percentage reflecting the minimum prediction accuracy.

|Name|Type|Description|
|----|----|-----------|
|className|String|A specified categorical value of the solution output field|

|Type|Description|
|----|-----------|
|Number|Value of the threshold represented as a percentage between 0 and 100.|

## MLPredictor - solution.getVersion\(\)

Gets the version of the active solution.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Version of the active solution|

## MLPredictor - solution.isActive\(\)

Determines if the specified solution is active.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if the solution is active, false otherwise|

## MLPredictor - solution.predict\(GlideRecord now\_GR, Object threshold\)

Gets solution prediction results as an Outcome object.

|Name|Type|Description|
|----|----|-----------|
|now\_GR|GlideRecord|GlideRecord of the solution input table|
|threshold|Object|Threshold value \(solution level threshold for similarity, class level threshold for classification\)|

|Type|Description|
|----|-----------|
|Object|Prediction outcome result of the specified solution \(var outcome = solution.predict\(now\_GR\)\)|

```
solutions.forEach(function(solution) {
         var outcome = solution.predict(current);
         /* Use this to set the field to the predicted value in the GlideRecord
         var fieldName = solution.getPredictedField();
         current[fieldName] = outcome.predictedValue();
         current.update();
         */
         gs.info("Predicted value: " + outcome.predictedValue())
         gs.info("Confidence: " + outcome.confidence())
});
```

## MLPredictor - solution.predictTopN\(GlideRecord now\_GR, Object topN\)

Returns a list of outcome objects up to the expected number of predictions. Maximum number 1000 predictions.

|Name|Type|Description|
|----|----|-----------|
|now\_GR|GlideRecord|GlideRecord of the solution|
|topN|Object|Expected number of predictions, any number over 1000 returns 1000 results|

|Type|Description|
|----|-----------|
|Array|List of outcome objects in an array including GlideRecord, threshold, system ID, and expected number of predictions \(topN object\)|

```
var isClassificationSolution = this.isClassificationSolution(solution);
 
	//classification solution each class has different threshold
	//therefore needs to get all the results from ml engine
	if (applyThreshold && isClassificationSolution) {
		var maxClassificationTopN = 50;
		outcomeArr = solution.predictTopN(now_GR, maxClassificationTopN);
	}
	else  {
		outcomeArr = solution.predictTopN(now_GR, topN);
	}
 
	if (outcomeArr === null) {
		//instead of returning null returning empty array
		return [];
	}
```

