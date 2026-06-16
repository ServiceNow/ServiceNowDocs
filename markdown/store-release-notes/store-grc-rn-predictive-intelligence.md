---
title: GRC: Predictive Intelligence release notes
description: Version history for the GRC: Predictive Intelligence application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-predictive-intelligence.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Predictive Intelligence release notes

Version history for the GRC: Predictive Intelligence application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.1 - June 2026 \(Australia\)**
    -   Changed:
        -   Enhancements to GRC predictive intelligenceGRC predictive intelligence has been updated with changes to access controls, data coverage, and model definitions to support improved prediction accuracy and platform compatibility.
        -   Refined read access for predictive modelsRead access permissions for predictive machine learning on GRC Issue and Task records have been updated to align with the required data scope. These changes support more consistent assignee recommendations and similarity results.No administrator action is required during upgrade. If your instance includes custom solutions, verify data access after upgrade.
        -   Expanded platform ML read accessThe platform ML reader role now includes read access to Risk Advanced Event records. This change allows predictive models to use additional risk event data.If your instance uses restrictive data policies, review this access after upgrade.
        -   Updates to similarity model and utility libraryThe risk similarity model definition has been updated, which may affect existing similarity results.The predictive intelligence utility library has also been updated to align with current platform ML APIs. No administrator action is required.
-   **Version 21.1.0 - December 2025 \(Zurich\)**

    Fixed: A defect related to role security has been fixed.

-   **Version 21.0.1 - August 2025**

    Fixed: Fixed issue with Remediation tasks recommendation due to invalid input sys\_id: PRB1884240.

-   **Version 20.1.0 - May 2025**

    Changed: Added upgrade impact changes related to the Impacted areas feature on regulatory alerts.

-   **Version 20.0.1 - February 2025**
    -   Fixed:
        -   Security bug.
        -   ACL bypass issues.
-   **Version 19.1.1 - November 2024**
    -   Changed:
        -   Security: Disabled sandbox access for Client-Callable Script Includes
        -   Added the "platform\_ml\_read" role under read access to all related columns and records of GRC tables that are part of Predictive Intelligence solution definition.
-   **Version 19.0.1 - August 2024**
    -   Fixed:
        -   Recommendations for 'Remediation tasks' were not visible to all issue personas.
        -   Recommendations for 'Assign to' were not visible to all users.
-   **Version 18.1.0 - June 2024**

    Changed: Standard record page improvements.

-   **Version 18.0.1 - February 2024**
    -   New: Addressed UX observations in remediation tasks
    -   Fixed: CSM/FSM Configurable workspace case details sidebar tab buttons not working
-   **Version 17.0.0 - August 2023**
    -   Fixed:
        -   Security issue with sub flow.
        -   Handle error message display for all 3 use cases when the solution definition is not trained.
        -   BU lite persona was not able to view ML related functionality.
-   **Version 16.0.1 - July 2023**

    Fixed: Addressed an issue where the Runtime access tracking field's value was inadvertently changing from "None" to "Enforcing" during the Utah upgrade.

-   **Version 16.0.0 - February 2023**

    New: Predict the risk statement for risks using platform ML capabilities.

-   **Version 15.0.1 - August 2022**

    New: Similar risk event suggestion

-   **Version 12.0.0 - March 2021**

    Fixed: Issue owner should be able to create remediation tasks and security issues.

-   **Version 11.0.2 - October 2020**
    -   New:
        -   Suggestions for similar issues and enable grouping of similar issues.
        -   Suggestions to remediate issues based on the history of similar remediation tasks.
-   **Version 10.1.2 - June 2020**
    -   New:
        -   Improved intelligent issue categorization, prioritization, and assignment of issues.
        -   Improved remediation task recommendation for issues.
        -   Improved indicator prediction to analyze the future values and breaches, and also understand how different KRIs and KCIs are correlated.

