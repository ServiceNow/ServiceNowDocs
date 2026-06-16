---
title: Task Intelligence for Customer Service release notes
description: Version history for the Task Intelligence for Customer Service application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-task-intel.html
release: store
topic_type: reference
last_updated: "2025-12-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Customer Service Management release notes, ServiceNow Store release notes]
---

# Task Intelligence for Customer Service release notes

Version history for the Task Intelligence for Customer Service application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 25.4.0 - December 2025**

    Changed: Support for granular roles in Task Intelligence for Customer Service.

-   **Version 25.3.0 - August 2025**

    New: Suggested Open Incidents for a given case.

-   **Version 25.2.1 - November 2024**
    -   New:
        -   Improve the model performance by identifying the dependent fields in a model before displaying the predicted values.
        -   Predict configured interaction record fields when the user tabs out from fields such as short description and description.
        -   Receive recommendations for similar open and closed cases that are automatically trained and deployed.
        -   Install the major issue management plugin and activate major issues to get major case recommendations.
-   **Version 25.1.2 - August 2024**

    New: Predict configured case record fields when the user tabs out from fields such as short description and description.

-   **Version 25.0.0 - May 2024**
    -   Changed:
        -   Task Intelligence admin console enhancements to display correct, incorrect, and skipped predictions by model and field, and compare models over a specified date range
        -   Filter out predicted values that are no longer active
        -   Introduced a new Now Assist system user for AI applications that captures AI changes in activity stream
        -   Added an "Updating" state in the banner to let users know that AI predictions are currently being processed
-   **Version 24.1.1 - February 2024**
    -   Document classifier: Increase efficiency and automation by using the document classifier feature to categorize incoming documents.
    -   Model performance on top 3 recommendations: View the prediction performance during model training for both auto fill and recommend models and use data to determine your preference for either autofill or recommendation as the prediction method.
    -   Monitoring model performance at field level: View the model performance by field on the Task Intelligence Admin Console dashboard.
    -   Filter out predictions that are no longer active choices.
    -   If upgrading from a prior release version to Vancouver, refer to the configuration documentation \(https://docs.servicenow.com/bundle/vancouver-customer-service-management/page/product/customer-service-management/concept/configure-task-intelligence.html\).

-   **Version 23.3.1 - September 2023**
    -   New
        -   Task Intelligence generalization: support for email to interaction and interaction to case
        -   Interaction record categorization at chat wrap up
        -   Top 3 recommendations display in CSM Configurable Workspace
-   **Version 23.1.1 - February 2023**

    New: New user experience for Document Intelligence configuration, training and deployment

-   **Version 22.2.6 - December 2022**

    Removed hard dependency between Task Intelligence and Document Intelligence.

-   **Version 22.2.4 - November 2022**
    -   New
        -   Added the language detection use case template on the Task Intelligence Admin Console
        -   DocIntel v2
-   **Version 22.1.21 - August 2022**

    Task Intelligence for Customer Service offers several AI capabilities such as language detection, multi-lingual email and case categorization, case sentiment analysis and document intelligence. These capabilities automate several routine tasks across the case lifecycle while enabling agents to focus on complex case resolution.


**Parent Topic:**[ServiceNow Store - Customer Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-csm.md)

