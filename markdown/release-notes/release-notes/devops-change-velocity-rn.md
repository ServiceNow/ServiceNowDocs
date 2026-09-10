---
title: DevOps Change Velocity release notes
description: The ServiceNow DevOps Change Velocity application improves visibility into your DevOps data in a single system, automates and accelerates change processes, and helps you gain insights to measure the performance of your DevOps environment. DevOps Change Velocity was enhanced and updated in the Australia release.The version 7.1 release adds support for authenticating Rally tool connections with OAuth 2.0 credentials, and GitHub Data Residency.The ServiceNow DevOps Change Velocity application improves visibility into your DevOps data in a single system, automates and accelerates change processes, and helps you gain insights to measure the performance of your DevOps environment. DevOps Change Velocity was enhanced and updated in the Australia release.The ServiceNow DevOps Change Velocity application improves visibility into your DevOps data in a single system, automates and accelerates change processes, and helps you gain insights to measure the performance of your DevOps environment. DevOps Change Velocity was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 3
---

# DevOps Change Velocity release notes

The ServiceNow® DevOps Change Velocity application improves visibility into your DevOps data in a single system, automates and accelerates change processes, and helps you gain insights to measure the performance of your DevOps environment. DevOps Change Velocity was enhanced and updated in the Australia release.

## About DevOps Change Velocity

-   Improve visibility into your DevOps data in a single system.
-   Automate the change workflow and approval decisions to increase change velocity while ensuring governance and control.
-   Track the progress of your work items, commits, artifacts, builds, and releases using the change requests to lend additional transparency and provide a single source of truth to all the personas involved.

See [DevOps Change Velocity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-landing-page-new.md) for more information.

## Activation and other requirements

**Important:** DevOps Change Velocity is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install DevOps Change Velocity by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/it-service-management-rn-landing.md)

## Version 7.1

The version 7.1 release adds support for authenticating Rally tool connections with OAuth 2.0 credentials, and GitHub Data Residency.

### What's new

-   **Rally authentication with OAuth 2.0**

    Authenticate a Rally tool connection using OAuth 2.0 credentials to strengthen your tool security.

-   **[GitHub Data Residency support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/playbook-enter-github-instance-details.md)**

    Connect to GitHub Enterprise Server with data residency controls to keep your organization's code and data in your preferred geographic location.


## Version 7.0

The ServiceNow® DevOps Change Velocity application improves visibility into your DevOps data in a single system, automates and accelerates change processes, and helps you gain insights to measure the performance of your DevOps environment. DevOps Change Velocity was enhanced and updated in the Australia release.

### What's changed

-   **[Jira authentication with 3LO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/connect-a-jira-tool-using-oauth-2-0-with-3lo.md)**

    Authenticate a Jira tool connection using OAuth 2.0 with three-legged OAuth \(3LO\) to enable secure, delegated access to your Jira account.

-   **[Bitbucket Cloud basic authentication using API token with scopes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/bitbucket-integration-dev-ops.md)**

    Connect to Bitbucket Cloud using Basic Auth by providing the email address and API token with the required scopes for your Bitbucket Cloud account as app password has been deprecated by Bitbucket.


## Version 6.3

The ServiceNow® DevOps Change Velocity application improves visibility into your DevOps data in a single system, automates and accelerates change processes, and helps you gain insights to measure the performance of your DevOps environment. DevOps Change Velocity was enhanced and updated in the Australia release.

### What's changed

-   **[Enhanced JFrog integration with DevOps Change Velocity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-jfrog-connect-workspace.md)**

    Gather JFrog evidence seamlessly and create change records automatically using the improved JFrog integration with DevOps Change Velocity.

-   **[Bearer authentication in JFrog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-jfrog-connect-workspace.md)**

    Connect to JFrog using the secure bearer token authentication to comply with JFrog’s updated security policies.

-   **[HTTP proxy for Docker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/servicenow-custom-actions-for-gitlab.md)**

    Connect to DevOps Change Velocity through HTTP proxy settings using environment variables in your Docker deployment for instances that run a proxy server.

-   **[Health scan enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/run-health-scan-check.md)**
    -   Identify any callback processing issues in your instance.
    -   Identify any access control rule \(ACL\) that is incorrectly associated with a role in your instance.
    -   Verify whether all DevOps tables are present in your instance and confirm whether all metadata in sys\_\* tables is present.
    -   Verify whether all DevOps roles in your instance contain all expected roles, including inherited roles.
-   **[Auto close without Change Management - State Model \[Legacy\] plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/dev-ops-change-acceleration.md)**

    Change requests can now be auto-closed without requiring you to install the Change Management - State Model \[Legacy\] plugin.


