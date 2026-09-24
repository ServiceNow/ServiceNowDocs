---
title: Test time explainability
description: Understand the reasons your machine learning solution made a specific prediction with Test time explainability, which returns a list of input features that influenced the prediction.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/predictive-intelligence/predictive-intel-test-time-explain.html
release: brazil
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Create and train a classification solution, Creating and training solutions, Predictive Intelligence, Machine learning and natural language capabilities, Enable AI Experiences]
---

# Test time explainability

Understand the reasons your machine learning solution made a specific prediction with Test time explainability, which returns a list of input features that influenced the prediction.

## Overview of Test time explainability

When Test time explainability \(TTE\) is enabled on a classification solution, every prediction is accompanied by an explanation that lists each input feature along with a contribution score. Features with the largest contribution scores are the strongest drivers of that individual prediction.

## Benefits of Test time explainability

-   Transparency: Explanations turn scores into confident decisions.
-   Accountability: Each prediction comes with a per-decision record of the factors that combined to shape the result.
-   Faster troubleshooting: Unexpected predictions are easier to investigate using the list of factors and their influence.

## Considerations for using Test time explainability

Be aware of the following considerations when using Test time explainability \(TTE\).

-   TTE supports only workflow Classification solutions.
-   TTE supports only the xgboost classifier method. Don't change the classifier\_method when the TTE flag is enabled.
-   TTE is turned off by default. You must set TTE to true during training and predicting.
-   TTE can be applied to nominal \(categorical\) and numeric columns only, not text columns. If input features consist of a mix of text, nominal, and numeric columns, the text columns are dropped. If the input features consist of text columns only, the solution training fails.

## Invoking Test time explainability

Test time explainability is set in two API calls: at the training stage, and at the prediction stage. When TTE is enabled, the prediction response includes an `explanation` object.

The following code snippet shows an example of defining a classification solution for training. The parameter test-time-explainability is set to true \(default is false\).

```
var mySolution = new sn_ml.ClassificationSolution({
    'label': 'telecom_customer_churn_with_tte',
    'dataset': myData,
    'predictedFieldName': 'churn',
    'inputFieldNames': [
        'age',
        'contract',
        'monthly_charge',
        'tenure_in_months',
        'online_security',
        'online_backup'
        // ... additional input fields
    ],
    'test-time-explainability': true
});

```

The following code snippet shows an example of requesting explanations at prediction time, after the model has trained successfully. The option test\_time\_explainability is set to true \(default is false\).

```
var input = new GlideRecord('u_telecom_customer_churn_train');
input.get('07601c45ff9232107334ffffffffff38'); // record must not be empty

var options = {};
options.apply_threshold = "false";
options.test_time_explainability = "true";
options.top_n = 100;

var solutionName = sn_ml.ClassificationSolutionStore.get(
    "ml_sn_global_global_telecom_customer_churn_with_tte"
);
var solutionVersion = solutionName.getLatestVersion();
gs.info(solutionVersion.predict(input, options));
```

The following snippet shows an example of the explanation in JSON format \(trimmed for readability\).

```
{
  "07601c45ff9232107334ffffffffff38": [
    {
      "confidence": 99.53,
      "threshold": 1.61,
      "predictedValue": "0",
      "explanation": {
        "prediction": 0.0047,
        "base_value": -0.1806,
        "all_contributors": [
          { "feature": "contract",          "raw_value": "Two Year", "encoded_value": 2.0,  "shap_value": -3.4014 },
          { "feature": "monthly_charge",     "raw_value": "58.55",    "encoded_value": 0.212, "shap_value": -0.6699 },
          { "feature": "tenure_in_months",   "raw_value": "29",       "encoded_value": 28.0,  "shap_value": -0.5553 },
          { "feature": "age",                "raw_value": "68",       "encoded_value": 49.0,  "shap_value":  0.3234 }
        ]
      }
    }
  ]
}
```

Following are the definitions of the fields in `explanation`.

<table id="table_aqk_dpl_jkc"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

prediction

</td><td>

The model's output for this record after all feature contributions are applied.

</td></tr><tr><td>

base\_value

</td><td>

The model's expected result before any feature contributions.

</td></tr><tr><td>

all\_contributors

</td><td>

The full list of input features and their contribution to this prediction.-   feature: The name of the input field.
-   raw\_value: The original value from the record \(for example, "Two Year" or "58.55"\).
-   encoded\_value: The internal numeric representation of the original value used by the model.
-   shap\_value: The contribution score. A positive value pushes the prediction higher; a negative value pushes it lower. The larger the magnitude, the stronger the influence.

</td></tr></tbody>
</table>The contributors are ordered by influence, so the features at the top of `all_contributors` are the strongest drivers of the prediction. Starting from the `base_value`, each `shap_value` influences the result up \(positive value\) or down \(negative value\).

**Related topics**  


[Configure XGBoost for classification or regression solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/predictive-intelligence/configure-xgboost-classification-regression-solutions.md)

[ClassificationSolution - Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/ClassificationSolutionAPI.md)

