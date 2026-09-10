---
title: Vulnerability Response Integration with Atlassian Jira release notes
description: Version history for the Vulnerability Response Integration with Atlassian Jira application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-vr-integration-jira.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Vulnerability Response version history release notes, ServiceNow Store - Security Operations version history release notes, ServiceNow Store version history release notes]
---

# Vulnerability Response Integration with Atlassian Jira release notes

Version history for the Vulnerability Response Integration with Atlassian Jira application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.1.6 - September 2026**

    Fixed: An integration failure due to the choice/select-type Jira field. Choice-type custom field mappings are correctly formatted for choice-type values as Jira expects, and Jira issues are created successfully.

-   **Version 1.1.4 - August 2026**
    -   Changed:
        -   Enhancements to the integration so that the current Get Issue Types \(v3\) and Get Creatable Fields \(v2\) APIs are supported, replacing the deprecated endpoints ahead of their anticipated retirement.
        -   Issue type references now use Jira's numeric ID instead of a name, and a one-time background job re-syncs existing Agile Tool Rule Config records to the new format upon upgrade.
-   **Version 1.0.4 - May 2024**
    -   Fixed:
        -   Vulnerability admin, Vulnerability Analyst from VR can create JIRA tickets
        -   Container admin, Container Analyst from Container Vulnerability Response can create Jira tickets
        -   Security Manager from Application Vulnerability Response can create Jira tickets
-   **Version 1.0.3 - October 2023**

    Fixed: Added null check during creation of Jira issue.

-   **Version 1.0.2 - August 2023 \(Vancouver\)**

    This app enables integration of Vulnerability Response with Atlassian Jira to create issues corresponding to Remediation Tasks.

    New:

    -   Integrate Vulnerability Response with Atlassian Jira to create issues or tickets corresponding to remediation tasks.
    -   Choose between automatic versus manual creation of issues or tickets.
    -   Track remediation progress by syncing status from Atlassian Jira to Vulnerability Response.

