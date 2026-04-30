---
title: Train the similarity model
description: Train your similar record models with training data to predict the similar records by recognizing similarities between fields of Incident table and training tables.
locale: en-US
release: zurich
product: Task Intelligence for ITSM
classification: task-intelligence-for-itsm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Set up, Create a similar records prediction model, Manage, Task Intelligence for ITSM, IT Service Management]
---

# Train the similarity model

Train your similar record models with training data to predict the similar records by recognizing similarities between fields of Incident table and training tables.

## Before you begin

You can set up a task intelligence model or use the base system template that is shipped with Task Intelligence for ITSM. For more information on setting up a new model, see [Set up similar records prediction model](set-up-similar-records-prediction-model.md)

Role required: sn\_ti\_admin.tia\_admin or sn\_itsm\_ml\_task.ti\_admin 

## About this task

When you train a machine learning model, the model looks at the prediction fields of a prediction table and the training fields of a training table. It uses the similarities in these fields to predict similar records.

You can select the table and fields that you want to predict, such as the Prediction table and Predictions fields. Also, you can select the tables and fields that you want the model to use to predict the similar records, such as the Training table and Training fields.  Select this information to tell the model what to look for during training .

**Note:** You can either use the recommended settings or customize the settings to fit your needs. 

## Procedure

1.  Enter a name for the model. 

2.  Select the **Prediction table** you want the model to predict. 

3.  Select **Conditions** to choose a set of records to use for training.

    The selected conditions determine how the model is trained. These conditions provide the requirements that a record must meet to make the predictions.

4.  Select the **Prediction fields** which will be used to predict similar records. 

    ![UI of the prediction table with its conditions and the prediction fields.](../image/TI_configure_similarity_model_predictions.png)

5.  Choose the set of records used for training the similar records model by selecting the conditions on the training tables and training fields for training the similarity models.

    **Note:** This field appears only when you select **Problem** or **Change Requests** training table in the **Define your Purpose** page. If you select the prediction table and training table as Incident, the conditions selected in Step 3 is applied on both prediction and training tables \(In this case both are incident tables\) to generate training records that are used for prediction.

6.  Select the **Training table** in the training data that you want the model to use to make predictions. 

7.  Select the **Training** fields that you want the model to use to make predictions. 

8.  Select the **Language** in which training takes place.

9.  Select the **Update Frequency** to decide how frequently the training should occur.

    ![UI of the training table and training fields section.](../image/TI_training_fields.png)

10. Review the resulting **Number of records** in the training data based on the selected conditions. 

    The records that are counted include the number of fields, parameters, and data that the model uses to train. Based on the provided information and the set conditions, the number or records gets updated automatically. The model needs a minimum of 10,000 records for effective training. If this minimum number hasn't been reached, try selecting different conditions. You can also click the refresh icon \(![get latest matrix refresh](../../service-operations-workspace/image/get-latest-matrix.png)\) to refresh the number.![UI of the "Review the resulting number of records" section](../image/TI_review_results.png)

11. Set a  **Training Frequency **to define how often the model automatically retrains.

    ![UI of the "Retraining configurations" section](../image/TI_Retraining_configuration.png)

12. Select **Launch training**.


## Result

If you’re training the model on a large amount of data, training can take some time. You can request that the system sends you an email when the training is done.

**Parent Topic:**[Set up similar records prediction model](set-up-similar-records-prediction-model.md)

