---
title: McAfee ePO integration for Security Operations release notes
description: Version history for the McAfee ePO integration for Security Operations on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-mcafee-epo.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# McAfee ePO integration for Security Operations release notes

Version history for the McAfee ePO integration for Security Operations on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 10.6.1 - June 2026**

    Fixed: Access issues for Security Analyst while querying tables.

-   **Version 10.6.0 - December 2025**

    New: Upgraded all dictionary-level read-only fields to Strict Read-Only to enhance security and prevent unauthorized changes.This update ensures the server consistently enforces read-only behaviour across all UIs, scripts, and integrations.

-   **Version 10.5.11 - August 2025**

    Fixed: Error sys\_scope during Lookup Source in McAfee EPO Integration.

-   **Version 10.5.1 - February 2025**

    New: Migrated existing default Workflows to Flow Designs using Flow Designer.

-   **Version 10.4.7 - November 2024**

    New: Migrated existing default Workflows to Flow Designs using Flow Designer.

-   **Version 10.4.6 - December 2023**

    Fixed: Misconfiguration of table/field ACLs within com.snc.secops.mcafee.epo plugin.

-   **Version 10.4.5 - November 2023**
    -   Changed: Added localization translations.
    -   Fixed: The report\_view access control list \(ACL\) was missing for some tables.
-   **Version 10.4.3 - August 2023**

    Changed:

    -   Migrated this integration to the capability framework.
    -   UI Framework built for capabilities in the new workspace.
-   **Version 10.3.6 - June 2022**

    Fixed: Localization and Internationalization issues in UI messages, and ACL-related issues are resolved to enable the Security Analyst to see capability profile records.

-   **Version 10.3.5 - October 2021**

    Fixed: Added additional password-related policies.

-   **Version 10.3.3 - December 2020**

    Changed: With Key Management Framework plugin, developers will have an ability to manage keys used for Password2 fields through crypto module definition.

-   **Version 5.0.0 - April 2019**
    -   Supports automated triggering of McAfee ePO queries and actions based on incident conditions
    -   Supports launching McAfee ePO capabilities manually from ServiceNow AI Platform® Security Incident Response \(SIR\) security incidents
    -   The flexibility to create multiple profiles for triggering different types of McAfee ePO and ServiceNow AI Platform Security Operations capabilities. These profiles automatically gather threat event information that is based on the conditions of specific incident types such as malware.
    -   Validate your profile configuration with a preview of the McAfee ePO results on SIR security incidents.
    -   Initiate malware scans from a SIR security incident to identify potential system compromise.
    -   Isolate compromised systems from the network, and, after remediation, return the systems to the network.
    -   If tagging is enabled, security tags identify which McAfee ePO capabilities are initially launched by a workflow and when the queries or actions are successfully completed.
    -   A complete audit trail of the McAfee ePO queries and actions is posted on SIR security incidents, and commands from the ServiceNow AI Platform are logged in the McAfee ePO console.
    -   Supports multiple McAfee ePO consoles so that you can apply different policies to user groups and regions.

