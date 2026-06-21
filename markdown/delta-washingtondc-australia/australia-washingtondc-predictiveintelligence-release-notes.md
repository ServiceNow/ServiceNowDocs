---
title: Combined Predictive Intelligence release notes for upgrades from Washington DC to Australia
description: Consolidated page of all release notes for Predictive Intelligence from Washington DC to Australia. Predictive Intelligence was previously called Agent Intelligence.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-washingtondc-australia/australia-washingtondc-predictiveintelligence-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Predictive Intelligence release notes for upgrades from Washington DC to Australia

Consolidated page of all release notes for Predictive Intelligence from Washington DC to Australia. Predictive Intelligence was previously called Agent Intelligence.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Predictive Intelligence release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Predictive Intelligence to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

If you’re upgrading to Washington DC, you won't be able to create new regression solutions. If you have existing solutions, they will still be supported and you will be able to train and modify them, but you won't be able to create new ones.

 The changes to the similarity and clustering solutions apply to all instances that are on Washington DC.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Predictive Intelligence.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Model Explainability](https://www.servicenow.com/docs/access?context=predictive-intel-explainability&family=yokohama&ft:locale=en-US)**

Learn which classes contribute most to your model's predictions by optionally adding Model Explainability to Workflow Classification solutions. Model Explainability provides a new tab labeled **Feature Importance** where you can run an analysis of each class's contribution to the overall prediction.

-   **[Leverage new advanced options for classification solutions](https://www.servicenow.com/docs/access?context=configuring-advanced-settings-ml-solutions&family=yokohama&ft:locale=en-US), from Yokohama Patch 4.**
    -   [Configure include only top N labels](https://www.servicenow.com/docs/access?context=predictive-intel-only-top-n-labels&family=yokohama&ft:locale=en-US). Limit the classification model to use only the top most frequent labels. You can choose a number as the limit.
    -   [Minimum records needed for label to include it](https://www.servicenow.com/docs/access?context=predictive-intel-minimum-records-needed-label&family=yokohama&ft:locale=en-US). Set a threshold for the minimum number of records a label must have in your dataset to be included in model training.
    -   [Remove others label](https://www.servicenow.com/docs/access?context=predictive-intel-remove-others-label&family=yokohama&ft:locale=en-US). Reduce noise in the model and enhance predictive accuracy by removing records with the label "others" from training data.
    -   [Use LightGBM algo for classification model training](https://www.servicenow.com/docs/access?context=predictive-intel-lightgbm-algo&family=yokohama&ft:locale=en-US). Enable the LightGBM \(Light Gradient-Boosting Machine\) algorithm for training classification models.
    -   [Config parameters for model config in classification](https://www.servicenow.com/docs/access?context=predictive-intel-config-parameters-classification&family=yokohama&ft:locale=en-US). Customize training behavior by including a dictionary of parameters in the JSON format.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Review any errors in predictions using the Observability Dashboard](https://www.servicenow.com/docs/access?context=prediction-errors-observability-dashboard&family=zurich&ft:locale=en-US)**

Monitor errors using the Observability Dashboard which provides analytics derived from a new table. This table is dedicated to logging any errors that may occur during Predictive Intelligence predictions.

-   **[Leverage new advanced options for classification solutions](https://www.servicenow.com/docs/access?context=configuring-advanced-settings-ml-solutions&family=zurich&ft:locale=en-US)**

Customize your classification models in Predictive Intelligence with the following advanced options.

    -   [Configure include only top N labels](https://www.servicenow.com/docs/access?context=predictive-intel-only-top-n-labels&family=zurich&ft:locale=en-US): Limit the classification model to use only the top most frequent labels. You can choose a number as the limit.
    -   [Minimum records needed for label to include it](https://www.servicenow.com/docs/access?context=predictive-intel-minimum-records-needed-label&family=zurich&ft:locale=en-US): Set a threshold for the minimum number of records a label must have in your dataset to be included in model training.
    -   [Remove others label](https://www.servicenow.com/docs/access?context=predictive-intel-remove-others-label&family=zurich&ft:locale=en-US): Reduce noise in the model and enhance predictive accuracy by removing records with the label "others" from training data.
    -   [Use LightGBM algo for classification model training](https://www.servicenow.com/docs/access?context=predictive-intel-lightgbm-algo&family=zurich&ft:locale=en-US): Enable the LightGBM \(Light Gradient-Boosting Machine\) algorithm for training classification models.
    -   [Config parameters for model config in classification](https://www.servicenow.com/docs/access?context=predictive-intel-config-parameters-classification&family=zurich&ft:locale=en-US): Customize training behavior by including a dictionary of parameters in the JSON format.

</td></tr><tr><td>

Australia

</td><td>

-   **[Predictive Intelligence Usage Analytics dashboard](https://www.servicenow.com/docs/access?context=predictive-intel-usage-analytics&family=australia&ft:locale=en-US)**

Usage Analytics dashboard is a central location to understand the adoption, effectiveness, and overall value of all your Predictive Intelligence solutions. Dashboard widgets offer several metrics such as total monthly count of predictions per solution type.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Predictive Intelligence features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **Pre-trained models for [similarity](https://www.servicenow.com/docs/access?context=create-similarity-solution&family=washingtondc&ft:locale=en-US) and [clustering](https://www.servicenow.com/docs/access?context=create-clustering-solution&family=washingtondc&ft:locale=en-US) solutions**

With the new pre-trained models, you won't need your own word corpus when creating new solutions.

**Important:** With the Washington DC release, clustering and similarity models use Workflow solutions. When existing solutions with a word corpus are retrained after upgrading, they become Workflow solutions, and the **Word Corpus** field is no longer visible on the form.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[Leverage new advanced options for classification solutions](https://www.servicenow.com/docs/access?context=configuring-advanced-settings-ml-solutions&family=xanadu&ft:locale=en-US), from Xanadu Patch 9.**

Five new advanced options are available for classification solutions, including new parameters and a new algorithm.

    -   [Configure include only top N labels](https://www.servicenow.com/docs/access?context=predictive-intel-only-top-n-labels&family=xanadu&ft:locale=en-US). Limit the classification model to use only the top most frequent labels. You can choose a number as the limit.
    -   [Minimum records needed for label to include it](https://www.servicenow.com/docs/access?context=predictive-intel-minimum-records-needed-label&family=xanadu&ft:locale=en-US). Set a threshold for the minimum number of records a label must have in your dataset to be included in model training.
    -   [Remove others label](https://www.servicenow.com/docs/access?context=predictive-intel-remove-others-label&family=xanadu&ft:locale=en-US). Reduce noise in the model and enhance predictive accuracy by removing records with the label "others" from training data.
    -   [Use LightGBM algo for classification model training](https://www.servicenow.com/docs/access?context=predictive-intel-lightgbm-algo&family=xanadu&ft:locale=en-US). Enable the LightGBM \(Light Gradient-Boosting Machine\) algorithm for training classification models.
    -   [Config parameters for model config in classification](https://www.servicenow.com/docs/access?context=predictive-intel-config-parameters-classification&family=xanadu&ft:locale=en-US). Customize training behavior by including a dictionary of parameters in the JSON format.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Validation logic ensures that Predictive Intelligence can access data tables**

Reduce errors while training Predictive Intelligence models with the help of new validation logic. This validation checks whether your data tables have ACLs \(Access Control Lists\) granting access to Predictive Intelligence.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Predictive Intelligence features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Predictive Intelligence features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Support for creating new regression solutions was removed. You will still be able to train and edit existing solutions, but you won't be able to create new ones.

</td></tr><tr><td>

Xanadu

</td><td>

The dashboard for Solution Statistics has been deprecated. Upgrading customers can continue to use their existing Solutions Statistics dashboards from the application menu. For new customers onboarding with the Xanadu release, the Solutions Statistics dashboard is not available. For more information, see [Review classification solution statistics](https://www.servicenow.com/docs/access?context=review-solution-statistics&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

With the Yokohama release, ITSM Predictive Intelligence Workbench is deprecated and no longer supported. To obtain the latest experience for this functionality, install the Task Intelligence for ITSM application \(com.snc.itsm\_ml\_task\). For more information, see [ITSM Predictive Intelligence Workbench release notes](https://www.servicenow.com/docs/access?context=itsm-predictive-intelligence-workbench-rn&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Predictive Intelligence.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

Predictive Intelligence is a ServiceNow AI Platform feature that is available with activation of the Predictive Intelligence Reports \(com.glide.platform\_ml\_pa\) plugin and its dependent Predictive Intelligence \(com.glide.platform\_ml\) plugin. For details, see [Install Predictive Intelligence](https://www.servicenow.com/docs/access?context=install-predictive-intelligence&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Predictive Intelligence is a ServiceNow AI Platform feature that is available with activation of the Predictive Intelligence plugin \(com.glide.platform\_ml\). For details, see [Install Predictive Intelligence](https://www.servicenow.com/docs/access?context=install-predictive-intelligence&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Predictive Intelligence is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Australia

</td><td>

Predictive Intelligence is a ServiceNow AI Platform feature that is active by default.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Predictive Intelligence we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Predictive Intelligence we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Predictive Intelligence, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   ****

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Predictive Intelligence we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Predictive Intelligence we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Use pre-trained models for clustering and similarity solutions to make creating solutions more efficient without needing your own word corpus.
-   You can edit and train existing regression solutions, but starting with Washington DC you won't be able to create new regression solutions.

 See [Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence-landing&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

-   The dashboard for Prediction Results has been migrated to the Next Experience UI. Upgrading customers with existing Prediction Results dashboards can use either the Next Experience UI version or access the Core UI version from within the new dashboard.
-   The dashboard for Solution Statistics has been deprecated. Upgrading customers can continue to use their existing Solutions Statistics dashboards from the application menu.
-   New advanced options for classification solutions are available from Xanadu Patch 9.

 See [Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence-landing&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Learn which classes contribute the most to your model's predictions by adding Model Explainability to Workflow Classification solutions.
-   ITSM Predictive Intelligence Workbench is deprecated in the Yokohama release.
-   New advanced options for classification solutions are available from Yokohama Patch 4.

 See [Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence-landing&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Predictive Intelligence errors are logged in a new, dedicated table. The PI - Observability Dashboard leverages this table to provide analytics on prediction errors.
-   New advanced options for Classification models are available, including new parameters and a new algorithm.
-   Validation logic ensures that Predictive Intelligence models have ACLs to access data tables.

 See [Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence-landing&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

A new Predictive Intelligence Usage Analytics dashboard provides you with actionable insights into model performance, user engagement, adoption trends, and product health.

 See [Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence-landing&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-washingtondc-australia/rn-combined-intro.md)

