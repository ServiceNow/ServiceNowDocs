---
title: Tanium Integration V2 for Security Operations release notes
description: Version history for the Security Operations Tanium integration v2 on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-tanium-v2.html
release: store
topic_type: reference
last_updated: "2021-10-14"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Tanium Integration V2 for Security Operations release notes

Version history for the Security Operations Tanium integration v2 on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 10.3.5 - October 2021**

    Fixed: Added additional password-related policies.

-   **Version 10.3.3 - December 2020**

    Changed: With Key Management Framework plugin, developers will have an ability to manage keys used for Password2 fields through crypto module definition.

-   **Version 5.0.5 - September 2019**
    -   Fixed:
        -   Maximum wait time for sightings search results
        -   Maximum results returned for sightings search
        -   Re-ordering of API username and password fields in integration configuration
        -   Availability of Tanium Sightings Details and Tanium Sightings Results in all Related Lists of the security incident without additional configuration
-   **Version 5.0.4 - June 2019**
    -   This version of the Tanium V2 integration supports expanded use cases for Tanium capabilities. It has been tested with versions 7.2x and 7.3x of the Tanium console.
    -   A more limited Tanium integration is currently available in the ServiceNow Store that supports queries for running process details. For more feature options and product capabilities, this V2 integration is the preferred version of the Tanium integration.
-   **Version 5.0.3 - April 2019**
    -   This is the initial version of the Tanium that supports expanded use cases for Tanium capabilities. A more limited Tanium is currently available in the ServiceNow Store that supports queries for running process details. For more feature options and product capabilities, this V2 integration is the preferred version of the Tanium.
        -   Supports automated triggering of Tanium queries and actions based on incident conditions
        -   Supports launching of Tanium capabilities manually from ServiceNow AI Platform® Security Incident Response \(SIR\) security incidents
        -   Flexibility to create multiple profiles for triggering different types of Tanium and ServiceNow AI Platform Security Operations capabilities. These profiles gather threat event information or perform actions based on the conditions of specific incident categories such as malware
        -   Validate your profile configuration with a preview of the Tanium results on SIR security incidents
        -   Isolate compromised systems from the network, and, after remediation, return the systems to the network
        -   Launch enterprise-wide searches for malicious hashes, and create child incidents or response tasks to track follow-up remediation
        -   If tagging is enabled, security tags identify which Tanium capabilities are initially launched by a workflow and when the queries or actions are successfully completed
        -   A full audit trail of Tanium queries and actions is logged in the work notes on SIR security incidents
        -   Supports multiple Tanium consoles so that you can apply different policies to user groups and regions

