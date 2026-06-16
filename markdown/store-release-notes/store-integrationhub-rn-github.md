---
title: GitHub spoke release notes
description: Version history for the Integration Hub GitHub spoke on the ServiceNow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-github.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# GitHub spoke release notes

Version history for the Integration Hub GitHub spoke on the ServiceNow.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.6.0 - June 2026**

    Fixed: Streamline ACLs

-   **Version 3.5.2 - April 2026**

    Fixed: Resolved an issue where theCreate Issue action failed when field values in the issue body contained an equals \(=\) sign

-   **Version 3.5.1 - January 2026**
    -   Fixed:
        -   Added support for retrieving GitHub organization audit log events through the new Audit Log action.
        -   Fixed an issue where a GitHub data stream action failed due to incorrect parent URL construction, causing malformed API requests.
        -   Introduced a new data stream action to fetch commit details by SHA, addressing a missing capability in the GitHub AI Agent.
-   **Version 3.5.0 - December 2025**
    -   Added a GitHub Agent that enables conversational file creation, branch management, and repository updates.
    -   Enhanced GitHub Enterprise integration to use the Audit Log API for secure, compliant event retrieval.
    -   Fixed repository schema fetch failure by aligning branch validation for Expense Tracker setup.
    -   Resolved API defects involving invalid org handling, future date validation, and pagination accuracy.
-   **Version 3.4.1 - November 2025**

    Fixed: Read-only Directive. Refer the global communication for the detailed notes for this directive.

-   **Version 3.3.0 - September 2025**

    Fixed - Required ACL\(s\) or Role\(s\) for agents.

-   **Version 3.2.2 - August 2025**

    Fixed - Create Comment on Pull Request, AI Agent output with anchor tags

-   **Version 3.2.1 - July 2025**

    Fixed: Event Source, Triggers status set to Published.

-   **Version 3.2.0 - May 2025**

    Minor release with new AI agents.

-   **Version 3.1.1 - November 2024**

    Fixed: Sandbox access for client.

-   **Version 3.0.1 - October 2024**

    Fixed: ACL issue.

-   **Version 3.0.0 - August 2024**
    -   New:
        -   Use of the trigger builder framework to create new trigger content for GitHub Spoke.
        -   Added Trigger for events Branch, Pull request, Push/commit and Release
-   **Version 2.3.0 - May 2024**
    -   Added the below actions:
        -   Look up Authenticated User
        -   Look up Organization Events Stream
        -   Look up Orgazination Outside CollaboratorsStream
        -   Look up Organization Pending Outside Collaborators Stream
        -   Look up Organization Invitations Stream
        -   Remove Organization Outside Collaborator
    -   Enhanced the integration functionality to support:
        -   Pending Invitations
        -   Outside Colloborators
        -   Pending Outside Colloborators
        -   Revoking Outside Colloborators
-   **Version 2.2.9 - January 2024**
    -   Fixed:
        -   Getting exception when using "Add collaborator" action
        -   Unusable "Update Branch Protection" branch as params not accepting null values
-   **Version 2.2.8 - October 2023**
    -   Fixed:
        -   Fix the double "p" typo under the buildDecisionTableInput function in GitHubCommitEventInputBuilder script includes
        -   Mark the GitHubUtils script includes to "all application scopes" instead of "this application only."
        -   Expose GitHub API Header fields, especially "Hook-ID" field, in the Decision Table's condition dropdown
        -   \[Security Bug\] Sub Flows configured to run as System \| GitHub Spoke
        -   \[Security Bug\] Missing OOB \`report\_view\` ACLs for multiple tables \| GitHub Spoke
-   **Version 2.2.7 - August 2023**

    In v2.2.7, the pagination issue for Data Stream actions was fixed.

-   **Version 2.2.6 - May 2023**
    -   Fixed: Download subscription job is successful even though get organization action is failed
    -   Fixed: Remove Organisation member action doesn't remove the user
-   **Version 2.2.4 - December 2022**

    Patch release of GitHub Spoke for IntegrationHub. This version includes localization fixes.

-   **Version 2.2.3 - October 2022**

    Fixed: Patch release of GitHub Spoke for Integration Hub. This version includes a fix to improve the installation performance and an issue with not being able to read property "name" for Organisational related actions.

-   **Version 2.2.2 - December 2021**

    New: This version adds a private action to get branches and commits from GitHub.

-   **Version 2.1.0 - September 2021**
    -   New:
        -   Added a sample outbound flow
        -   Added authentication configuration template for easier connection setup
    -   Changed: Updated sample inbound subflows for better integration experience
-   **Version 2.0.4 - July 2021**

    Patch Release for GitHub Spoke of IntegrationHub. This version adds KMF modules for additional security of the password2 fields, and makes it compatible with Rome.

-   **Version 2.0.3 - June 2021**

    This is a patch release for the GitHub spoke with fixes included in it.

-   **Version 2.0.1 - February 2021**

    Added support for downloading user subscriptions, tracking user activity, and reclaiming licenses for GitHub Enterprise Cloud and GitHub Enterprise Server subscriptions.

-   **Version 1.0.2 - February 2020**

    Fixed an issue with webhooks.

-   **Version 1.0.1 - January 2020**

    Automate branch, repository, source code, and issue management of your GitHub instance from the ServiceNow instance.


