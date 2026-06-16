---
title: SuccessFactors spoke release notes
description: Version history for the Integration Hub SuccessFactors spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-successfactors.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# SuccessFactors spoke release notes

Version history for the Integration Hub SuccessFactors spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.11.0 - June 2026**

    Security patch on non-glide ACLs

-   **Version 4.10.1 - May 2026**

    Fixed: Added null-check in script parser to handle Look up Users action more accurately

-   **Version 4.10.0 - April 2026**
    -   Added 8 OData actions to provide function parity with the existing the traditional Employee Central SOAP actions. Customers now have options to use either OData or SOAP for their respective use cases
    -   Rename some old action labels into more descriptive labels
    -   Fixed: Additional encoding applied to resource path in "Look up Candidate by ID" action
-   **Version 4.9.2 - March 2026**
    -   Renamed Skill Profile External ID input label in the Delete Skill Mapping action.
    -   Deprecated existing Create or Update Skill Profile action and added new action for with updated input fields.
    -   Updated Create Skill action input mapping for API fields.
    -   Added outputs fields to map default value in Look up Employee Skills Stream, Look up Rated Skills Mapping, and Look up Skills Stream.
    -   Fixed error thrown when the API returns longDescriptions as an empty array.
-   **Version 4.9.0 - February 2026**
    -   Added/enhanced 8 actions
    -   Added a sample agentic workflow
-   **Version 4.8.0 - December 2025**
    -   Added 10 AI Agents
    -   Security enhancement: Make the sample outbound todo staging table read-only
-   **Version 4.7.0 - October 2025**
    -   Added a new sample subflow to retrieve worker profile information in batches based on the company territory code.
    -   Fixed:
        -   Updated description in XML to include Page Size input for Look up Departments stream action.
        -   Removed unnecessary error log in execution for Create To-do and Update To-do actions.
        -   Issued in payload formation during multiple input fields in Create Record action.
        -   Fixed Employee Time Off Balances Action fetches only the first element in the array.
        -   Used API name to call script-includes in script parse instead of name.
-   **Version 3.7.0 - October 2025**
    -   Added a new sample subflow to retrieve worker profile information in batches based on the company territory code.
    -   Fixed:
        -   Updated description in xml to include Page Size input for Look up Departments stream action.
        -   Removed unnecessary error log in execution for Create Todo and Update Todo actions.
        -   Issued in payload formation during multiple input fields in Create Record action.
        -   Fixed Employee Time Off Balances Action fetches only the first element in the array.
        -   Used API name to call script-includes in script parse instead of name.
-   **Version 4.6.0 - August 2025**
    -   Added: "Parent Department" to Retrieve Department action, and updated its related the sample subflow
    -   Fixed: Pass an additional parameter of 'new\_token=true' while requesting the access token in the OAuth SAML grant flow
-   **Version 4.5.1 - April 2025**

    Fixed:

    -   Execution gets cancelled as subflow is set to run in foreground in Call Run SuccessFactors Service Subflow action.
    -   hasRole implementation from Update Employee Address action.
-   **Version 4.5.0 - March 2025**

    Added 3 actions.

-   **Version 3.5.0 - March 2025**

    Added 3 new spoke actions.

-   **Version 4.4.0 - January 2025**
    -   Added 3 actions
    -   Fixed: Employee Recurring Compensations action with unexpected "No record is found from given input" error.
-   **Version 3.4.0 - January 2025**

    Added 9 new actions.

-   **Version 4.3.0 - November 2024**

    Added/improved 6 actions.

-   **Version 4.2.2 - August 2024**

    Fixed: Retrieve Worker Profiles action's getFirstNode in object when phone information is not available.

-   **Version 3.3.2 - August 2024**

    Fixed: Retrieve Worker Profiles actions's function getFirstNode in object when phone information is not available.

-   **Version 4.2.1 - March 2024**
    -   Fixed ACL to tighten the right user level access to the corresponding actions
    -   Fixed Look up Activity SFTP action's addDays function
-   **Version 3.3.1 - March 2024**
    -   Fixed ACL to tighten the right user level access to the corresponding actions
    -   Fixed Look up Activity SFTP action's addDays function
-   **Version 4.2.0 - February 2024**
    -   New: Added 2 actions.
    -   Fixed: Page Size should be mandatory with a default value for datastream actions.
-   **Version 3.3.0 - February 2024**
    -   New: Added 2 actions.
    -   Fixed: Page Size should be mandatory with a default value for datastream actions.
-   **Version 4.1.1 - December 2023**

    Fixed dynamic subflow of employee recurring compensations.

-   **Version 3.2.1 - December 2023**

    Fixed: Unable to execute dynamic actions using subflow.

