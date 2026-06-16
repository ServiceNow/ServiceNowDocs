---
title: Splunk Enterprise Security integration release notes
description: Version history for the Security Operations Splunk Enterprise Security integration on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-splunk-es.html
release: store
topic_type: reference
last_updated: "2024-04-04"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Splunk Enterprise Security integration release notes

Version history for the Security Operations Splunk Enterprise Security integration on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 12.0.12 - April 2024**
    -   Fixed:
        -   Splunk ES Event ingestion scheduled scripts upgrade are made safe.
        -   Splunk ES integration processing issues when large payloads are ingested.
        -   Couple of SplunkES errors with respect to field translations.
-   **Version 12.0.10 - November 2023**
    -   Changed: Minor improvements to our backend libraries.
    -   Fixed: Splunk ES Integration does not pick up notable event updates in Splunk.
-   **Version 12.0.6 - May 2023**

    Fixed:

    -   One-Time Retrieval was not working on the scheduling page of the profile when we change the date format to dd-MM-YYYY for Splunk ES.
    -   Affected User Aggregation is not working in Splunk ES.
    -   ServiceNow Security Operations Event Ingestion Addon for Splunk ES - Events imported are not visible in the 'Splunk ES Event to Tasks' table.
-   **Version 12.0.5 - January 2023**

    Minor fixes related to errors during Splunk ES event profile creation.

-   **Version 12.0.4 - September 2022**
    -   Fixed:
        -   Handled missing Notable events during the Splunk server downtime.
        -   In the Splunk ES Event to Task table, Notable ID is persisted as a separate column since Notable ID data is cleared after one week.
        -   To handle delay in SIR creation, Fetch and Poll scheduled jobs are split into two different jobs.
-   **Version 12.0.2 - June 2022**
    -   New:
        -   Added new system properties for the following:
            -   To expose the delimiter character.
            -   To limit the number of values to parse in each field received from Splunk.
            -   To define the number of overlap minutes to add while retrieving the events from Splunk \(to overcome indexing delay from Splunk\).
            -   Added a hint at the end to determine if the Splunk field values are limited and truncated.
    -   Changed:
        -   Updated AngularJS library version.
        -   Modifying the Splunk ES profile rules doesn't wipe out all the mapping data.
    -   Fixed:
        -   The issue with special characters '$&amp;' combination in the Notable Event field values.
        -   Creating Blank SIR \(skipping SIR sequence\) when M2M mapping is performed for Observable/CIs in Profile.
        -   The Profile pulls events though it gets updated from Scheduled to Manual ingestion type.
-   **Version 12.0.1 - March 2022**
    -   New:
        -   Added new system property for the following:
            -   To expose the delimiter character.
            -   To limit the number of values to parse in each field received from Splunk.
            -   To define the number of overlap minutes to add while retrieving the events from Splunk \(to overcome indexing delay from Splunk\).
    -   Changed: Updated AngularJS library version.
    -   Fixed:
        -   Fixed the issue with special characters '&amp;' combination in the notable event field values.
        -   Creating Blank SIR \(Skipping SIR sequence\) when M2M mapping is done for Observable/CIs in Profile.
        -   The Profile pulls events though it is updated from Scheduled to Manual ingestion type.
-   **Version 12.0.0 - December 2021**
    -   New:
        -   Enabled token based authentication for Splunk ES notable event ingestion.
        -   You can now modify the default notable event reference link URL during Profile creation. This is used in related lists that contains all records for aggregated events.
    -   Changed:
        -   Multiple Splunk ES Correlation Rules can be selected in a single profile.
        -   Ability to map multiple Splunk ES notable event fields to Affected User Fields \(Related List\) on SIR incident.
        -   Ability to map event fields to watch list type fields during mapping phase of integration profile set-up.
        -   Modified the Event Import table default retention to 30 days.
        -   Modified the profile behavior to prevent activating until the profile is complete.
-   **Version 11.0.0 - June 2021**

    New: You can export and import Splunk Enterprise Security profiles settings from one ServiceNow AI Platform instance to a different ServiceNow AI Platform instance. The settings you can export and import include profile name, correlation rules, mappings, filters, aggregation criteria, field translations, fetched sample data, scheduling, and configuration tile source information.

-   **Version 10.5.0 - February 2021**

    New: Introduced capability to support compound logic for aggregation criteria conditions in Splunk ES integration. For example, you can now use multiple matching field values using an 'OR' condition.

-   **Version 10.4.0 - October 2020**
    -   Changed:
        -   When a notable event correlation rule is disabled or inactive in Splunk ES, profile settings \(e.g. sample events, mappings\) are retained. Rule must be de-selected, replaced, and new settings created to erase existing settings.
        -   Suppressed notable events in Splunk ES will always be excluded during ingestion of events without additional filtering required.
        -   Updated the polling mechanism for profiles to create an overlap window between successive polls to ensure no notable events are missed within a specific interval.
        -   When two or more Splunk ES fields are mapped to a single SIR field, e.g. Description, and if one Splunk ES field value is NULL/empty, the SIR field will populate the remaining non-NULL field values.
    -   Fixed:
        -   Notable events will be ingested even if the correlation rule has special characters, such as back slash \(\\\), extra spaces at the end of rule name and other special characters \(~!@\#$%^&amp;\*\(\)\_+\{\}\[\]“:;‘?&gt;&lt;,./\|\\\).
-   **Version 10.0.2 - May 2020**
    -   Changed: 'Source' field name in Manual Event Forwarding type profile is changed to 'Splunk Source Field Value' to distinguish from other Source fields in the profile.
    -   Fixed:
        -   Optimized Splunk ES notable events queries, including clustering multiple profile queries into a single query, to reduce performance overhead on the Splunk ES source server.
        -   Date/Time fields for Splunk ES are stored in UTC format to avoid time zone discrepancies between Spunk source and SeviceNow instance.
        -   When a profile is copied, the Additional Settings configuration values will also be copied along with all other profile configuration settings.
-   **Version 9.1.0 - January 2020**
    -   New:
        -   Name column size increased to 100
        -   When a notable event is forwarded twice from Splunk ES, no duplicate Security Incident will be created/event aggregated to an existing Security Incident
        -   Users can create a manual profile with the same source, depending on the Active/Inactive status of the existing profile
        -   Added a notable event hyperlink entry in the aggregated event related list entries
        -   Default hyperlink format for worknote mapping
        -   Mapping format will support new lines when multiple event fields are mapped to a single incident field
    -   Fixed: Tooltip localization in the mapping section for +,-,\{\} icons
-   **Version 9.0.4 - November 2019**
    -   New:
        -   Create profiles to create SIR incidents for specific types of Notable events with the following configurations:
            -   Create scheduled alert and manual forwarding profiles.
            -   Map Spunk Enterprise Security notable events to SIR fields and preview them with sample data.
            -   Filter conditions and aggregation criteria for creation of SIR incidents.
            -   One-time retrieval of events for the past seven days.
            -   On-going retrieval of events with a polling interval.
            -   Notable events updates to Splunk Enterprise Security during SIR creation and closure.
            -   Aggregation of events to SIR incidents with multiple CI’s and observables.
            -   Modify manual notable event forwarding profile to use source instead of source type for mapping event types.
            -   Aggregation of events to SIR incidents when mapped splunk field to work notes and selecting log work notes check box during aggregation.

