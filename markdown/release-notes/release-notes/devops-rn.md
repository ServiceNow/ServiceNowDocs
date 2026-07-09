---
title: DevOps Change Velocity release notes
description: The ServiceNow DevOps Change Velocity application improves visibility into your DevOps data in a single system, automates and accelerates change processes, and helps you gain insights to measure the performance of your DevOps environment. DevOps Change Velocity was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 8
---

# DevOps Change Velocity release notes

The ServiceNow® DevOps Change Velocity application improves visibility into your DevOps data in a single system, automates and accelerates change processes, and helps you gain insights to measure the performance of your DevOps environment. DevOps Change Velocity was enhanced and updated in the Yokohama release.

## DevOps Change Velocity highlights for the Yokohama release

-   Integrate with the Harness orchestration tool to discover Harness pipelines and enable change automation.
-   Detect anomalies and issues in your DevOps Change Velocity instance using health scans.

See [DevOps Change Velocity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-landing-page-new.md) for more information.

**Important:** DevOps Change Velocity is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading DevOps Change Velocity to Yokohama

If you are a new customer or are using a zBoot instance and you want to create type-based workflow change requests in DevOps Change Velocity, you must add the**com.snc.change\_management.change\_model.type\_compatibility** property and set it to True. For more information, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/t_AddAPropertyUsingSysPropsList.md).

If you are an upgrading customer, you must run the **ReConfigure Bitbucket Server Repositories for PullRequest** job to re-configure your existing Bitbucket Server or Bitbucket Data Center repositories so that pull request records can be imported. You can navigate to **All &gt; System Definition &gt; Scheduled Jobs** to search for this job and run it.

## New in the Yokohama release

-   **[Harness integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/harness-integration-with-devops-change-velocity.md)**

    Discover Harness pipelines and configure real-time notifications to enable change traceability and automation by integrating the Harness orchestration tool with DevOps Change Velocity.

-   **[DevOps Health instance scan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/run-health-scan-check.md)**

    Detect anomalies and issues in the instance by running or scheduling health scans on your DevOps Change Velocity instance.

-   **[Bitbucket Cloud tool integration with ServiceNow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/bitbucket-integration-dev-ops.md)**

    Integrate the Bitbucket Cloud coding tool with DevOps Change Velocity to connect, discover, import, and process real-time repository events in DevOps Change Velocity.

-   **[DevOps Change Workspace UI for simplified creation of custom tool integration with planning, coding and orchestration capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/create-a-tool-integration-from-the-devops-change-workspace.md)**

    Integrate a new custom tool across planning, coding and orchestration capabilities with basic know-how of ServiceNow using an intuitive DevOps Change Workspace UI. It offers easy navigation to the ServiceNow Platform for defining transformer or adapter rules, or integrate the ability to do so within the Workspace wherever applicable, and embeds necessary documentation links and tooltips to support self-service.

-   **[Import based evidence collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/import-based-evidence-collection-for-orchestration-capability.md)**

    Improve instance efficiency by skipping step-level pipeline processing for accelerated change management and evidence collection for GitHub Actions, Azure DevOps \(ADO\), GitLab and  Jenkins orchestration tools.


## Changed in this release

-   **[Simplified onboarding of orchestration tools not supported in the base system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-user-created-orchestration-tool-integration.md)**

    Integrate orchestration tools that aren’t supported in the base system by leveraging a generic framework.

-   **[Custom fields for planning tool integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/add-custom-field-for-a-planning-tool-integration.md)**

    Add custom fields into your planning tool integration to improve configurability and access business-specific information, which facilitates more informed decision-making.

-   **[Additional scans for DevOps Health Scan Content pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/run-health-scan-check.md)**

    Additional set of proactive checks focused on problems that tend to occur before or after an upgrade along with identifying configuration issues like plugin and version incompatibilities, or pipelines that chronically fail, have been added.

-   **[Import pull-request records for Bitbucket Server or Bitbucket Data Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-wkspc-bitbucket-tool-conn.md)**

    Import pull-request records for Bitbucket Server or Data Center for improved insights and efficiency.

-   **[Change request creation with errors in DevOps data retrieval for Harness pipelines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/change-request-creation-with-devops-data-retrieval-errors.md)**

    Enable change request creation even if there is an error in retrieving the DevOps data for a Harness pipeline.

-   **[Branch name filter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/create-devops-change-request-manual.md)**

    Search for build numbers by the branch name while associating DevOps data to a change request in the Service Operations Workspace \(SOW\) or Classic UI.

-   **[Test summary name in GitHub Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/servicenow-devops-custom-actions-from-github-marketplace.md)**

    The servicenow-devops-test-report custom action in GitHub now includes an optional test-summary-name parameter to specify the test summary results name.

-   **[Token based authentication for Rally](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/configure-webhooks-for-rally-manually.md)**

    Configure webhooks for Rally using token based authentication instead of using the integration username and password.

-   **[Renamed variables for Docker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/servicenow-custom-actions-for-gitlab.md)**

    The environmental variables in the Generic Docker actions for DevOps Change Velocity have been renamed by removing the CI prefix for better clarity.

-   **[Security scan results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/dev-ops-change-acceleration.md)**

    Security scan results on the change record associated to a pipeline execution with a linked package are now displayed in the **Security Summaries** tab.

-   **[Source of commits in SOW](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/create-change-sow.md)**

    View the source of commits like pipeline execution, branch, repository, and so on for a change request in the DevOps data section of the Service Operations Workspace.

-   **[Track file changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/sc-github.md)**

    The **Track file changes** option is now disabled by default when a repository is configured to prevent any potential security risks.

-   **[Close code value for a change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/dev-ops-administration.md)**

    Two new properties have been added in DevOps Change Velocity, so that you can specify a close code value for a change request based on the change request completion state when the autoCloseChange parameter is enabled.

