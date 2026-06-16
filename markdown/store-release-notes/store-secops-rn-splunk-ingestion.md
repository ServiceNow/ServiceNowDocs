---
title: Splunk Enterprise Event Ingestion for Security Operations release notes
description: Version history for the Splunk Enterprise Event Ingestion for Security Operations application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-splunk-ingestion.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Splunk Enterprise Event Ingestion for Security Operations release notes

Version history for the Splunk Enterprise Event Ingestion for Security Operations application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 11.6.4 - June 2026**

    Fixed: Data ingestion issue caused by Splunk indexing delay.

-   **Version 11.6.3 - May 2026**
    -   Fixed:
        -   Cobalt Raven Non-Glide Query ACLs Directive: Resolved issues related to ACL directives for non-Glide queries in Cobalt Raven.
        -   SIR Creation Failure from SIEM Ingestion: Security Incident Response \(SIR\) records were not created due to restricted access to Secure Notes in the Crypto module after the Yokohama upgrade. This occurred when the System Access Module Access policy was not configured.
        -   Sandbox Compatibility with KittyJS: Addressed sandbox-related issues to ensure compatibility with KittyJS.
        -   Multi-Value Field Parsing Issue: Multi-value fields were not split correctly due to a mismatch in delimiters used for combining and splitting values. Values are now parsed and separated as expected.
-   **Version 11.6.2 - March 2026**

    New: Incorporated strategies to present data without relying on CMDB or identity tables in the integration.

-   **Version 11.5.1 - December 2025**

    New: Upgraded all dictionary-level read-only fields to Strict Read-Only to enhance security and prevent unauthorized changes.This update ensures the server consistently enforces read-only behaviour across all UIs, scripts, and integrations.

-   **Version 11.4.1 - August 2025**
    -   New: Enabling users with "sn\_si.ingestion\_profile\_admin" role to manage ingestion profiles on Splunk V2 Integration
    -   Fixed: Handled node restart scenario for splunk v2.
-   **Version 11.3.4 - June 2025**
    -   Fixed:
        -   When multiple values are going in the affected users or configurations items from splunk, an error alert message pop up with the message: input value was not found for mapped field.
        -   Affected user getting mapped to empty user record if no value corresponding to it in Splunk v2.
-   **Version 11.3.3 - April 2025**

    Fixed: Issue related to the configuration item mapping.

-   **Version 11.3.1 - November 2024**
    -   Changed: Changed the Search API to v2 version.
    -   Fixed:
        -   An intermittent 404 error during ingestion is happened.
        -   Null pointer check was missing for the alert list associated with Splunk Event profiles, which caused a NPE in case the alert list is empty.
-   **Version 11.2.12 - April 2024**

    Fixed: Performance issues while creating SIRs, when large volume of Splunk events are ingested.

-   **Version 11.2.9 - February 2024**

    Fixed: Splunk Integration payload variables are now processed correctly.

-   **Version 11.2.6 - November 2023**

    Changed: Minor improvements to our backend libraries.

-   **Version 12.0.8 - August 2023**
    -   Changed: You can now map Notable Event fields to specific observable types.
    -   Fixed:
        -   Notables are not pulled if the MID server is down in Splunk ES integration.
        -   Splunk ES integration for the SIR module stopped ingesting notables due to large payload events exceeding the string size limit of 32 MB.
        -   Updates to the SIR after the creation are disregarded when the Integration Transform script takes a long time.
-   **Version 12.0.7 - July 2023**

    Fixed: Errors in the 'Preview' section while creating an event profile.

-   **Version 11.2.4 - May 2023**
    -   Fixed:
        -   One-Time Retrieval was not working on the scheduling page of the profile when we change the date format to dd-MM-YYYY for Splunk V2.
        -   Splunk Event Profiles: Lengthy field labels are split to the following line at 200% browser zoom.
-   **Version 11.2.3 - January 2023**

    Minor fixes related to errors during Splunk v2 event profile creation.

-   **Version 11.2.2 - September 2022**

    Fixed: Localization text fixes.

-   **Version 11.2.0 - May 2022**
    -   New: Enabled token-based authentication.
    -   Fixed:
        -   When you perform an M2M mapping for Observables/CIs in the Profile, a blank SIR gets created \(skipping the SIR sequence\).
        -   Fixed the issue of Aggregation with Reference fields.
