---
title: Task Intelligence Admin Console release notes
description: Version history for the Task Intelligence Admin Console application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-nowintel-task-intelligence-admin-console.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Platform Analytics release notes, ServiceNow Store release notes]
---

# Task Intelligence Admin Console release notes

Version history for the Task Intelligence Admin Console application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 5.3.0 - March 2026**
    -   New: Added contextual UI information notes on the Task Intelligence Monitoring page.
    -   Fixed:
        -   Fixed  issue in the auto-deploy feature where newly trained model is automatically deployed when it outperforms the currently deployed model.
        -   Fixed Task Intelligence training page to display correct data for the “Currently Deployed”.
        -   Updated the filter on the Task Intelligence Monitoring page to ensure results are limited to a 90-day data window.
        -   Adopted enhanced platform security feature to export Task Intelligence Models.
-   **Version 5.2.1 - December 2025**
    -   New: Added validation to prevent categorization model training when no prediction records are available.
    -   Changed: Modified the "tia\_user" role from accessing admin pages such as model setup, History, and System Properties under TI.
    -   Fixed:
        -   Fixed an issue where the Condition Builder component did not display true/false values in read-only mode and corrected field and toggle styling during ITSM model setup.
        -   Fixed errors in language and sentiment models when no records were found.
        -   Fixed issue where MTTR was not visible on page reload in the Monitoring page.
        -   Fixed the UI filter condition in model setup.
    -   Removed:
        -   Enhanced security by removing "admin" roles in ACLs.
        -   Removed the "view training results" link from the monitoring page for users with the "tia\_user" role.
-   **Version 5.1.0 - September 2025**
    -   Fixed:
        -   Improved security by updating GlideQuery to GlideQuerySecure.
        -   Fixed an issue on the "Train Your Model" page to accurately display the total number of record.
        -   Fixed query condition on the Monitoring page to ensure correct data filtering and display.
-   **Version 5.0.7 - August 2025**
    -   Fixed:
        -   Fixed errors and parsing issue during setup.
        -   Fixed query condition in the Analytics Dashboard.
        -   Fixed help link on the Setup page.
        -   Fixed the issue reported when querying a non-existent ML object.
-   **Version 5.0.6 - June 2025**

    Minor bug fix.

-   **Version 5.0.5 - April 2025**

    Fixed: Fixed the filter conditions in model config.

-   **Version 5.0.4 - December 2024**
    -   Fixed:
        -   Fixed error when the training data exceeds 100K for Similarity model
        -   Fixed label display to show the appropriate metric label in the monitoring page
        -   Fixed error that occurred while disabling the auto-training
        -   Fixed a display issue in the help content when viewed on Safari browser
        -   Fixed the input/output filter for Similarity model
-   **Version 5.0.1 - November 2024**
    -   New:
        -   Added the ability to configure auto-training for the chosen frequency for the categorization and similarity model
        -   Added the ability to configure auto-deploy for categorization
        -   Added below features to TIAC Similarity model support
            -   Added: Define the purpose page
            -   Added support to configure columns to show on "Sample results" page
            -   Added new condition filter for training inputs
-   **Version 4.3.3 - August 2024**
    -   Added support for Similarity model: In this release we have added support for the PI similarity model directly from the TI Admin Console. This enables execution of Similarity model based tasks while remaining in the Task Intelligence environment. There are several constraints in this release which will be addressed in future release.
    -   1.  There is no provision in this release for estimating the accuracy of the model prior to deployment. Suggestion is to first deploy in a sub pod environment and then perform testing based on results. When satisfied, transition to production environments.
2.  There is are no application level metrics available for Similarity in the dashboard. Some model level execution metrics are provided. To determine how well the model is working for an instance, suggestion is to collect results after using the model and assembling a spreadsheet to help determine results.
3.  There is no facility to tune the model. Sometimes models offer the ability to label data which is used to help tune the model. This is not supported in this release.
-   **Version 4.2.3 - May 2024**
    -   Fixed accessibility defects
    -   Enhanced monitoring dashboard
-   **Version 4.1.0 - February 2024**

    Fixed issues.

-   **Version 4.0.3 - January 2024**

    Security fix.

-   **Version 4.0.2 - November 2023**
    -   Improvements to reporting:
        -   Administrators can now view the % Correct per field on the Monitoring page, rather than combined across all fields in the model.
        -   The "Assess your model" screen shows "Top 3" % Correct or "Top 1" % Correct depending on the model setting selected by the administrator.
-   **Version 3.0.5 - August 2023**
    -   New:
        -   Define your purpose page: With the Define your purpose page, you can control table configurations and setup for your field value prediction models.
        -   Warning if creating a model that predicts the same fields as an existing model: When creating or editing a model, a warning is shown when categorization models predict the same fields as another model. Two models predicting the same field could overwrite each other.
        -   Optional attachments: You can add information gathered from email and chat attachments to train your model.
    -   Changed:
        -   Customer Service Management language removed: Verbiage for help and on-screen text no longer refers only to Cases as support for IT Service Management increases.
        -   Template form updates: Templates no longer refer only to Cases as support for IT Service Management increases.
-   **Version 2.2.1 - May 2023**

    Changed: Changes to support model improvements in Utah and future features.

-   **Version 2.1.2 - February 2023**
    -   New:
        -   Warnings when selecting fields to be predicted by the auto-categorization solution if those fields are also covered by another trained model \(in Task Intelligence, Predictive Intelligence or Predictive Intelligence Workbench\). Links are provided to check the configuration of the other models to confirm if there are conflicting prediction conditions \(such as predicting product field only if priority is not 1\).
        -   Direct link to help navigate to Document Intelligence
    -   Fixed: Improved the handling of record count on large datasets for model training
-   **Version 2.0.3 - November 2022**
    -   New
        -   Language Detection setup flow and monitoring
        -   Support for Dark Theme
    -   Changed: Improved data-driven templates for UI build flexibility
-   **Version 1.0.3 - August 2022**

    The Task Intelligence Admin Console allows you to easily setup and configure ML solutions to automate task workflows. By following guided setups for specific business outcome objectives, you will quickly be able to track how ML solutions are impacting creation, deflection, triage, remediation and optimization moments to lower the mean-time to resolve \(MTTR\) of tasks.


**Parent Topic:**[ServiceNow Store - Platform Analytics release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-air.md)