-   **[Support for MID Server cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/playbook-enter-github-instance-details.md)**

    Improve load balancing and failover protection by selecting a MID Server cluster when connecting to a tool instance associated with a MID Server cluster. This configuration enables multiple MID Servers with relevant capabilities to be grouped.

-   **[Improved UX for DevOps Change health scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/run-health-scan-check.md)**

    Run health scans and analyze findings efficiently in the DevOps Change workspace with an intuitive and user-friendly interface.

-   **[Pipeline association for GitHub Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/sc-github.md)**

    When onboarding GitHub Actions pipelines through the App onboarding catalog or the onboarding APIs, now only the selected pipelines are associated with the DevOps app. If no pipeline is selected, all pipelines within the specified repository are associated.

-   **[Tool connection check status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-reference-error-messages.md)**

    If a tool is marked as Disconnected because of a system-generated failure during an unsuccessful connection check, any subsequent successful check automatically updates the connection status to Connected. If you manually disconnect the tool, the tool status remains Disconnected even if there’s a subsequent successful connection check.

-   **[New roles for vulnerability integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/installed-with-dev-ops.md)**
    -   The sn\_vul.app\_sec\_manager role is added to the DevOps Tool Owner \[sn\_devops.tool\_owner\] role when the DevOps Vulnerability Integrations plugin \(sn\_devops\_vul\_ints\) is installed.
    -   The sn\_vul\_veracode.configure\_integration role is added to the DevOps Tool Owner \[sn\_devops.tool\_owner\] role when the Vulnerability Response Integration with Veracode plugin \(sn\_vul\_veracode\) is installed.
-   **[Prod deploy commit logic for other step types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/dev-ops-commits-release.md)**

    Update the **sn\_devops.commit\_rel\_change\_step\_type** property to have other step types, like Test or Deploy, use the same commit logic as Prod Deploy.

-   **[Override start and end time of a change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/dev-ops-config-change-details.md)**

    Set the  **sn\_devops.change\_request.auto\_close\_allow\_override\_start\_time ** and  **sn\_devops.change\_request.auto\_close\_allow\_override\_end\_time ** properties as false to consider the change request start and end time instead of the pipeline’s when the  autoCloseChange  parameter is enabled in a pipeline.

-   **[Node version of DevOps extension](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/config-dev-ops-extensions-azure.md)**

    The node version of the ServiceNow DevOps  extension has been upgraded to version 20.x in Azure DevOps.

-   **[Enhanced pipeline governance in GitLab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/servicenow-custom-actions-for-gitlab.md)**

    View change request details like status, sys\_id, priority in the GitLab console when a change request is created in GitLab using Docker image.

-   **[Health scan enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/run-health-scan-check.md)**
    -   Identify outdated or prolonged discover and import requests using the DevOps -Stale or Long-Running Discover and Import Requests health check.
    -   Verify whether webhooks have been configured correctly for any tracked repository, pipeline, or plan in  GitHub,  GitLab,  Azure DevOps, and  Jenkins using the DevOps webhook configuration analysis health check.
    -   Identify OAuth app configuration issues for GitHub tools in the connected state using the DevOps webhook configuration analysis health check.
    -   Verify if any scheduled job has been configured to run as an invalid or non-admin user.
    -   Navigate to the Findings list from the DevOps Change Workspace home page by selecting  **View all findings ** in the  Health scan findings  widget. 
-   **[Enhanced JFrog integration with DevOps Change Velocity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-jfrog-connect-workspace.md)**

    Gather JFrog evidence seamlessly and create change records automatically using the improved JFrog integration with DevOps Change Velocity.

-   **[Bearer authentication in JFrog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-jfrog-connect-workspace.md)**

    Connect to JFrog using the secure bearer token authentication to comply with JFrog’s updated security policies.

-   **[HTTP proxy for Docker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/servicenow-custom-actions-for-gitlab.md)**

    Connect to DevOps Change Velocity through HTTP proxy settings using environment variables in your Docker deployment for instances that run a proxy server.

-   **[Health scan enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/run-health-scan-check.md)**
    -   Identify any callback processing issues in your instance.
    -   Identify any access control rule \(ACL\) that is incorrectly associated with a role in your instance.
    -   Verify whether all DevOps tables are present in your instance and confirm whether all metadata in sys\_\* tables is present.
    -   Verify whether all DevOps roles in your instance contain all expected roles, including inherited roles.
-   **[Auto close without Change Management - State Model \[Legacy\] plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/dev-ops-change-acceleration.md)**

    Change requests can now be auto-closed without requiring you to install the Change Management - State Model \[Legacy\] plugin.


## Activation information

Activate DevOps Change Velocity by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Performance Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/pa-overview.md)**

    ServiceNow® Performance Analytics is an in-platform process optimization solution to create management dashboards, report on KPIs and metrics, and answer key business questions. The application helps improve quality and reduces the costs of service delivery.

-   **[Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/c_ITILChangeManagement.md)**

    The ServiceNow® Change Management application provides a systematic approach to control the life cycle of all changes, facilitating beneficial changes to be made with minimum disruption to IT services.

-   **Agile Development**

    The ServiceNow® Agile Development application helps you deliver software projects more efficiently by managing and tracking software development life cycles using an iterative, incremental, and flexible approach.

-   **[Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/grc-risk-overview.md)**

    The ServiceNow® Governance, Risk, and Compliance Risk Management application helps you continuously monitor and identify high-impact risks, improve your risk-based decision-making, and reduce reaction time effectively. The application also provides structured workflows for the management of risk assessments, risk indicators, and risk issues.


**Parent Topic:**[IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/it-service-management-rn-landing.md)