-   **Version 11.1.0 - December 2021**
    -   Changed:
        -   Modified the Event Import table default retention to 30 days.
        -   Modified the profile behavior to prevent activating until the profile is complete.
    -   Fixed:
        -   UI fixes to support Next Experience UI.
        -   Fixed an issue where Splunk Alerts for large payloads did not process.
        -   Fixed an issue with an infinite loop caused by \($&amp;\) characters in the Splunk value.
-   **Version 10.6.0 - June 2021**
    -   New:
        -   You can export and import Splunk Enterprise Event Ingestion profiles settings from one ServiceNow AI Platform instance to a different ServiceNow AI Platform instance. The settings you can export and import include profile name, correlation rules, mappings, filters, aggregation criteria, field translations, fetched sample data, scheduling, and configuration tile source information.
        -   A new mapping field Splunk Alert Name is added so that you can trace an event to the source alert rule in Splunk.
        -   Added left navigation menus for Event Import and Event to Task Table Entries.
        -   When a single field contains multiple values, those values are parsed and mapped to individual field entries on the SIR incident form. For example, the source IP addresses, asset names, or URLs may have multiple observable field entries or multiple CIs, those are parsed and mapped to individual field entries on the SIR incident form.
    -   Fixed:
        -   Fetching of sample data breaks when an alert name has a special character like Comma\(,\).
        -   The Splunk profile sometimes may not connect when multiple Splunk sources are configured.
-   **Version 10.6.0 - November 2020**
    -   New:
        -   Multiple similar alerts can now be selected in a single profile.
        -   If a Splunk event field is mapped to a multi-value field and the aggregated event field values are different than the initial triggering event. The additional values are added to the SIR incident field. This applies to commonly mapped multi-value fields such as the following:
            -   Observables
            -   Configuration Items
            -   Affected Users
    -   Fixed: Minor bug fixes.
-   **Version 10.5.1 - August 2020**
    -   New:
        -   Implemented support for Splunk Accelerated Datamodel functionality when ingesting alerts in Splunk Enterprise Integration.
        -   User can create profiles by selecting specific Splunk apps \(along with core 'Search' app\) for ingesting alerts.
    -   Fixed: Renaming an Event Profile removes all the field translations configured in the profile.
-   **Version 10.4.0 - June 2020**

    New: Field translations \(which are used during alert fields mapping\) have been modified to be made profile specific instead of Global.

-   **Version 5.2.1 - February 2020**
    -   New:
        -   Added the ability to map event fields to watch list type fields during mapping phase of integration profile setup
        -   Moved System Properties to Splunk Integration Settings
        -   Two profiles cannot be active with the same alert name
        -   Added the ability to create a second default manual profile if the initial default profile is inactive
        -   Error messages - No sample alerts exist, no fields extracted in triggered alert queries, and invalid date selection for one-time \(historical\) event retrieval
        -   Mapping format to support new lines when multiple event fields are mapped to single incident field
        -   Added the ability to expand mapping fields for input expressions to handle longer strings that wrap text similar to Splunk ES integration
        -   Mapping support to Subcategory field
        -   Extended the size of Name and Alert List Selection column in Splunk Event profile
-   **Version 5.1.1 - December 2019**
    -   Fixed:
        -   Fixed Integration Configuration tile when on-prem is selected
        -   Display aggregated alerts for a security incident to Security Analyst
-   **Version 5.1.0 - September 2019**
    -   New: Observables as aggregation criteria in Splunk event profile
    -   Fixed:
        -   Conversion of Splunk events to incidents with special characters
        -   TimeStamp conversion to match the correct time in Splunk
        -   Pulling all the records from Splunk using pagination
        -   Fixed the filteration logic for creation of security incidents
        -   Information indication when invalid field value is mapped
        -   Fixed the alert selection when Localization is on
-   **Version 5.0.2 - April 2019**
    -   Create multiple alert ingestion profiles to create SIR security incidents for specific types of threats such as phishing and malware
    -   Create multiple event profiles for on-demand event forwarding from your Splunk console to create SIR security incidents
    -   Drag-and-drop mapping of Splunk alert and event field values to associated SIR security incident fields
    -   A preview of the SIR security incident layout based on sample alerts or events to validate profile configuration
    -   Ingest historical alerts as well as ongoing, future alerts on configurable intervals
    -   Aggregate events or alerts to existing SIR security incidents based on matching field values to avoid duplicate security incidents

