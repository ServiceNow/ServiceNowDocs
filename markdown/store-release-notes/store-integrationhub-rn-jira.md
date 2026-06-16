---
title: Jira spoke release notes
description: Version history for the Integration Hub Jira spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-jira.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Jira spoke release notes

Version history for the Integration Hub Jira spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 6.1.3 - June 2026**

    Fixed: Streamline ACLs

-   **Version 6.0.1 - April 2026**
    -   New:
        -   Actions: Report Personal Data. You are now required by Atlassian to report user personal data usage if you store such details using existing actions of the spoke in your apps. Refer User privacy guide by Atlassian for more details.
        -   Authentication Template for Jira Cloud. Refer product documentation for more details on how to setup.
    -   Changed: Based on guidance for Building Secure and Scalable Integrations: Our Guidance for Third-Party Appsby Atlassian, the way to setup and authenticate Jira Connection has been changed for Jira Cloud customers.
    -   Removed: Authentication Template for Jira Server. You can continue to setup the spoke for Jira Server / Jira Data Center via Connections &amp; Credentials. Refer product documentation for more details on how to setup.
-   **Version 5.4.0 - January 2026**

    New: Jira Webhooks now have HMAC as supported authentication.

-   **Version 5.3.2 - December 2025**

    Fixed: Action: Create Issue

-   **Version 5.3.0 - September 2025**
    -   Fixed:
        -   Required ACL\(s\) and Role\(s\) for agents.
        -   JiraErrorHandler made public for cross scope access.
        -   Create Issue action Request Type data type.
-   **Version 5.2.3 - August 2025**

    Fixed - AI Agents - Output response includes anchor tags are now rendered as clickable link.

-   **Version 5.2.1 - July 2025**

    Fixed: Event Source, Triggers status set to Published.

-   **Version 4.6.0 - May 2025**

    Minor release with new AI agents.

-   **Version 5.2.0 - May 2025**
    -   New: Actions: Look up Audit Logs Stream \(Server 10+\) and Look up Server
    -   Minor release with new AI agents
-   **Version 5.1.1 - April 2025**

    Fixed - Actions: Update Issue, Look up Stories Stream, and Look up Issues Stream action.

-   **Version 5.1.0 - November 2024**

    Fixed: Sandbox Access for Client.

-   **Version 5.0.1 - October 2024**

    Fixed 2 bugs.

-   **Version 5.0.0 - August 2024**

    New: Added Triggers that will show up in the Trigger picker while authoring Flows to trigger Flows based on Jira Events. Note: The Triggers are only available Xanadu and onward releases.

-   **Version 4.4.1 - July 2024**

    Fixed: Create User action due to mandatory products value required in a REST API.

