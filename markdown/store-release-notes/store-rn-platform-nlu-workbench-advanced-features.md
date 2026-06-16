---
title: NLU Workbench - Advanced Features release notes
description: Version history for the NLU Workbench - Advanced Features application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-platform-nlu-workbench-advanced-features.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Platform Analytics release notes, ServiceNow Store release notes]
---

# NLU Workbench - Advanced Features release notes

Version history for the NLU Workbench - Advanced Features application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 7.0.25 - March 2026**

    Fixed bugs.

-   **Version 7.0.22 - July 2025**

    Fixed security bugs.

-   **Version 7.0.20 - June 2025**

    Cosmetic bug fixes.

-   **Version 7.0.18 - December 2024**
    -   Fixes related to batch testing and EFL
    -   Fixes for security bugs
-   **Version 7.0.10 - May 2024**

    Security fixes.

-   **Version 6.2.4 - October 2023**

    Fixed: PRB1692353 - This version includes a critical fix \(the Publish button was not selectable for a retrained model\).

-   **Version 7.0.6 - September 2023**

    This patch release contains a fix for the blank page error on the Batch Testing Results Screen.

-   **Version 7.0.5 - August 2023**

    New: An NLU Home Page with models for different applications organized in tabs. An Irrelevance Detection Page to manage utterances that are not relevant to NLU models. A new Expert Feedback Loop page to tune the ITSM Issue Auto Resolution model.

-   **Version 6.2.2 - May 2023**

    Fixed: Internal fixes, no changes to customer facing features

-   **Version 6.0.2 - February 2023**
    -   New: every NLU model is now associated to a default test set, which can be maintained and updated over time to test the model's performance.
    -   Changed: in Expert feedback loop, the feedback provided is directly added to the model and its default test set, to update the model's training and test data.
    -   Removed: removed the Optimize process, and embedded the improvements of optimize directly into the Train button.
-   **Version 5.1.3 - November 2022**

    Changed: Intent Discovery is no longer required to install the NLU Workbench - Advanced Features app.

-   **Version 5.1.0 - September 2022**

    Removed dependency on Intent Discovery application, and added NLU Advanced Features sub-group in left Navigator

-   **Version 5.0.3 - August 2022**
    -   New:
        -   A card based view of providing feedback for utterances is added to Expert Feedback Loop
        -   System properties used in expert feedback loop are now exposed under settings
    -   Changed:
        -   Improved NLU performance dashboard to display prediction results based on user confirmation in Virtual Agent conversations
        -   Improved warnings and guidance around testing multiple models in batch testing
        -   Utterances that dont belong to a model are now skipped from batch testing to provide more accurate results
        -   Feature name changes
-   **Version 4.0.5 - February 2022**
    -   New: Expert Feedback Loop: Use this feature to provide feedback on the predictions of utterances in your VA logs. Once you provide enough feedback, you can improve the test set and optimize your model to improve its prediction capabilities
    -   Fixed:
        -   Editing or deleting an utterance from the conflict review fails
        -   Conflicts are shown only against one intent even though multiple intent are conflicting
-   **Version 3.1.2 - November 2021**

    Changed: Test set quality verification for intent coverage now available at test set selection. Decide the test set to run batch testing or optimization without having to wait until the test is run.

-   **Version 3.0.4 - August 2021**
    -   New:
        -   Model Optimization Test: Test a single trained model against your utterances before publishing it by leveraging a better pre-trained language model and to reduce incorrect predictions
        -   Batch Testing Insights: See the prediction trends among your utterances. Batch testing results now show:
            -   Top 5 incorrect intents
            -   Top 5 missed intents
        -   Export Test Results: Export the test results as a downloadable CSV file
    -   Changed: "Skipped" is now "Missed"
-   **Version 2.0.5 - May 2021**
    -   New: Model threshold recommendation: Receive recommendations for the threshold precentages of your NLU Models to help improve the intent predictions \(Requires Quebec Patch 2\) Improved test set results: See a breakdown of the correct, incorrect, and missed predictions from your models.
    -   Changed: Test set: You can now view the utterances in your test set and import more utterances. Multiple intents: You can now specify multiple intents for a single utterance.
    -   Fixed: Scroll issue on the results page. Inconsistency between percentages on the results and details pages.
    -   Removed: The fields "Confidence Threshold", "Predicted Intent" and "Prediction Model" on table \[nlu\_batch\_test\_result\] were populated in previous versions of the application "NLU Workbench - Advanced Features", but with version 2.0.5, these fields have been deprecated and are no longer populated with any data.
-   **Version 1.0.12 - February 2021**

    New: Delivers advanced features for NLU Model management such as NLU Intent Conflict Review, Batch Testing for NLU, and NLU Model Performance. This application is dependent on the NLU Workbench - Advanced Features plugin and NLU Workbench plugin.


**Parent Topic:**[ServiceNow Store - Platform Analytics release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-air.md)

