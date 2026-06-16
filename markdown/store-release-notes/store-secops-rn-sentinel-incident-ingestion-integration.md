---
title: Microsoft Azure Sentinel - Incident Ingestion Integration for Security Operations release notes
description: Version history for the Microsoft Azure Sentinel - Incident Ingestion Integration for Security Operations on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-sentinel-incident-ingestion-integration.html
release: store
topic_type: reference
last_updated: "2026-05-05"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Microsoft Azure Sentinel - Incident Ingestion Integration for Security Operations release notes

Version history for the Microsoft Azure Sentinel - Incident Ingestion Integration for Security Operations on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 11.2.3 - May 2026**

    Fixed: Access issues for Security Analyst on querying tables.

-   **Version 11.2.2 - April 2026**
    -   Fixed:
        -   Fixed SIR creation issue from SIEM ingestion caused by missing Crypto module access for Secure Notes post Yokohama upgrade \(Module Access policy\).
        -   Fixed subcategory mapping failure when value contains comma \(,\).
-   **Version 11.2.1 - March 2026**

    Fixed: Observable ingestion to validate successful insert before creating M2M task-observable relationships, preventing orphaned records when observable creation fails silently.

-   **Version 11.2.0 - December 2025**

    New: Upgraded all dictionary-level read-only fields to Strict Read-Only to improve security and prevent unauthorized changes.This update ensures the server consistently enforces read-only behaviour across all UIs, scripts, and integrations.

-   **Version 11.1.0 - August 2025**
    -   New: Enabling users with "sn\_si.ingestion\_profile\_admin" role to manage ingestion profiles on Azure Integration.
    -   Fixed:
        -   Category field in Azure Sentinel import not populating as per field translation mapping in sn\_si\_incident table. Allowing the user to create multiple field translations for an attribute.
        -   If filter condition on coulmn 'properties\(labels\(labelName\)\)' in the 'Azure Sentinel Incident Import' table requires more than 40 characters data to be matched, condition will be failed and no SIR will get created.
        -   Issue with Delimiter given for multiple values in mapping page.
        -   Field translation not working in Azure Sentinel mapping.
-   **Version 11.0.26 - July 2025**
    -   Changed: Introduced support for polling closed incidents during ongoing ingestion processes. Additionally, a new state field has been added to the mapping section.
    -   Fixed:
        -   AzureSentinelCommentStatusSync script include throwing "String object has exceeded maximum permitted size of 33554432" error.
        -   Empty SIR's getting created.
        -   Microsoft Azure Sentinel Incident Ingestion Integration For Security Operations" is not handling an error properly - infinite loop.
-   **Version 11.0.25 - June 2025**
    -   Fixed:
        -   AzureSentinelCommentStatusSync script include throwing "String object has exceeded maximum permitted size of 33554432" error.
        -   Empty SIR's getting created.
-   **Version 11.0.24 - May 2025**
    -   Changed: Introduced support for polling closed incidents during ongoing ingestion processes. Additionally, a new state field has been added to the mapping section.
    -   Fixed: Multiple issues have been addressed and resolved as part of this release.
-   **Version 11.0.22 - February 2025**
    -   Fixed:
        -   Techniques is missing from Azure Sentinel payload
        -   Only supports single alert link in the SIR work notes and getting extra comma on multiple alerts for Azure Sentinel Integration.
-   **Version 11.0.21 - September 2024**
    -   Fixed:
        -   In case of unterminated literal in response from sentinel, alert and entities creation is handled.
        -   Synchronization issue between SIR and Microsoft Sentinel due to 500 internal server error.
-   **Version 11.0.20 - May 2024**
    -   Changed: The new UI dependency is removed.
    -   Fixed: For CMDB CI translation, the option "Cannot convert null to an object" while performing field translation is now fixed.
-   **Version 11.0.17 - February 2024**
    -   New:
        -   Introduced a system property to control the delimiter for mapping by the users.
        -   Introduced a system property which will poll for updates all along and will not depend on overriding flag in the mapping section.
    -   Fixed:
        -   Aggregation for two fields was considering one of the fields and not both,fixed the same.
        -   Integration was not triggering closure updates flow for an incident closed within milliseconds.