-   **Version 4.1.0 - October 2023**
    -   Fixed:
        -   Retrieve Worker Profile does not work for delta.
        -   Addition of try catch block in 'SuccessFactorsScriptParserUtil' script include to handle missing tag for 'assignment\_class'.
-   **Version 3.2.0 - October 2023**
    -   Fixed:
        -   Retrieve Worker Profile does not work for delta
        -   Addition of try catch block in 'SuccessFactorsScriptParserUtil' script include to handle missing tag for 'assignment\_class'
-   **Version 4.0.5 - August 2023**
    -   Fixed:
        -   The wrong value retrieved from primary job and secondary job
        -   The truncated session ID
-   **Version 3.1.7 - August 2023**
    -   Fixed:
        -   The wrong value retrieved from primary job and secondary job
        -   The truncated session ID
-   **Version 4.0.4 - July 2023**

    Fixed the success or failure status of the user activity subflow.

-   **Version 3.1.6 - July 2023**

    Fixed the user activity subflow activity's success or failure status.

-   **Version 4.0.1 - March 2023**
    -   Fixed:
        -   Bug fixes on security and error message handling
        -   Fixing extra white spaces found in Employee Time Off, Get Business Units, and Get Global Information by Entity actions
-   **Version 3.1.3 - March 2023**
    -   Fixed:
        -   Bug fixes on security and error message handling
        -   Fixing extra white spaces found in Employee Time Off, Get Business Units, and Get Global Information by Entity actions
-   **Version 4.0.0 - February 2023**
    -   Changed:
        -   SuccessFactors Spoke to support OAuth SAML grant-type authentication, which will be the defacto auth method starting in Nov 2023 per SuccessFactors announcement
        -   This Spoke DOES NOT support Basic Auth. Users who are looking for Basic Auth SuccessFactors Spoke should download and install 3.x instead
-   **Version 3.1.2 - December 2022**
    -   Patch release ofSuccessFactors Spoke for IntegrationHub. This version includes below fixes:
        -   Pull Todos not populating the urls for few categories
        -   Ended employment not getting pulled in case of multiple employments
        -   Able to create a webhook record with a null name value
        -   Under rehire scenario, the employee gets rehired with the same employee number and header information of the terminated employment
        -   No active identifier for multiple Primary Jobs
        -   Error 'No record found for the given input value' in Get Pick List Options
        -   Fixes to 'Get Entities' because of increased response size
        -   Full load fetching only 500 records
        -   The effective workers service returns data on the past date
-   **Version 3.1.0 - September 2022**
    -   Minor release of SAP Successfactors Spoke for Integration Hub. In this version:
        -   A new action has been added: Retrieve Full Job History Including Secondary Assignments and the existing action Retrieve Job History Including Secondary Assignments is deprecated.
        -   The following existing actions are updated:​
            -   Retrieve Worker Profiles​
            -   Retrieve Effective Worker Profiles​
            -   Retrieve Todos​
            -   Retrieve Locations​
-   **Version 3.0.1 - December 2021**

    Changed: Patch release of SuccessFactors Spoke for IntegrationHub. The version includes security-related changes.

-   **Version 3.0.0 - March 2021**
    -   New:
        -   Added the integration profile for SuccessFactors integration
        -   Below Subflows are developed for this spoke:
            -   SuccessFactors Download Subscriptions: Get all active users from SuccessFactors
            -   SuccessFactors Update User Activity: Update the last activity date of the users in the software subscription table by reading the Login report file attached to the integration profile
            -   SuccessFactors Update User Activity SFTP: Update the last activity date of the users in the software subscription table by importing the activity file from SFTP location
            -   SuccessFactors Reclaim Subscription: Inactivate the user in SuccessFactors by setting status to inactive
-   **Version 2.0.1 - December 2020**

    Patch release of SuccessFactors spoke for IntegrationHub.

-   **Version 2.0.0 - September 2020**
    -   Updated release of the SuccessFactors Spoke for IntegrationHub
    -   More employee lifecycle Actions such as request time off, view time off, view total rewards, report no show, offboard employee, etc.
    -   Sample listener to get SuccessFactors webhook event notification
    -   Remote Tables to view SuccessFactors data on demand
-   **Version 1.0.2 - June 2020**
    -   The SuccessFactors spoke provides a list of actions that wraps around the primary ODATA APIs and SOAP Compound Employee API provided by SuccessFactors. In addition, this spoke provides two sample flows that demonstrate how to perform:
        -   Constant sync departments, locations, job profiles, worker profiles, effective dated worker profiles, job history, secondary job assignment, and to-dos from SuccessFactors to ServiceNow
        -   Bi-directionally create and update to-dos from ServiceNow to SuccessFactors