-   **Version 4.4.0 - June 2024**
    -   Due to changes in third-party APIs, we made the following changes:
        -   New:
            -   New actions equivalent to the ones that were deprecated:
                -   Create Issue \(create\_issue\_4\)
                -   Get Projects \(Metadata\) \(Deprecated\) \(get\_projects\_v3\)
                -   Get Projects \(Metadata\) \(get\_projects\_v4\)
                -   Get Issue Types \(Metadata\) \(get\_issue\_type\_v3\)
                -   Get Creatable Fields \(Metadata\) \(get\_creatable\_fields\_v2\)
        -   Removed:
            -   Deprecated actions:
                -   Create Issue \(create\_issue\_3\)
                -   Get Projects \(Metadata\) \(get\_projects\_2\)
                -   Get Issue Types \(Metadata\) \(get\_issue\_type\_2\)
                -   Get Creatable Fields \(Metadata\) \(get\_creatable\_fields\)
        -   Reference:
            -   Jira APIs \(https://developer.atlassian.com/changelog/\#CHANGE-1304\) have changed.
            -   Jira APIs are moving away to use Project IDs \(in lieu of Project Names\) and Issue Type IDs \(in lieu of Issue Type Names\).
        -   Other changes:
            -   Fixed:
                -   Update Issue action to manage issue
                -   Link field correctly
-   **Version 4.3.2 - January 2024**
    -   New: Added server\_type parameter in the configuration template
    -   Fixed:
        -   Payload for additional fields in Update Issue action
        -   Retain credentials when upgrading Jira Spoke
        -   Payload for Multiline fields additional fields in Update Issue action
-   **Version 4.3.1 - September 2023**
    -   Fixed:
        -   Missing OOB 'report\_view' ACLs for multiple tables
        -   Create Issue, Update Issue - Assign to - Payload for Jira Server
        -   "Get Issues" action returns Assignee as well
-   **Version 4.3.0 - August 2023**
    -   New: 2 actions - Look up Users Assignable to Projects and Create Issues
    -   Changed: 1 action - Get Creatable Fields \(Metadata\)
    -   Fixed: 2 problems - Create issue was setting Priority as --None-- and conn\_sys\_id was not declared
-   **Version 4.2.0 - June 2023**

    New: Added actions: Add Watcher, Delete Watcher, Look up Watchers.

-   **Version 4.1.0 - February 2023**
    -   New:
        -   Create Project, Look up Project, Look up Users Stream by Name actions
        -   OAuth support for Jira Cloud
    -   Changed: Look up Users Stream
-   **Version 4.0.0 - November 2022**
    -   New: Equivalent or better actions are made available for every action that was deprecated with the latest error handling mechanism and complex object outputs. Some of the actions make use of dynamic inputs as well for ease of use.
    -   Changed: Category for Look up Audit Log Streams from User Management to Audit Management.
    -   Removed: Majority of old actions are deprecated.
-   **Version 3.2.3 - September 2022**

    Fixed: De-duplication improvements.

-   **Version 3.2.2 - June 2022**
    -   Fixed: Patch release of Jira Spoke. This version includes the below changes:
        -   Fix for an issue with 'is not valid' message while sending empty values within the action - Create Issue.
        -   Issue with 'Look up Users' not running for custom queries.
        -   Fix for an issue - 'Field 'priority' cannot be set' within the action - 'Create Issue'.
        -   Fix for action - 'Look up User Account ID', returning a random user if an exact user match doesn't exist.
-   **Version 3.2.1 - March 2022**

    Fixed: This version adds a fix to show the 'Create Issue' action that was missing on Quebec.

-   **Version 3.2.0 - February 2022**

    New: Minor release of Jira Spoke for IntegrationHub. This version includes a new version of the Update Issue action.

-   **Version 3.1.1 - December 2021**

    Changed: This version includes changes in the output of the ‘Get Issues’ action.

-   **Version 3.0.12 - November 2021**

    Fixes were made in this version of the Jira spoke.

-   **Version 3.0.9 - October 2021**

    Fixed: This version includes a fix for missing Issue ID in the response of webhook when the attachment is created or deleted, and fix at webhook events.

-   **Version 3.0.7 - September 2021**

    Fixed: This is a patch version of Jira Spoke. It includes seven fixes.

-   **Version 3.0.5 - June 2021**

    This is a patch version of Jira Spoke. It includes a fix within error handling for the 'Update Issue' action.

-   **Version 3.0.4 - May 2021**

    This is a major version of Jira Spoke. It includes new actions for Webhook Management and Utility actions. Updated action for Look up Records by JQL Stream, and fixed an issue for User Management API changes of Jira.

-   **Version 2.6.8 - August 2020**
    -   Compatibility: Orlando, Paris
    -   Fixed: This is a patch version and includes a fix.
-   **Version 2.6.7 - July 2020**
    -   Compatibility: Orlando, Paris
    -   New: This release of Jira spoke includes updates to Webhook Management and SDLC Management.
-   **Version 2.6.5 - March 2020**
    -   Fixed:
        -   The ID field incorrectly returned a floating-point string value instead of a number
        -   Parsing issue at webhook sub-flow payload
-   **Version 2.6.4 - February 2020**

    New: Sprint Management actions and a fix to parse the webhook subflow payload

-   **Version 2.6.4 - January 2020**

    New: Features for SDLC project management and managing user subscriptions and actions

-   **Version 2.5.7 - July 2020**
    -   Compatibility: New York
    -   New: This updated release of Jira spoke includes changes to the action 'Get All Projects' and decisions for webhook events.
-   **Version 2.5.5 - March 2020**

    Fixed: The ID field incorrectly returned a floating-point string value instead of a number

-   **Version 2.5.1 - December 2019**

    Error handling to display an appropriate error message when invalid data is filled in on the Create Issue action and flow is run.

-   **Version 2.5.0 - October 2019**

    Added new actions to support design time metadata retrieval \(introspection\) and bi-directional webhook support as external Flow Designer triggers.

-   **Version 2.0.7 - August 2019**

    Licensing patch for the Jira spoke on Integration Hub

-   **Version 1.5.1 - March 2019**
    -   Provides Actions to automate tasks in Jira for user management, issues, projects, and the software development lifecycle
    -   Synchronize data in ServiceNow with Jira to increase collaboration between ServiceNow users and DevOps Teams

**Parent Topic:**[ServiceNow Store - Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-integrationhub-landing.md)

