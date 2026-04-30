---
title: Config parameters for model config in classification
description: Customize the training behavior of your classification solution by passing in a dictionary of parameters in JSON format.
locale: en-US
release: zurich
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring advanced settings for your ML solutions, Configure Predictive Intelligence, Predictive Intelligence, Enable AI experiences]
---

# Config parameters for model config in classification

Customize the training behavior of your classification solution by passing in a dictionary of parameters in JSON format.

## Before you begin

Role required: ml\_admin or admin

## About this task

You can fine-tune model performance by passing in a dictionary of parameters to adjust training behavior.

Understand the machine learning hyperparameters relevant to your model objective. This option is advanced and should be modified with care.

You can add these parameters in the solution definition form by using the following procedure.

Alternatively, you can use a script to add these parameters. For the format to use when scripting, see the **What to do next** section of this page.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Classification** &gt; **Solution Definitions**.

2.  Open an existing classification solution or create a new one.

3.  Select the **Advanced Solution Settings** tab in the **Related Links** section of the form.

4.  Select **New** to open the **Advanced Solution Setting** \(ml\_advanced\_solution\_settings\) form.

5.  In the **Solution Parameters** field, search for `Config parameters for model config in classification`.

6.  In the **User Inputs** field, enter the following key-value pairs, after editing the values per your requirements.

    **Note:** When pasting the parameters into the solution definition form, don't include JSON's enclosing label, braces, or parentheses. Enter the key-value pairs in the format shown here, after editing the values according to your requirements.

    ```
    'max_depth': 10,'learning_rate': 0.1,'objective': 'multi:softprob','num_class': 11,'random_state': 10,'eval_metric': 'mlogloss','booster': 'gbtree','n_estimators': 150,'verbosity': 1,'use_label_encoder': false,'tree_method': 'hist','num_parallel_tree': 1,'gamma': 0.25,'subsample': 0.8,'max_delta_step': 5,'reg_alpha': 0,'reg_lambda': 1,'colsample_bytree': 0.8,'colsample_bylevel': 1,'colsample_bynode': 1,'min_child_weight': 1.25,'n_jobs': 11,'validate_parameters': true
    ```

7.  Select **Submit** to update the solution definition.


## Result

The setting appears as a row on the **Advanced Solution Setting** tab on your solution's form.

![On the Solution Definition form, in the Advanced Solutions Settings tab, config parameters is highlighted.](../images/predictive-intel-config-parameters-classificationZ1.png)

## What to do next

Retrain your solution.

You can also pass in this dictionary with a script. Be sure to use the enclosing label, braces, and parentheses when scripting.

Script example:

```
config.setModelParams({                   
                    'max_depth': 10,                   
                    'learning_rate': 0.1,
                    'objective': 'multi:softprob',
                    'num_class': 11,
                    'random_state': 10,
                    'eval_metric': 'mlogloss',
                    'booster': 'gbtree',
                    'n_estimators': 150,
                    'verbosity': 1,
                    'use_label_encoder': false,
                    'tree_method': 'hist',
                    'num_parallel_tree': 1,
                    'gamma': 0.25,
                    'subsample': 0.8,
                    'max_delta_step': 5,
                    'reg_alpha': 0,
                    'reg_lambda': 1,
                    'colsample_bytree': 0.8,
                    'colsample_bylevel': 1,
                    'colsample_bynode': 1,
                    'min_child_weight': 1.25,
                    'n_jobs': 11,
                    'validate_parameters': true
                    });
```

JSON example:

```
        
            {                    
              "classification_model_params": {
                'max_depth': 10,
                'learning_rate': 0.1,
                'objective': 'multi:softprob',
                'num_class': 11,
                'random_state': 10,
                'eval_metric': 'mlogloss',
                'booster': 'gbtree',
                'n_estimators': 150,
                'verbosity': 1,
                'use_label_encoder': false,
                'tree_method': 'hist',
                'num_parallel_tree': 1,
                'gamma': 0.25,
                'subsample': 0.8,
                'max_delta_step': 5,
                'reg_alpha': 0,
                'reg_lambda': 1,
                'colsample_bytree': 0.8,
                'colsample_bylevel': 1,
                'colsample_bynode': 1,
                'min_child_weight': 1.25,
                'n_jobs': 11,
                'validate_parameters': true
                }
              }
```

**Related topics**  


[Using Machine Learning APIs](../concept/using-ml-apis.md#)

[Create and train a classification solution](create-solution-definition.md)

