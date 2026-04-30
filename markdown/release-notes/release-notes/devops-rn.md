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

See [DevOps Change Velocity](https://www.servicenow.com/docs/access?context=devops-landing-page-new&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information.

**Important:** DevOps Change Velocity is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading DevOps Change Velocity to Yokohama

If you are a new customer or are using a zBoot instance and you want to create type-based workflow change requests in DevOps Change Velocity, you must add the**com.snc.change\_management.change\_model.type\_compatibility** property and set it to True. For more information, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

If you are an upgrading customer, you must run the **ReConfigure Bitbucket Server Repositories for PullRequest** job to re-configure your existing Bitbucket Server or Bitbucket Data Center repositories so that pull request records can be imported. You can navigate to **All &gt; System Definition &gt; Scheduled Jobs** to search for this job and run it.

## New in the Yokohama release

-   **[Harness integration](https://www.servicenow.com/docs/access?context=harness-integration-with-devops-change-velocity&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Discover Harness pipelines and configure real-time notifications to enable change traceability and automation by integrating the Harness orchestration tool with DevOps Change Velocity.

-   **[DevOps Health instance scan](https://www.servicenow.com/docs/access?context=run-health-scan-check&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Detect anomalies and issues in the instance by running or scheduling health scans on your DevOps Change Velocity instance.

-   **[Bitbucket Cloud tool integration with ServiceNow](https://www.servicenow.com/docs/access?context=bitbucket-integration-dev-ops&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Integrate the Bitbucket Cloud coding tool with DevOps Change Velocity to connect, discover, import, and process real-time repository events in DevOps Change Velocity.

-   **[DevOps Change Workspace UI for simplified creation of custom tool integration with planning, coding and orchestration capabilities](https://www.servicenow.com/docs/access?context=create-a-tool-integration-from-the-devops-change-workspace&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Integrate a new custom tool across planning, coding and orchestration capabilities with basic know-how of ServiceNow using an intuitive DevOps Change Workspace UI. It offers easy navigation to the ServiceNow Platform for defining transformer or adapter rules, or integrate the ability to do so within the Workspace wherever applicable, and embeds necessary documentation links and tooltips to support self-service.

-   **[Import based evidence collection](https://www.servicenow.com/docs/access?context=import-based-evidence-collection-for-orchestration-capability&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Improve instance efficiency by skipping step-level pipeline processing for accelerated change management and evidence collection for GitHub Actions, Azure DevOps \(ADO\), GitLab and  Jenkins orchestration tools.


## Changed in this release

-   **[Simplified onboarding of orchestration tools not supported in the base system](https://www.servicenow.com/docs/access?context=devops-user-created-orchestration-tool-integration&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Integrate orchestration tools that aren’t supported in the base system by leveraging a generic framework.

-   **[Custom fields for planning tool integration](https://www.servicenow.com/docs/access?context=add-custom-field-for-a-planning-tool-integration&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Add custom fields into your planning tool integration to improve configurability and access business-specific information, which facilitates more informed decision-making.

-   **[Additional scans for DevOps Health Scan Content pack](https://www.servicenow.com/docs/access?context=run-health-scan-check&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Additional set of proactive checks focused on problems that tend to occur before or after an upgrade along with identifying configuration issues like plugin and version incompatibilities, or pipelines that chronically fail, have been added.

-   **[Import pull-request records for Bitbucket Server or Bitbucket Data Center](https://www.servicenow.com/docs/access?context=devops-wkspc-bitbucket-tool-conn&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Import pull-request records for Bitbucket Server or Data Center for improved insights and efficiency.

-   **[Change request creation with errors in DevOps data retrieval for Harness pipelines](https://www.servicenow.com/docs/access?context=change-request-creation-with-devops-data-retrieval-errors&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Enable change request creation even if there is an error in retrieving the DevOps data for a Harness pipeline.

-   **[Branch name filter](https://www.servicenow.com/docs/access?context=create-devops-change-request-manual&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Search for build numbers by the branch name while associating DevOps data to a change request in the Service Operations Workspace \(SOW\) or Classic UI.

-   **[Test summary name in GitHub Actions](https://www.servicenow.com/docs/access?context=servicenow-devops-custom-actions-from-github-marketplace&version=yokohama&pubname=yokohama-it-service-management&section=servicenow-devops-test-report-custom-action&ft:locale=en-US)**

    The servicenow-devops-test-report custom action in GitHub now includes an optional test-summary-name parameter to specify the test summary results name.

-   **[Token based authentication for Rally](https://www.servicenow.com/docs/access?context=configure-webhooks-for-rally-manually&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Configure webhooks for Rally using token based authentication instead of using the integration username and password.

-   **[Renamed variables for Docker](https://www.servicenow.com/docs/access?context=servicenow-custom-actions-for-gitlab&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    The environmental variables in the Generic Docker actions for DevOps Change Velocity have been renamed by removing the CI prefix for better clarity.

-   **[Security scan results](https://www.servicenow.com/docs/access?context=dev-ops-change-acceleration&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Security scan results on the change record associated to a pipeline execution with a linked package are now displayed in the **Security Summaries** tab.

-   **[Source of commits in SOW](https://www.servicenow.com/docs/access?context=create-change-sow&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    View the source of commits like pipeline execution, branch, repository, and so on for a change request in the DevOps data section of the Service Operations Workspace.

-   **[Track file changes](https://www.servicenow.com/docs/access?context=sc-github&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    The **Track file changes** option is now disabled by default when a repository is configured to prevent any potential security risks.

-   **[Close code value for a change request](https://www.servicenow.com/docs/access?context=dev-ops-administration&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Two new properties have been added in DevOps Change Velocity, so that you can specify a close code value for a change request based on the change request completion state when the autoCloseChange parameter is enabled.

-   **[Support for MID Server cluster](https://www.servicenow.com/docs/access?context=playbook-enter-github-instance-details&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Improve load balancing and failover protection by selecting a MID Server cluster when connecting to a tool instance associated with a MID Server cluster. This configuration enables multiple MID Servers with relevant capabilities to be grouped.

-   **[Improved UX for DevOps Change health scans](https://www.servicenow.com/docs/access?context=run-health-scan-check&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Run health scans and analyze findings efficiently in the DevOps Change workspace with an intuitive and user-friendly interface.

-   **[Pipeline association for GitHub Actions](https://www.servicenow.com/docs/access?context=sc-github&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    When onboarding GitHub Actions pipelines through the App onboarding catalog or the onboarding APIs, now only the selected pipelines are associated with the DevOps app. If no pipeline is selected, all pipelines within the specified repository are associated.

-   **[Tool connection check status](https://www.servicenow.com/docs/access?context=devops-reference-error-messages&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    If a tool is marked as Disconnected because of a system-generated failure during an unsuccessful connection check, any subsequent successful check automatically updates the connection status to Connected. If you manually disconnect the tool, the tool status remains Disconnected even if there’s a subsequent successful connection check.

-   **[New roles for vulnerability integration](https://www.servicenow.com/docs/access?context=installed-with-dev-ops&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**
    -   The sn\_vul.app\_sec\_manager role is added to the DevOps Tool Owner \[sn\_devops.tool\_owner\] role when the DevOps Vulnerability Integrations plugin \(sn\_devops\_vul\_ints\) is installed.
    -   The sn\_vul\_veracode.configure\_integration role is added to the DevOps Tool Owner \[sn\_devops.tool\_owner\] role when the Vulnerability Response Integration with Veracode plugin \(sn\_vul\_veracode\) is installed.
-   **[Prod deploy commit logic for other step types](https://www.servicenow.com/docs/access?context=dev-ops-commits-release&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Update the **sn\_devops.commit\_rel\_change\_step\_type** property to have other step types, like Test or Deploy, use the same commit logic as Prod Deploy.

-   **[Override start and end time of a change request](https://www.servicenow.com/docs/access?context=dev-ops-config-change-details&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Set the  **sn\_devops.change\_request.auto\_close\_allow\_override\_start\_time ** and  **sn\_devops.change\_request.auto\_close\_allow\_override\_end\_time ** properties as false to consider the change request start and end time instead of the pipeline’s when the  autoCloseChange  parameter is enabled in a pipeline.

-   **[Node version of DevOps extension](https://www.servicenow.com/docs/access?context=config-dev-ops-extensions-azure&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    The node version of the ServiceNow DevOps  extension has been upgraded to version 20.x in Azure DevOps.

-   **[Enhanced pipeline governance in GitLab](https://www.servicenow.com/docs/access?context=servicenow-custom-actions-for-gitlab&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    View change request details like status, sys\_id, priority in the GitLab console when a change request is created in GitLab using Docker image.

-   **[Health scan enhancements](https://www.servicenow.com/docs/access?context=run-health-scan-check&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**
    -   Identify outdated or prolonged discover and import requests using the DevOps -Stale or Long-Running Discover and Import Requests health check.
    -   Verify whether webhooks have been configured correctly for any tracked repository, pipeline, or plan in  GitHub,  GitLab,  Azure DevOps, and  Jenkins using the DevOps webhook configuration analysis health check.
    -   Identify OAuth app configuration issues for GitHub tools in the connected state using the DevOps webhook configuration analysis health check.
    -   Verify if any scheduled job has been configured to run as an invalid or non-admin user.
    -   Navigate to the Findings list from the DevOps Change Workspace home page by selecting  **View all findings ** in the  Health scan findings  widget. 
-   **[Enhanced JFrog integration with DevOps Change Velocity](https://www.servicenow.com/docs/access?context=devops-jfrog-connect-workspace&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Gather JFrog evidence seamlessly and create change records automatically using the improved JFrog integration with DevOps Change Velocity.

-   **[Bearer authentication in JFrog](https://www.servicenow.com/docs/access?context=devops-jfrog-connect-workspace&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Connect to JFrog using the secure bearer token authentication to comply with JFrog’s updated security policies.

-   **[HTTP proxy for Docker](https://www.servicenow.com/docs/access?context=servicenow-custom-actions-for-gitlab&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Connect to DevOps Change Velocity through HTTP proxy settings using environment variables in your Docker deployment for instances that run a proxy server.

-   **[Health scan enhancements](https://www.servicenow.com/docs/access?context=run-health-scan-check&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**
    -   Identify any callback processing issues in your instance.
    -   Identify any access control rule \(ACL\) that is incorrectly associated with a role in your instance.
    -   Verify whether all DevOps tables are present in your instance and confirm whether all metadata in sys\_\* tables is present.
    -   Verify whether all DevOps roles in your instance contain all expected roles, including inherited roles.
-   **[Auto close without Change Management - State Model \[Legacy\] plugin](https://www.servicenow.com/docs/access?context=dev-ops-change-acceleration&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Change requests can now be auto-closed without requiring you to install the Change Management - State Model \[Legacy\] plugin.


## Activation information

Activate DevOps Change Velocity by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Performance Analytics](https://www.servicenow.com/docs/access?context=pa-overview&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

    ServiceNow® Performance Analytics is an in-platform process optimization solution to create management dashboards, report on KPIs and metrics, and answer key business questions. The application helps improve quality and reduces the costs of service delivery.

-   **[Change Management](https://www.servicenow.com/docs/access?context=c_ITILChangeManagement&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    The ServiceNow® Change Management application provides a systematic approach to control the life cycle of all changes, facilitating beneficial changes to be made with minimum disruption to IT services.

-   **Agile Development**

    The ServiceNow® Agile Development application helps you deliver software projects more efficiently by managing and tracking software development life cycles using an iterative, incremental, and flexible approach.

-   **[Risk Management](https://www.servicenow.com/docs/access?context=grc-risk-overview&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    The ServiceNow® Governance, Risk, and Compliance Risk Management application helps you continuously monitor and identify high-impact risks, improve your risk-based decision-making, and reduce reaction time effectively. The application also provides structured workflows for the management of risk assessments, risk indicators, and risk issues.


**Parent Topic:**[IT Service Management release notes](../it-service-management/it-service-management-rn-landing.md)

