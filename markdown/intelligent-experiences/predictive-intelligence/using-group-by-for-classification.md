---
title: Using Group By for classification
description: Use APIs to simultaneously submit multiple classification solutions for training based on the Group By field.
locale: en-US
release: xanadu
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: concept
last_updated: "2024-10-04"
reading_time_minutes: 2
breadcrumb: [Create and train a classification solution, Creating and training solutions, Predictive Intelligence, Enable AI experiences]
---

# Using Group By for classification

Use APIs to simultaneously submit multiple classification solutions for training based on the Group By field.

You can use the optional Group By capability to train and maintain one classification solution that covers more than one data area, such as geographical location or domain.

To train a solution using Group By, you must add the groupby parameter while creating a classification solution definition using APIs. The groupby parameter accepts only categorical columns as inputs, where individual models are created on the subset of data belonging to each of the groupby values. Only those child solutions that pass the minimum records criteria set for the capability are created. Here, the prediction calls are routed to the corresponding Group By model based on the Group By value present in the prediction input. Batch predictions are not supported.

## A Group By scenario for geographical locations

Let's say your global company uses classification routing for incoming records, with one support center in the US and one in Europe. Here, you want to create a single classification solution that has one model for your United States incidents and another model for your European incidents.

In this scenario, you could use one of these two approaches:

-   Create and train two separate ML classification solution definitions, where one is filtered by US incidents only, and one by European incidents only.
-   Use the groupby parameter to create Groupby for the country location so that all US definitions create a US model and all European definitions create a European model. Then, based on the incident, the system identifies which model it uses to predict the correct classification category.

The second approach has benefits in that the models you use can even be in different domains, such as healthcare or finance. This approach is especially beneficial if you have several country locations or domains to maintain.

## Example usage for training and prediction using Group By via API

```
var myIncidentData = new sn_ml.DatasetDefinition({
    'tableName' : 'incident',
    'fieldNames' : ['category','short_description','assignment_group','description','priority'],
    'encodedQuery' : 'activeANYTHING'
});

var mySolution = new sn_ml.ClassificationSolution({
    'label': 'solution label',
    'dataset' : myIncidentData,
    'groupByFieldName' : 'assignment_group',
    'predictedFieldName': 'category',
    'inputFieldNames': ['short_description','description','priority']
});
//Add solution definition
var solution_gr = sn_ml.ClassificationSolutionStore.add(mySolution)
//Get existing solution
var my_unique_name = sn_ml.ClassificationSolutionStore.get('solution name');
// submit training job
var solutionVersion = my_unique_name.submitTrainingJob();


// Run prediction
var input = new GlideRecord("incident");
input.get("sys_id");
// configure optional parameters
var options = {};
options.apply_threshold = false;
var mlSolution = sn_ml.ClassificationSolutionStore.get('solution name');
//Prediction using glide record
var results = mlSolution.getActiveVersion().predict(input, options);
//Prediction using map
var results = mlSolution.getActiveVersion().predict([{ 'short_description': input.short_description,
                                                         'assignment_group': input.assignment_group }], options);
```

For more context regarding this example and the general usage of Machine Learning APIs, see the links in the Related Content section on this page.

**Related topics**  


[DatasetDefinition - Global](https://www.servicenow.com/docs/access?context=DatasetDefinitionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

[ClassificationSolution - Global](https://www.servicenow.com/docs/access?context=ClassificationSolutionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

[ClassificationSolutionStore - Global](https://www.servicenow.com/docs/access?context=ClassificationSolutionStoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

[ClassificationSolutionVersion - Global](https://www.servicenow.com/docs/access?context=ClassificationSolutionVersionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

