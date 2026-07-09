---
title: DevOps Change Velocity release notes
description: The ServiceNow DevOps Change Velocity application improves visibility into your DevOps data in a single system, automates and accelerates change processes, and helps you gain insights to measure the performance of your DevOps environment. DevOps Change Velocity was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
---

# DevOps Change Velocity release notes

The ServiceNow® DevOps Change Velocity application improves visibility into your DevOps data in a single system, automates and accelerates change processes, and helps you gain insights to measure the performance of your DevOps environment. DevOps Change Velocity was enhanced and updated in the Zurich release.

## DevOps Change Velocity highlights for the Zurich release

-   Improve instance efficiency by skipping step-level pipeline processing.
-   Improve load balancing and failover protection by selecting a MID Server cluster during tool connection.

See [DevOps Change Velocity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/devops-landing-page-new.md) for more information.

**Important:** DevOps Change Velocity is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Import based evidence collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/import-based-evidence-collection-for-orchestration-capability.md)**

    Improve instance efficiency by skipping step-level pipeline processing for accelerated change management and evidence collection for GitHub Actions, Azure DevOps \(ADO\), GitLab and  Jenkins orchestration tools.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Support for MID Server cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/playbook-enter-github-instance-details.md)**

    Improve load balancing and failover protection by selecting a MID Server cluster when connecting to a tool instance associated with a MID Server cluster. This configuration enables multiple MID Servers with relevant capabilities to be grouped.

-   **[Improved UX for DevOps Change health scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/run-health-scan-check.md)**

    Run health scans and analyze findings efficiently in the DevOps Change workspace with an intuitive and user-friendly interface.

-   **[Pipeline association for GitHub Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/sc-github.md)**

    When onboarding GitHub Actions pipelines through the App onboarding catalog or the onboarding APIs, now only the selected pipelines are associated with the DevOps app. If no pipeline is selected, all pipelines within the specified repository are associated.

-   **[Tool connection check status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/devops-reference-error-messages.md)**

    If a tool is marked as Disconnected because of a system-generated failure during an unsuccessful connection check, any subsequent successful check automatically updates the connection status to Connected. If you manually disconnect the tool, the tool status remains Disconnected even if there’s a subsequent successful connection check.

-   **[New roles for vulnerability integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/installed-with-dev-ops.md)**
    -   The sn\_vul.app\_sec\_manager role is added to the DevOps Tool Owner \[sn\_devops.tool\_owner\] role when the DevOps Vulnerability Integrations plugin \(sn\_devops\_vul\_ints\) is installed.
    -   The sn\_vul\_veracode.configure\_integration role is added to the DevOps Tool Owner \[sn\_devops.tool\_owner\] role when the Vulnerability Response Integration with Veracode plugin \(sn\_vul\_veracode\) is installed.
-   **[Prod deploy commit logic for other step types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/dev-ops-commits-release.md)**

    Update the **sn\_devops.commit\_rel\_change\_step\_type** property to have other step types, like Test or Deploy, use the same commit logic as Prod Deploy.

-   **[Override start and end time of a change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/dev-ops-config-change-details.md)**

    Set the  **sn\_devops.change\_request.auto\_close\_allow\_override\_start\_time ** and  **sn\_devops.change\_request.auto\_close\_allow\_override\_end\_time ** properties as false to consider the change request start and end time instead of the pipeline’s when the  autoCloseChange  parameter is enabled in a pipeline.

-   **[Node version of DevOps extension](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/config-dev-ops-extensions-azure.md)**

    The node version of the ServiceNow DevOps  extension has been upgraded to version 20.x in Azure DevOps.

-   **[Enhanced pipeline governance in GitLab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/servicenow-custom-actions-for-gitlab.md)**

    View change request details like status, sys\_id, priority in the GitLab console when a change request is created in GitLab using Docker image.

-   **[Health scan enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/run-health-scan-check.md)**
    -   Identify outdated or prolonged discover and import requests using the DevOps -Stale or Long-Running Discover and Import Requests health check.
    -   Verify whether webhooks have been configured correctly for any tracked repository, pipeline, or plan in  GitHub,  GitLab,  Azure DevOps, and  Jenkins using the DevOps webhook configuration analysis health check.
    -   Identify OAuth app configuration issues for GitHub tools in the connected state using the DevOps webhook configuration analysis health check.
    -   Verify if any scheduled job has been configured to run as an invalid or non-admin user.
    -   Navigate to the Findings list from the DevOps Change Workspace home page by selecting  **View all findings ** in the  Health scan findings  widget. 
-   **[Enhanced JFrog integration with DevOps Change Velocity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/devops-jfrog-connect-workspace.md)**

    Gather JFrog evidence seamlessly and create change records automatically using the improved JFrog integration with DevOps Change Velocity.

-   **[Bearer authentication in JFrog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/devops-jfrog-connect-workspace.md)**

    Connect to JFrog using the secure bearer token authentication to comply with JFrog’s updated security policies.

-   **[HTTP proxy for Docker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/servicenow-custom-actions-for-gitlab.md)**

    Connect to DevOps Change Velocity through HTTP proxy settings using environment variables in your Docker deployment for instances that run a proxy server.

-   **[Health scan enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/run-health-scan-check.md)**
    -   Identify any callback processing issues in your instance.
    -   Identify any access control rule \(ACL\) that is incorrectly associated with a role in your instance.
    -   Verify whether all DevOps tables are present in your instance and confirm whether all metadata in sys\_\* tables is present.
    -   Verify whether all DevOps roles in your instance contain all expected roles, including inherited roles.
-   **[Auto close without Change Management - State Model \[Legacy\] plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/dev-ops-change-acceleration.md)**

    Change requests can now be auto-closed without requiring you to install the Change Management - State Model \[Legacy\] plugin.

-   **[Jira authentication with 3LO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/connect-a-jira-tool-using-oauth-2-0-with-3lo.md)**

    Authenticate a Jira tool connection using OAuth 2.0 with three-legged OAuth \(3LO\) to enable secure, delegated access to your Jira account.

-   **[Bitbucket Cloud basic authentication using API token with scopes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/bitbucket-integration-dev-ops.md)**

    Connect to Bitbucket Cloud using Basic Auth by providing the email address and API token with the required scopes for your Bitbucket Cloud account as app password has been deprecated by Bitbucket.


## Activation information

Install DevOps Change Velocity by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Performance Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/pa-overview.md)**

    The ServiceNow® Performance Analytics application is an in-platform process optimization solution to create management dashboards, report on Key Performance Indicators \(KPIs\) and metrics, and answer key business questions. The application helps improve quality and reduces the costs of service delivery.

-   **[Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/c_ITILChangeManagement.md)**

    The ServiceNow® Change Management application provides a systematic approach to control the life cycle of all changes, facilitating beneficial changes to be made with minimum disruption to IT services.

-   **Agile Development**

    The ServiceNow® Agile Development application helps you deliver software projects more efficiently by managing and tracking software development life cycles using an iterative, incremental, and flexible approach.

-   **[Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/grc-risk-overview.md)**

    The ServiceNow® Governance, Risk, and Compliance Risk Management application helps you continuously monitor and identify high-impact risks, improve your risk-based decision-making, and reduce reaction time effectively. The application also provides structured workflows for the management of risk assessments, risk indicators, and risk issues.


**Parent Topic:**[IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/it-service-management-rn-landing.md)