-   **Version 11.0.16 - December 2023**

    Fixed: A few validations on the fields for a configuration tile were broken. This is now fixed.

-   **Version 11.0.15 - November 2023**
    -   New:
        -   Supports Overridable fields on the Profile Field Mapping section. When the checkbox for a specific field is selected, any new or updated information from Azure Sentinel incidents will automatically synchronize with the corresponding field in the SIR incident data. The affected users, observables, and CIs are enabled by default in the profile section. Any new observables, CIs, or affected users detected during the polling interval will be appended to corresponding related lists. For all other enabled fields, depending on the mapping, the existing data will be overwritten with the latest data, and changes will be captured as field changes in the worknotes.
        -   You can now automatically process new alerts and entities added to Azure Sentinel incidents \(as long as one of the fields in the Profile Mapping section has the override flag enabled\).
        -   Historical Incident Retrieval: For one-time retrieval of past incidents from Microsoft Azure.
-   **Version 11.0.9 - August 2023**

    Fixed:

    -   Aggregated incidents bidirectional sync should also mention which aggregated incident is getting updated.
    -   Lag in comments sync to ServiceNow or missing Sentinel comments/updates in ServiceNow is addressed.
    -   Automation Activity is posted instead of Worknotes for comment synchronization in the Worknotes section of the SIR form.
    -   Comments and Worknotes synchronization flow getting timed out when a huge number of security incidents are opened or fixed.
    -   Synchronize initial Azure Sentinel Incident comments with SIR Work notes during the incident to task creation.
-   **Version 11.0.8 - February 2023**
    -   Fixed:
        -   Removed the cmdb\_ci field that got updated twice during the transformation.
        -   Availability of all column options in the dropdown of the Filter Condition Builder/
        -   Creation of Azure Sentinel properties \(labels\(labelName\)\) and labelTypes columns out-of-the-box and not dynamically.
-   **Version 11.0.7 - November 2022**
    -   Fixed:
        -   Endpoint, Source, and Base URL are configurable, as the hardcoded ones failed in the GCC environment.
        -   Incident API version is configurable, similar to the Alert API and Entity API versions.
-   **Version 11.0.6 - September 2022**
    -   Fixed:
        -   Improve logging for integration.
        -   Performance fix.
-   **Version 11.0.5 - June 2022**

    Fixed: Inactive close codes are shown in the Additional Options section in close code - classification Reason Mapping.

-   **Version 11.0.4 - March 2022**
    -   Fixed:
        -   Profile goes into an error state because of refusal of connection from Microsoft \(which is intermittent and resolves in successive calls\). It is not considered for ingestion, hence fixed it by polling the error state profiles.
        -   Fixed Sentinel Incident Assignment and Labels, which were reset while updating Sentinel status from ServiceNow.
        -   Fixed the data of all the entities of an incident that is not getting resolved while ingestion or pulling sample data.
        -   Fixed the tabs that were getting disabled while clicking the Save button on the Additional options page.
        -   Usage of undeclared variables in Sentinel integration is removed.
        -   Comments with escape characters / and """" are now supported on Sentinel.
        -   Fixed the Azure Sentinel comments with rich text that were not rendered in SNOW incidents.
        -   Fixed Initial Status Update Subflow is failing due to ACL on sn\_sec\_sentinel\_incident\_to\_task table in domain separation.
-   **Version 11.0.3. - December 2021**

    Fixed: UI changes.

-   **Version 11.0.1 - October 2021**
    -   Fixed:
        -   Added additional password-related policies
        -   Comments synchronization issue is fixed
        -   Mapped work notes added as a new work note for each aggregated incident is fixed
-   **Version 11.0.0 - June 2021**

    New: This integration includes the following key features: Discover Microsoft Azure Sentinel incidents that are candidates for security incidents and automate the creation of security incidents. Mapping of Microsoft Azure Sentinel incident and entity fields to SIR security incident fields. Filtering of Microsoft Azure Sentinel incidents. Aggregation of similar incidents to existing open security incidents so that you don't have to create duplicate security incidents. Automatic Microsoft Azure Sentinel incident status update for SIR security incident creation and closure. Scheduled ingestion of incidents that create security incidents periodically. Synchronization of Microsoft Azure Sentinel incident comments with SIR Work notes.


