---
title: Model Explainability
description: Analyze the importance of each input field to your model's predictions using model explainability. Create a Workflow Classification model that includes a graphical analysis of feature importance by executing the provided script.
locale: en-US
release: australia
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create and train a classification solution, Creating and training solutions, Predictive Intelligence, Enable AI experiences]
---

# Model Explainability

Analyze the importance of each input field to your model's predictions using model explainability. Create a Workflow Classification model that includes a graphical analysis of feature importance by executing the provided script.

## Before you begin

-   This method uses the Workflow Classification Solution API, instead of the Solution Definition form, to create and train a model with explainability added. For information about the components of Workflow Classification models, see [Create and train a classification solution](create-solution-definition.md).
-   Role required: ml\_admin or admin

## About this task

Model explainability helps identify the key features that influence the model's predictions during training.

**Note:** Explainability can't be added to an existing model. This method uses a script to create and train a new Workflow Classification model. For more information about scripting the creation of Classification solutions, see ClassificationSolution - Global.

The script provided in the procedure creates and trains a model with explainability set to true. On the new model's solution form, an additional tab labeled **Feature Importance** appears. This tab offers a graph of the relative contribution of each input to the prediction.![On the Solution form, the Feature Importance tab is highlighted. In the output (predicted) field, the value Global is selected, and an example graph is displayed.](../images/predictive-intel-explainability1.png)

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scripts - Background**.

2.  Edit the query filter and table, field, and variable values in the following script according to your planned model, then execute the script.

    ```
    // Define a dataset
                        var myIncidentData = new sn_ml.DatasetDefinition({
                        'tableName': 'incident',
                        'fieldNames': ['category', 'short_description', 'sys_updated_by', 'assignment_group', 'description', 'priority'],
                        'encodedQuery': 'activeANYTHING'
                        });
                        
                        // Define a classification solution definition with explainability field
                        var mySolution = new sn_ml.ClassificationSolution({
                        'label': 'model explainability',
                        'dataset': myIncidentData,
                        'predictedFieldName': 'category',
                        'inputFieldNames': ['short_description', 'priority'],
                        //setting the explainability field to true.
                        'explainability': true,
                        });
                        
                        // Add solution to ClassificationSolutionStore
                        var my_unique_name = sn_ml.ClassificationSolutionStore.add(mySolution)
                        
                        // Submit training job
                        var solutionVersion = mySolution.submitTrainingJob();
                    
    ```

    **Note:** Substitute the query filter and table, field, and variable names in this script with your own values.

3.  Navigate to the ML Solutions \[ml\_solution\] table and open your new solution by selecting the value of its **Active** field.

4.  On the solution form, locate and open the **Feature Importance** tab.

    **Feature Importance** displays a drop-down list.

    ![On the Feature Importance tab, the drop-down list containing the range of possible classes for the output field.](../images/explainability-supplement.png)

    -   The label for this drop-down list is the name of your output \(predicted\) field, so the label is specific to each model.
    -   The values in the drop-down list are the possible output classes for your output field, plus the **Global** option.
<table id="choicetable_afh_pny_12c"><thead><tr><th align="left" id="d167647e157">

List option

</th><th align="left" id="d167647e160">

Description

</th></tr></thead><tbody><tr><td id="d167647e166">

**__Global__**

</td><td>

Provides an overview of how the model behaves across all predictions, showing the overall impact of each input feature.Select **Global** to open a graph of the importance of your input fields to predictions for all output classes as a whole.

</td></tr><tr><td id="d167647e181">

**`Your output class value`**

</td><td>

Focuses on the model's behavior for the chosen class only, showing how input features contribute to predictions on a per-class basis.Select one of the possible output classes to open a graph of the importance of your input fields to predictions for that class.

</td></tr></tbody>
</table>5.  Launch the graphical analysis by selecting a value from the drop-down list.

    The y axis shows your input fields and the x axis shows the numerical importance for each input. The label of the graph reflects the class that you chose in the drop-down list. ![On the Feature Importance tab, one of the possible output classes is selected. An example graph is displayed, illustrating the importance of the input fields to predictions for this class.](../images/predictive-intel-explainability2.png)

    You can hover over a bar to display the numerical percentage for each input's importance.


## Result

A positive importance value means that the input field increases the model's prediction score. A negative value means that the input field decreases the prediction score.

## What to do next

Consider dropping input fields with low importance scores. Retrain your model after modification.

**Related topics**  


[Using Machine Learning APIs](../concept/using-ml-apis.md#)

[bundle-crapiref.ClassificationSolutionAPI]

[Create and train a classification solution](create-solution-definition.md)

