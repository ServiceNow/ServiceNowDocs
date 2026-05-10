---
title: Using Machine Learning APIs
description: Use ServiceNow Machine Learning \(ML\) APIs to train Machine Learning models and run inferences.This section briefly describes classes for training ML solutions and running inferences with trained solutions.Follow this example procedure to learn how to configure and train a solution.Follow these example breakdowns to learn how to manage trained solution versions.
locale: en-US
release: australia
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Using Predictive Intelligence, Predictive Intelligence, Enable AI experiences]
---

# Using Machine Learning APIs

Use ServiceNow Machine Learning \(ML\) APIs to train Machine Learning models and run inferences.

ML APIs enable training solutions and managing solution versions. You can get and set active versions, monitor training status, and more. The ML API also provides encoders, which enable using term frequency–inverse document frequency \(TF-IDF\) as a word corpus. Predictability estimates enable assessing the predictive value of table columns.

**Note:** Predictive Intelligence APIs run with full privileges before the Vancouver Patch 7 Hotfix 2b and Washington DC Patch 7 releases. With later releases, grant access using ACLs. For more information see [Query ACLs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/query-acl-rule.md).

## ML API class overview

This section briefly describes classes for training ML solutions and running inferences with trained solutions.

-   **Datasets**

    A dataset is a set of records including a table name, columns, and row selection criteria to use as input for ML training algorithms. Datasets don't contain the actual data.

    For more information, see [DatasetDefinition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/DatasetDefinitionAPI.md).

-   **ML objects – Solutions, Encoders, and Estimates**

    ML objects define a specific training configuration to apply on a dataset. Some operations are common across ML objects. Solution objects include classification, clustering, regression, and similarity.

    Encoders are text processing objects that are either pre-trained or trained based on the language datasets you provide. You can train encoders that determine how the system interprets and processes text fields. For ML solutions that include text, you can train an encoder to specify how to process text and use the trained encoder in a solution.

    PredictabilityEstimate objects estimate which fields in a dataset are predictable and the features on which this predictability is based.

    For more information, see:

    -   [ClassificationSolution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/ClassificationSolutionAPI.md)
    -   [ClusteringSolution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/ClusteringSolutionAPI.md)
    -   [Encoder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/EncoderAPI.md)
    -   [PredictabilityEstimate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/PredictabilityEstimateAPI.md)
    -   [RegressionSolution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/RegressionSolutionAPI.md)
    -   [SimilaritySolution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/SimilaritySolutionAPI.md)
-   **Stores**

    ML objects are maintained in a specific store for each object type. Each store class includes methods for add, get, update, and delete operations.

    For more information, see:

    -   [ClassificationSolutionStore](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/ClassificationSolutionStoreAPI.md)
    -   [ClusteringSolutionStore](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/ClusteringSolutionStoreAPI.md)
    -   [EncoderStore](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/EncoderStoreAPI.md)
    -   [PredictabilityEstimateStore](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/PredictabilityEstimateStoreAPI.md)
    -   [RegressionSolutionStore](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/RegressionSolutionStoreAPI.md)
    -   [SimilaritySolutionStore](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/SimilaritySolutionStoreAPI.md)
-   **Versions**

    Each trained object results in a new version that you can run tasks on. Use the version API to get any solution version and run tasks on it.

    For more information, see:

    -   [ClassificationSolutionVersion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/ClassificationSolutionVersionAPI.md)
    -   [ClusteringSolutionVersion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/ClusteringSolutionVersionAPI.md)
    -   [EncoderVersion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/EncoderVersionAPI.md)
    -   [PredictabilityEstimateVersion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/PredictabilityEstimateVersionAPI.md)
    -   [RegressionSolutionVersion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/RegressionSolutionVersionAPI.md)
    -   [SimilaritySolutionVersion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/SimilaritySolutionVersionAPI.md)

### Putting it together: ML API flows

You can use the following flow to configure and train solutions, encoders, and predictability estimates:

1.  Define a dataset \(DatasetDefinition\)
2.  Create an ML object \(Solution/Encoder/PredictabilityEstimate\)
3.  Add to store \(Store\)
4.  Train \(Solution/Encoder/PredictabilityEstimate\)

**Note:** The encoder definitions support multiple dataset definitions, but have the same training flow.

To train a solution with an encoder, create the encoder first, then include the encoder in the solution configuration.

1.  Create an encoder \(Encoder\)
2.  Define a dataset \(DatasetDefinition\)
3.  Create solution specifying encoder \(Solution\)
4.  Add to store \(SolutionStore\)
5.  Train \(Solution\)

ML object encoder requirements:

-   Required in similarity API solutions.
-   Required in clustering API solutions, unless using the Levenshtein distance algorithm, in which case encoders are optional.
-   Optional for classification and regression solutions.
-   Unavailable for predictability estimates.

## Getting started with ML API solution training

Follow this example procedure to learn how to configure and train a solution.

