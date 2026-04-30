---
title: Using Machine Learning APIs
description: Use ServiceNow Machine Learning \(ML\) APIs to train Machine Learning models and run inferences.This section briefly describes classes for training ML solutions and running inferences with trained solutions.Follow this example breakdown to learn how to configure and train a solution.Follow these example breakdowns to learn how to manage trained solution versions.
locale: en-US
release: xanadu
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Using Predictive Intelligence, Predictive Intelligence, Enable AI experiences]
---

# Using Machine Learning APIs

Use ServiceNow Machine Learning \(ML\) APIs to train Machine Learning models and run inferences.

ML APIs enable training solutions and managing solution versions. You can get and set active versions, monitor training status, and more. The ML API also provides encoders, which enable using term frequency–inverse document frequency \(TF-IDF\) as a word corpus. Predictability estimates enable assessing the predictive value of table columns.

**Note:** Predictive Intelligence APIs run with full privileges before the Vancouver Patch 7 Hotfix 2b and Washington DC Patch 7 releases. With later releases, grant access using ACLs. For more information see [Query ACLs](https://www.servicenow.com/docs/access?context=query-acl-rule&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## ML API class overview

This section briefly describes classes for training ML solutions and running inferences with trained solutions.

-   **Datasets**

    A dataset is a set of records including a table name, columns, and row selection criteria to use as input for ML training algorithms. Datasets don't contain the actual data.

    For more information, see [DatasetDefinition](https://www.servicenow.com/docs/access?context=DatasetDefinitionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

-   **ML objects – Solutions, Encoders, and Estimates**

    ML objects define a specific training configuration to apply on a dataset. Some operations are common across ML objects. Solution objects include classification, clustering, regression, and similarity.

    Encoders are text processing objects that are either pre-trained or trained based on the language datasets you provide. You can train encoders that determine how the system interprets and processes text fields. For ML solutions that include text, you can train an encoder to specify how to process text and use the trained encoder in a solution.

    PredictabilityEstimate objects estimate which fields in a dataset are predictable and the features on which this predictability is based.

    For more information, see:

    -   [ClassificationSolution](https://www.servicenow.com/docs/access?context=ClassificationSolutionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
    -   [ClusteringSolution](https://www.servicenow.com/docs/access?context=ClusteringSolutionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
    -   [Encoder](https://www.servicenow.com/docs/access?context=EncoderAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
    -   [PredictabilityEstimate](https://www.servicenow.com/docs/access?context=PredictabilityEstimateAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
    -   [RegressionSolution](https://www.servicenow.com/docs/access?context=RegressionSolutionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
    -   [SimilaritySolution](https://www.servicenow.com/docs/access?context=SimilaritySolutionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
-   **Stores**

    ML objects are maintained in a specific store for each object type. Each store class includes methods for add, get, update, and delete operations.

    For more information, see:

    -   [ClassificationSolutionStore](https://www.servicenow.com/docs/access?context=ClassificationSolutionStoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
    -   [ClusteringSolutionStore](https://www.servicenow.com/docs/access?context=ClusteringSolutionStoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
    -   [EncoderStore](https://www.servicenow.com/docs/access?context=EncoderStoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
    -   [PredictabilityEstimateStore](https://www.servicenow.com/docs/access?context=PredictabilityEstimateStoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
    -   [RegressionSolutionStore](https://www.servicenow.com/docs/access?context=RegressionSolutionStoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
    -   [SimilaritySolutionStore](https://www.servicenow.com/docs/access?context=SimilaritySolutionStoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
-   **Versions**

    Each trained object results in a new version that you can run tasks on. Use the version API to get any solution version and run tasks on it.

    For more information, see:

    -   [ClassificationSolutionVersion](https://www.servicenow.com/docs/access?context=ClassificationSolutionVersionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
    -   [ClusteringSolutionVersion](https://www.servicenow.com/docs/access?context=ClusteringSolutionVersionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
    -   [EncoderVersion](https://www.servicenow.com/docs/access?context=EncoderVersionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
    -   [PredictabilityEstimateVersion](https://www.servicenow.com/docs/access?context=PredictabilityEstimateVersionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
    -   [RegressionSolutionVersion](https://www.servicenow.com/docs/access?context=RegressionSolutionVersionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
    -   [SimilaritySolutionVersion](https://www.servicenow.com/docs/access?context=SimilaritySolutionVersionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

### Putting it together: ML API flows

You can use the following flow to configure and train solutions, encoders, and predictability estimates:

![This image illustrates the API flow from defining dataset, creating a ML object, adding the ML object to a store, and training the ML object.](../images/ml-api-flow-solution1.png "ML API flow – Solution, encoder, and estimate training")

**Note:** The encoder definitions support multiple dataset definitions, but have the same training flow.

To train a solution with an encoder, create the encoder first, then include the encoder in the solution configuration.

![This image illustrates the API flow from defining dataset, creating a solution object specifying an existing encoder, adding the solution to a store, and training the solution.](../images/ml-api-flow-solution2-encoder.png "ML API flow – Solution API training with encoder")

ML object encoder requirements:

-   Required in similarity API solutions.
-   Required in clustering API solutions, unless using the Levenshtein distance algorithm, in which case encoders are optional.
-   Optional for classification and regression solutions.
-   Unavailable for predictability estimates.

## Getting started with ML API solution training

Follow this example breakdown to learn how to configure and train a solution.

-   **Configure and train a solution**

    ![This image illustrates the API flow from defining dataset, creating a classification solution object, adding the solution to a store, and training the solution.](../images/ml-api-flow-classification.png)

    1.  Define a dataset using the [DatasetDefinition](https://www.servicenow.com/docs/access?context=DatasetDefinitionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US) API.

        ```
        var myData = new sn_ml.DatasetDefinition({
        
          'tableName' : 'incident',
          'fieldNames' : ['assignment_group', 'short_description', 'description'],
          'encodedQuery' : 'activeANYTHING'
        
        });
        ```

    2.  Use the constructor to define the solution, including the dataset in the configuration.

        ```
        var mySolution = new sn_ml.ClassificationSolution({
        
          'label': "my solution definition",
          'dataset' : myData,
          'predictedFieldName' : 'assignment_group',
          'inputFieldNames':['short_description']
        
        });
        ```

        -   [ClassificationSolution\(\)](https://www.servicenow.com/docs/access?context=ClassificationSolutionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
        -   [ClusteringSolution\(\)](https://www.servicenow.com/docs/access?context=ClusteringSolutionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
        -   [Encoder\(\)](https://www.servicenow.com/docs/access?context=EncoderAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
        -   [PredictabilityEstimate\(\)](https://www.servicenow.com/docs/access?context=PredictabilityEstimateAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
        -   [RegressionSolution\(\)](https://www.servicenow.com/docs/access?context=RegressionSolutionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
        -   [SimilaritySolution\(\)](https://www.servicenow.com/docs/access?context=SimilaritySolutionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
    3.  Add the solution definition to the store using the add\(\) method.

        ```
        var my_unique_name = sn_ml.ClassificationSolutionStore.add(mySolution);
        ```

        -   [ClassificationSolutionStore - add\(\)](https://www.servicenow.com/docs/access?context=ClassificationSolutionStoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
        -   [ClusteringSolutionStore – add\(\)](https://www.servicenow.com/docs/access?context=ClusteringSolutionStoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
        -   [EncoderStore - add\(\)](https://www.servicenow.com/docs/access?context=EncoderStoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
        -   [PredictabilityEstimateStore - add\(\)](https://www.servicenow.com/docs/access?context=PredictabilityEstimateStoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
        -   [RegressionSolutionStore - add\(\)](https://www.servicenow.com/docs/access?context=RegressionSolutionStoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
        -   [SimilaritySolutionStore - add\(\)](https://www.servicenow.com/docs/access?context=SimilaritySolutionStoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
    4.  Train the solution using the submitTrainingJob\(\) method. After training is complete, you can manage the trained solution using a solution version API. A solution can be retrained multiple times. Each training results in a new solution "version" on which you can run inferences.

        ```
        var myClassifierVersion = mySolution.submitTrainingJob();
        ```

        -   [ClassificationSolution - submitTrainingJob\(\)](https://www.servicenow.com/docs/access?context=ClassificationSolutionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
        -   [ClusteringSolutionVersion – submitTrainingJob\(\)](https://www.servicenow.com/docs/access?context=ClusteringSolutionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
        -   [Encoder - submitTrainingJob\(\)](https://www.servicenow.com/docs/access?context=EncoderAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
        -   [PredictabilityEstimate - submitTrainingJob\(\)](https://www.servicenow.com/docs/access?context=PredictabilityEstimateAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
        -   [RegressionSolution - submitTrainingJob\(\)](https://www.servicenow.com/docs/access?context=RegressionSolutionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
        -   [SimilaritySolution - submitTrainingJob\(\)](https://www.servicenow.com/docs/access?context=SimilaritySolutionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
-   **View all classification solutions in a store**

    You can use the store getAllNames\(\) method to see a list of all solutions that have been added to the store.

    ```
    gs.print(JSON.stringify(JSON.parse(sn_ml.ClassificationSolutionStore.getAllNames()), null, 2));
    ```

    In the output, the system has named the solution `ml_x_snc_global_global_my_solution_definition`. Use this name in subsequent examples to get version information.

    ```
    *** Script: [
      "ml_incident_assignment",
      "ml_x_snc_global_global_my_solution_definition",
      "ml_incident_categorization"
    ]
    ```

    -   [ClassificationSolutionStore - getAllNames\(\)](https://www.servicenow.com/docs/access?context=ClassificationSolutionStoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
    -   [ClusteringSolutionStore – getAllNames\(\)](https://www.servicenow.com/docs/access?context=ClusteringSolutionStoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
    -   [EncoderStore - getAllNames\(\)](https://www.servicenow.com/docs/access?context=EncoderStoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
    -   [PredictabilityEstimateStore - getAllNames\(\)](https://www.servicenow.com/docs/access?context=PredictabilityEstimateStoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
    -   [RegressionSolutionStore - getAllNames\(\)](https://www.servicenow.com/docs/access?context=RegressionSolutionStoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
    -   [SimilaritySolutionStore - getAllNames\(\)](https://www.servicenow.com/docs/access?context=SimilaritySolutionStoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

## Getting started with ML API solution versions

Follow these example breakdowns to learn how to manage trained solution versions.

-   **Check training status**

    Get the classification solution from the store, choose a version, and check its training status. The methods used for checking training status are applicable to all ML object types.

    ![This image illustrates the API flow from accessing an classification solution in the store, choosing a solution version, and checking its training status.](../images/ml-api-flow-classification-getStat.png)

    1.  Get the solution from the classification solution store using the get\(\) method.

        ```
        // Get the solution created in the previous example from the classification solution store
        var mlSolution = sn_ml.ClassificationSolutionStore.get('ml_x_snc_global_global_my_solution_definition');
        ```

        -   [ClassificationSolutionStore - get\(\)](https://www.servicenow.com/docs/access?context=ClassificationSolutionStoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
        -   [ClusteringSolutionStore – get\(\)](https://www.servicenow.com/docs/access?context=ClusteringSolutionStoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
        -   [EncoderStore - get\(\)](https://www.servicenow.com/docs/access?context=EncoderStoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
        -   [PredictabilityEstimateStore - get\(\)](https://www.servicenow.com/docs/access?context=PredictabilityEstimateStoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
        -   [RegressionSolutionStore - get\(\)](https://www.servicenow.com/docs/access?context=RegressionSolutionStoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
        -   [SimilaritySolutionStore - get\(\)](https://www.servicenow.com/docs/access?context=SimilaritySolutionStoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
    2.  Access the most recent solution version using the getLatestVersion\(\) solution method and get its training status using the getStatus\(\) version method.

        ```
        // Access the latest version of the solution and print its training status
        gs.print(JSON.stringify(JSON.parse(mlSolution.getLatestVersion().getStatus(), null, 2)));
        ```

        Output when training is complete:

        ```
        *** Script: {"state":"solution_complete","percentComplete":"100","hasJobEnded":"true"}
        ```

        |getLatestVersion\(\)|getStatus\(\)|
        |--------------------|-------------|
        |[ClassificationSolution - getLatestVersion\(\)](https://www.servicenow.com/docs/access?context=ClassificationSolutionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)|[ClassificationSolutionVersion - getStatus\(\)](https://www.servicenow.com/docs/access?context=ClassificationSolutionVersionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)|
        |[ClusteringSolution – getLatestVersion\(\)](https://www.servicenow.com/docs/access?context=ClusteringSolutionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)|[ClusteringSolutionVersion – getStatus\(\)](https://www.servicenow.com/docs/access?context=ClusteringSolutionVersionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)|
        |[Encoder - getLatestVersion\(\)](https://www.servicenow.com/docs/access?context=EncoderAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)|[EncoderVersion - getStatus\(\)](https://www.servicenow.com/docs/access?context=EncoderVersionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)|
        |[PredictabilityEstimate - getLatestVersion\(\)](https://www.servicenow.com/docs/access?context=PredictabilityEstimateAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)|[PredictabilityEstimateVersion - getStatus\(\)](https://www.servicenow.com/docs/access?context=PredictabilityEstimateVersionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)|
        |[RegressionSolution - getLatestVersion\(\)](https://www.servicenow.com/docs/access?context=RegressionSolutionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)|[RegressionSolutionVersion - getStatus\(\)](https://www.servicenow.com/docs/access?context=RegressionSolutionVersionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)|
        |[SimilaritySolution - getLatestVersion\(\)](https://www.servicenow.com/docs/access?context=SimilaritySolutionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)|[SimilaritySolutionVersion - getStatus\(\)](https://www.servicenow.com/docs/access?context=SimilaritySolutionVersionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)|

-   **Get predictions using a solution version**

    After the solution has been trained, get the trained version and run a prediction on it. Get the solution you created from the store. Next, choose the trained version and predict the trained version. ![This image illustrates the API flow from accessing classification solution in the store, choosing a solution version, and getting prediction input data.](../images/ml-api-flow-classification-predict.png)

    **Note:** Predictions cannot be made on encoders and predictability estimates.

    1.  Get the solution from the classification solution store using the get\(\) method.

        ```
        // Get the solution created in the first example from the classification solution store
        var mlSolution = sn_ml.ClassificationSolutionStore.get('ml_x_snc_global_global_my_solution_definition');
        ```

    2.  Use the [GlideRecord](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US) API get\(\) method to provide a record from the Incident \[incident\] table.

        ```
        // single GlideRecord input
        var input = new GlideRecord("incident");
        input.get("<sys_id>");
        ```

    3.  Optional. Configure the ClassificationSolutionVersion – predict\(\) method **options** parameter to return the top three results and return all results.

        ```
        // configure optional parameters
        var options = {};
        options.top_n = 3;
        options.apply_threshold = false;
        ```

    4.  Declare a variable called `results` and assign it to the prediction job. To run the prediction job, get the most recent solution version using the ClassificationSolution – getLatestVersion\(\) method and call the ClassificationSolutionVersion – predict\(\) method on it.

        ```
        var results = mlSolution.getLatestVersion().predict(input, options);
        ```

        -   [ClassificationSolutionVersion - predict\(\)](https://www.servicenow.com/docs/access?context=ClassificationSolutionVersionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
        -   [ClusteringSolutionVersion – predict\(\)](https://www.servicenow.com/docs/access?context=ClusteringSolutionVersionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
        -   [RegressionSolutionVersion - predict\(\)](https://www.servicenow.com/docs/access?context=RegressionSolutionVersionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
        -   [SimilaritySolutionVersion - predict\(\)](https://www.servicenow.com/docs/access?context=SimilaritySolutionVersionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
    5.  Print the predicted results output.

        ```
        gs.print(JSON.stringify(JSON.parse(results), null, 2));
        ```

        Predicted results example output:

        ```
        *** Script: {
          "<sys_id>": [
            {
              "confidence": 99,
              "threshold": 24.75,
              "predictedValue": "Email",
              "predictedSysId": ""
            },
            {
              "confidence": 5.88210244009169,
              "threshold": 100,
              "predictedValue": "Email (I/f)",
              "predictedSysId": ""
            },
            {
              "confidence": 2.3461203499840932,
              "threshold": 14.81,
              "predictedValue": "Authentication",
              "predictedSysId": ""
            }
          ]
        }
        ```


