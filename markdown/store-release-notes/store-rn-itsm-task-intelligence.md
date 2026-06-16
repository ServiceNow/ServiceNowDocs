---
title: Task Intelligence for ITSM release notes
description: Version history for the Task Intelligence for ITSM application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itsm-task-intelligence.html
release: store
topic_type: reference
last_updated: "2025-12-04"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - IT Service Management release notes, ServiceNow Store release notes]
---

# Task Intelligence for ITSM release notes

Version history for the Task Intelligence for ITSM application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 8.2.1 - December 2025**

    New: Added scoped role sn\_itsm\_ml\_task.ti\_user that grants view-only access to the ITSM Task Intelligence Monitoring Dashboard.

-   **Version 8.1.0 - September 2025**

    Changed: Ensured that predicted similarity count in the Task Intelligence admin page is correctly displayed for authorized roles.

-   **Version 8.0.0 - May 2025**

    New Ships a new model out of the box to recommend a major incident using Task Intelligence.

-   **Version 7.0.0 - November 2024**
    -   New:
        -   Updated the existing Task Intelligence template to be generic to surface similar problems and similar change requests along with similar incidents
        -   Introduces new page "Define the purpose" to select the prediction and training tables for similarity models
        -   Ships a new model out of the box to suggest similar open problems for incident
        -   Ships a new model out of the box to suggest similar open change requests for incident
        -   Support for defining conditions on training table for similarity models
-   **Version 6.0.1 - August 2024**
    -   New:
        -   Ships a new Task Intelligence template to surface similar incidents
        -   Ships a new model out of the box to suggest similar incidents
    -   Changed: Renamed OOB incident categorization model to "Incident Categorization"
-   **Version 1.2.0 - February 2024**
    -   New:
        -   Technical support to return top "n" recommendations.
            -   "n" is being set in Recommended Actions application
    -   Minor issue fixes
-   **Version 1.1.0 - November 2023**

    Changed: The options for setting your preferences for each incident field are relocated to the Assess your model section.

-   **Version 1.0.0 - August 2023**
    -   Predict and recommend the incident field information to help with incident categorization and reduce the handle time for agents and increase productivity;
    -   Define the purpose, set the prediction preferences and behaviour, train with your data, and deploy the solution model for predicting and recommending incident fields
    -   Track and monitor the performance of the deployed model.
    -   Edit the deployed model based on the performance results, train and deploy the model again.