-   **Configure and train a solution**
    1.  Define a dataset using the [DatasetDefinition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/DatasetDefinitionAPI.md) API.

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

        -   [ClassificationSolution\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/ClassificationSolutionAPI.md)
        -   [ClusteringSolution\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/ClusteringSolutionAPI.md)
        -   [Encoder\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/EncoderAPI.md)
        -   [PredictabilityEstimate\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/PredictabilityEstimateAPI.md)
        -   [RegressionSolution\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/RegressionSolutionAPI.md)
        -   [SimilaritySolution\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/SimilaritySolutionAPI.md)
    3.  Add the solution definition to the store using the add\(\) method.

        ```
        var my_unique_name = sn_ml.ClassificationSolutionStore.add(mySolution);
        ```

        -   [ClassificationSolutionStore - add\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/ClassificationSolutionStoreAPI.md)
        -   [ClusteringSolutionStore – add\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/ClusteringSolutionStoreAPI.md)
        -   [EncoderStore - add\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/EncoderStoreAPI.md)
        -   [PredictabilityEstimateStore - add\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/PredictabilityEstimateStoreAPI.md)
        -   [RegressionSolutionStore - add\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/RegressionSolutionStoreAPI.md)
        -   [SimilaritySolutionStore - add\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/SimilaritySolutionStoreAPI.md)
    4.  Train the solution using the submitTrainingJob\(\) method. After training is complete, you can manage the trained solution using a solution version API. A solution can be retrained multiple times. Each training results in a new solution "version" on which you can run inferences.

        ```
        var myClassifierVersion = mySolution.submitTrainingJob();
        ```

        -   [ClassificationSolution - submitTrainingJob\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/ClassificationSolutionAPI.md)
        -   [ClusteringSolutionVersion – submitTrainingJob\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/ClusteringSolutionAPI.md)
        -   [Encoder - submitTrainingJob\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/EncoderAPI.md)
        -   [PredictabilityEstimate - submitTrainingJob\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/PredictabilityEstimateAPI.md)
        -   [RegressionSolution - submitTrainingJob\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/RegressionSolutionAPI.md)
        -   [SimilaritySolution - submitTrainingJob\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/SimilaritySolutionAPI.md)
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

    -   [ClassificationSolutionStore - getAllNames\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/ClassificationSolutionStoreAPI.md)
    -   [ClusteringSolutionStore – getAllNames\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/ClusteringSolutionStoreAPI.md)
    -   [EncoderStore - getAllNames\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/EncoderStoreAPI.md)
    -   [PredictabilityEstimateStore - getAllNames\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/PredictabilityEstimateStoreAPI.md)
    -   [RegressionSolutionStore - getAllNames\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/RegressionSolutionStoreAPI.md)
    -   [SimilaritySolutionStore - getAllNames\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/SimilaritySolutionStoreAPI.md)

## Getting started with ML API solution versions

Follow these example breakdowns to learn how to manage trained solution versions.

-   **Check training status**

    Get the classification solution from the store, choose a version, and check its training status. The methods used for checking training status are applicable to all ML object types.

    1.  Get the solution from the classification solution store using the get\(\) method.

        ```
        // Get the solution created in the previous example from the classification solution store
        var mlSolution = sn_ml.ClassificationSolutionStore.get('ml_x_snc_global_global_my_solution_definition');
        ```

        -   [ClassificationSolutionStore - get\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/ClassificationSolutionStoreAPI.md)
        -   [ClusteringSolutionStore – get\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/ClusteringSolutionStoreAPI.md)
        -   [EncoderStore - get\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/EncoderStoreAPI.md)
        -   [PredictabilityEstimateStore - get\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/PredictabilityEstimateStoreAPI.md)
        -   [RegressionSolutionStore - get\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/RegressionSolutionStoreAPI.md)
        -   [SimilaritySolutionStore - get\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/SimilaritySolutionStoreAPI.md)
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
        |[ClassificationSolution - getLatestVersion\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/ClassificationSolutionAPI.md)|[ClassificationSolutionVersion - getStatus\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/ClassificationSolutionVersionAPI.md)|
        |[ClusteringSolution – getLatestVersion\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/ClusteringSolutionAPI.md)|[ClusteringSolutionVersion – getStatus\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/ClusteringSolutionVersionAPI.md)|
        |[Encoder - getLatestVersion\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/EncoderAPI.md)|[EncoderVersion - getStatus\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/EncoderVersionAPI.md)|
        |[PredictabilityEstimate - getLatestVersion\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/PredictabilityEstimateAPI.md)|[PredictabilityEstimateVersion - getStatus\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/PredictabilityEstimateVersionAPI.md)|
        |[RegressionSolution - getLatestVersion\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/RegressionSolutionAPI.md)|[RegressionSolutionVersion - getStatus\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/RegressionSolutionVersionAPI.md)|
        |[SimilaritySolution - getLatestVersion\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/SimilaritySolutionAPI.md)|[SimilaritySolutionVersion - getStatus\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/SimilaritySolutionVersionAPI.md)|

-   **Get predictions using a solution version**

    After the solution has been trained, get the trained version and run a prediction on it. Get the solution you created from the store. Next, choose the trained version and predict the trained version.

    **Note:** Predictions cannot be made on encoders and predictability estimates.

    1.  Get the solution from the classification solution store using the get\(\) method.

        ```
        // Get the solution created in the first example from the classification solution store
        var mlSolution = sn_ml.ClassificationSolutionStore.get('ml_x_snc_global_global_my_solution_definition');
        ```

    2.  Use the [GlideRecord](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/c_GlideRecordAPI.md) API get\(\) method to provide a record from the Incident \[incident\] table.

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

        -   [ClassificationSolutionVersion - predict\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/ClassificationSolutionVersionAPI.md)
        -   [ClusteringSolutionVersion – predict\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/ClusteringSolutionVersionAPI.md)
        -   [RegressionSolutionVersion - predict\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/RegressionSolutionVersionAPI.md)
        -   [SimilaritySolutionVersion - predict\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/SimilaritySolutionVersionAPI.md)
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


