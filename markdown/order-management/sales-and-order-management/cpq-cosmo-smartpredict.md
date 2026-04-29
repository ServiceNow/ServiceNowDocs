---
title: Cosmo SmartPredict
description: Cosmo SmartPredict delivers AI-powered, in-context recommendations during configuration, helping users make informed decisions. It learns from live or uploaded data to generate accurate suggestions, improving configuration speed and consistency across blueprints. For clarity, suggestions are labeled Good, Better, or Best.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [CPQ, Configure, price, quote, Explore, Sales and Order Management]
---

# Cosmo SmartPredict

Cosmo SmartPredict delivers AI-powered, in-context recommendations during configuration, helping users make informed decisions. It learns from live or uploaded data to generate accurate suggestions, improving configuration speed and consistency across blueprints. For clarity, suggestions are labeled Good, Better, or Best.

Cosmo SmartPredict provides users with fast, in-context, predictive recommendations as they complete their configurations. SmartPredict can be trained either on existing configurations that are stored in the CPQ environment or on data that is uploaded via a CSV file.

Cosmo SmartPredict leverages a strong underlying AI model, but depends on the quantity and the quality of the data that it is provided for training.

## Setting up Cosmo SmartPredict

Access to Cosmo SmartPredict is restricted. To have SmartPredict provisioned in your CPQ environment, contact support. Once provisioned, SmartPredict can be enabled on individual blueprints selectively. To enable SmartPredict on a blueprint, navigate to the blueprint, click the new Smart Predict tile in the blueprint, and click the toggle button on the SmartPredict screen.

To create a SmartPredict model, click **Create** to start defining the model parameters. At a minimum, a model must have a name and a variable name. Several additional model settings determine what data the model should use for training.

-   Training with live data

    If you choose to use live data to train your model, existing and future configurations in CPQ that use this blueprint will serve as inputs to refine the model for the fields in the blueprint. You can further refine the training data by defining a start date and by specifying inclusion or exclusion of fields. You can create additional filters based on field values. Any filtering of the training data is optional. If all other parameters are left blank, the model will be trained on all existing configurations of the blueprint. Once finished setting parameters, click **Save &amp; Train** to begin training the model.

    Optional filtering parameters include:

    -   Start date: Choose a start date \(inclusive\) of configurations to train on. If blank, configurations will not be filtered by created date.
    -   Fields: Individual fields on the blueprint can be selected to be either included or excluded.
    -   Additional filters: To filter the training configuration data down to only those that match the filter criteria, you can select individual fields and enter equals criteria.
-   Training with data from a CSV file

    Models can also be trained with data from external sources by formatting and uploading the data as a CSV file. In CSV data, the first row must be the variable names of the fields. You can download a sample CSV file with all the fields on the blueprint from the CSV upload page.

    When formatting the CSV file, you can choose to provide only a subset of the available fields on the blueprint.

    -   Fields: The column header should be the variable name of the field that the values are provided for. Only fields that are of a type that can be predicted are used in training: Boolean, number, picklist, sets, and product pickers. Text fields are not predicted and are not used in training.
    -   Multiselect picklists: Provide multiple values of a picklist using commas with no spaces.
    -   Sets and product pickers: The formatting for set and product picker fields is `SetVariableName_index_fieldVariableName` or `ProductPickerVariableName_index_fieldVariableName`, using: 0, 1, or 2 for indexes, and the variable name for the fields, sets, or product pickers.

Once a model has been saved, it is queued for training based on the uploaded data or the filtered live data. Training is variable based on the amount of data that is supplied, but typically takes a few hours, or at most, a day. Once the model has completed training, it can be activated and deployed.

Models are retrained if the filters, fields, or start date are changed when the model is using live data. If new CSV data is uploaded, the model is retrained. Models using live data continue to be trained on live data periodically. When the model is being automatically trained with new live data, there is no need to redeploy the blueprint to have it use the updated model.

## Using Cosmo SmartPredict

Once a model has been trained for a blueprint, it can be activated. Multiple SmartPredict models can be trained, but only one model can be active on a blueprint at any time. If a model is changed or activated for a blueprint, the blueprint must be redeployed to use the new model.

For an end user to trigger the recommendations from Cosmo SmartPredict, approximately 5% of the fields must be filled in with a value.

Predicted field types include numbers, picklists, Boolean values, sets \(including number, picklist, and Boolean fields\), product pickers, and subfields of all these types. Text fields are not predicted.

Three types of recommendations are provided to the user: Good, Better, and Best. These recommendations correspond to the model predictions based on the training data. As always, the quality of the data heavily influences the quality of the predictions.

Recommendations can change based on the fields that are filled out. Fields that are user-edited will not have a prediction.

If sets or product pickers are included in the predictions, all the fields in a set or product picker row have a predicted value.

## SmartPredict V1 and V2

Two models of SmartPredict are available: V1 and V2. While the V1 model remains available, V2 has superior capabilities.

The V2 model introduces several key enhancements and changes compared to its predecessor:

-   Enhanced prediction confidence: V2 is engineered to provide higher-confidence predictions, typically offering a single, highly probable recommendation to guide your decisions.
-   Broader field support: Prediction capabilities now extend to include sets and product picker fields, significantly widening its applicability across your configurations.
-   Expanded prediction options: Unlike V1, V2 is not restricted to predicting three indexes or options for sets and product pickers, allowing for more comprehensive and flexible suggestions.
-   Training data accessibility: Administrators can download the CSV training data used for any scenario from in the platform, offering greater transparency and control.

However, V2 model training times are significantly longer. For data sets of a few thousand rows, training typically ranges from 30 to 60 minutes. Furthermore, the model requires activation via the scenario list page. Activation consistently takes from 20 to 40 minutes, regardless of the training data size.

The V1 model remains operational, providing a smooth transition period as you consider whether to adopt V2.

Your input on the accuracy, performance, and overall experience with the V2 model is crucial for our continuous improvement. We are eager to hear about your experiences and celebrate the successes of customers leveraging AI in configuration. Please share your feedback with our support or product teams.

## Notes and recommendations

Our AI model infrastructure requires substantial resources. To effectively manage capacity, models that have not been accessed for a prolonged period or exhibit very low usage may be automatically deactivated. Should your model be deactivated, you can easily reactivate it from the scenario list page. Allow approximately 20-40 minutes for the reactivation process to complete before predictions become available again.

In general, about 400 configurations are required to have a robust data set on which to train the model.

As with any AI model, the quality of the training data is the main factor in the quality of the predictions.

