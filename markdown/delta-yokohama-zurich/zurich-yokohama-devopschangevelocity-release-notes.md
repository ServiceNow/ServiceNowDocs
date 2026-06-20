---
title: Combined DevOps Change Velocity release notes for upgrades from Yokohama to Zurich
description: Consolidated page of all release notes for DevOps Change Velocity from Yokohama to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-yokohama-zurich/zurich-yokohama-devopschangevelocity-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 10
breadcrumb: [Products combined by family]
---

# Combined DevOps Change Velocity release notes for upgrades from Yokohama to Zurich

Consolidated page of all release notes for DevOps Change Velocity from Yokohama to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family DevOps Change Velocity release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading DevOps Change Velocity to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

If you are a new customer or are using a zBoot instance and you want to create type-based workflow change requests in DevOps Change Velocity, you must add the**com.snc.change\_management.change\_model.type\_compatibility** property and set it to True. For more information, see [Add a system property](https://servicenow-staging.fluidtopics.net/access?context=t_AddAPropertyUsingSysPropsList&family=yokohama&ft:locale=en-US).

 If you are an upgrading customer, you must run the **ReConfigure Bitbucket Server Repositories for PullRequest** job to re-configure your existing Bitbucket Server or Bitbucket Data Center repositories so that pull request records can be imported. You can navigate to **All &gt; System Definition &gt; Scheduled Jobs** to search for this job and run it.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for DevOps Change Velocity.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Harness integration](https://servicenow-staging.fluidtopics.net/access?context=harness-integration-with-devops-change-velocity&family=yokohama&ft:locale=en-US)**

Discover Harness pipelines and configure real-time notifications to enable change traceability and automation by integrating the Harness orchestration tool with DevOps Change Velocity.

-   **[DevOps Health instance scan](https://servicenow-staging.fluidtopics.net/access?context=run-health-scan-check&family=yokohama&ft:locale=en-US)**

Detect anomalies and issues in the instance by running or scheduling health scans on your DevOps Change Velocity instance.

-   **[Bitbucket Cloud tool integration with ServiceNow](https://servicenow-staging.fluidtopics.net/access?context=bitbucket-integration-dev-ops&family=yokohama&ft:locale=en-US)**

Integrate the Bitbucket Cloud coding tool with DevOps Change Velocity to connect, discover, import, and process real-time repository events in DevOps Change Velocity.

-   **[DevOps Change Workspace UI for simplified creation of custom tool integration with planning, coding and orchestration capabilities](https://servicenow-staging.fluidtopics.net/access?context=create-a-tool-integration-from-the-devops-change-workspace&family=yokohama&ft:locale=en-US)**

Integrate a new custom tool across planning, coding and orchestration capabilities with basic know-how of ServiceNow using an intuitive DevOps Change Workspace UI. It offers easy navigation to the ServiceNow Platform for defining transformer or adapter rules, or integrate the ability to do so within the Workspace wherever applicable, and embeds necessary documentation links and tooltips to support self-service.

-   **[Import based evidence collection](https://servicenow-staging.fluidtopics.net/access?context=import-based-evidence-collection-for-orchestration-capability&family=yokohama&ft:locale=en-US)**

Improve instance efficiency by skipping step-level pipeline processing for accelerated change management and evidence collection for GitHub Actions, Azure DevOps \(ADO\), GitLab and  Jenkins orchestration tools.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Import based evidence collection](https://servicenow-staging.fluidtopics.net/access?context=import-based-evidence-collection-for-orchestration-capability&family=zurich&ft:locale=en-US)**

Improve instance efficiency by skipping step-level pipeline processing for accelerated change management and evidence collection for GitHub Actions, Azure DevOps \(ADO\), GitLab and  Jenkins orchestration tools.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing DevOps Change Velocity features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Simplified onboarding of orchestration tools not supported in the base system](https://servicenow-staging.fluidtopics.net/access?context=devops-user-created-orchestration-tool-integration&family=yokohama&ft:locale=en-US)**

Integrate orchestration tools that aren’t supported in the base system by leveraging a generic framework.

-   **[Custom fields for planning tool integration](https://servicenow-staging.fluidtopics.net/access?context=add-custom-field-for-a-planning-tool-integration&family=yokohama&ft:locale=en-US)**

Add custom fields into your planning tool integration to improve configurability and access business-specific information, which facilitates more informed decision-making.

-   **[Additional scans for DevOps Health Scan Content pack](https://servicenow-staging.fluidtopics.net/access?context=run-health-scan-check&family=yokohama&ft:locale=en-US)**

Additional set of proactive checks focused on problems that tend to occur before or after an upgrade along with identifying configuration issues like plugin and version incompatibilities, or pipelines that chronically fail, have been added.

-   **[Import pull-request records for Bitbucket Server or Bitbucket Data Center](https://servicenow-staging.fluidtopics.net/access?context=devops-wkspc-bitbucket-tool-conn&family=yokohama&ft:locale=en-US)**

Import pull-request records for Bitbucket Server or Data Center for improved insights and efficiency.

-   **[Change request creation with errors in DevOps data retrieval for Harness pipelines](https://servicenow-staging.fluidtopics.net/access?context=change-request-creation-with-devops-data-retrieval-errors&family=yokohama&ft:locale=en-US)**

Enable change request creation even if there is an error in retrieving the DevOps data for a Harness pipeline.

-   **[Branch name filter](https://servicenow-staging.fluidtopics.net/access?context=create-devops-change-request-manual&family=yokohama&ft:locale=en-US)**

Search for build numbers by the branch name while associating DevOps data to a change request in the Service Operations Workspace \(SOW\) or Classic UI.

-   **[Test summary name in GitHub Actions](https://servicenow-staging.fluidtopics.net/access?context=servicenow-devops-test-report-custom-action&family=yokohama&ft:locale=en-US)**

The servicenow-devops-test-report custom action in GitHub now includes an optional test-summary-name parameter to specify the test summary results name.

-   **[Token based authentication for Rally](https://servicenow-staging.fluidtopics.net/access?context=configure-webhooks-for-rally-manually&family=yokohama&ft:locale=en-US)**

Configure webhooks for Rally using token based authentication instead of using the integration username and password.

-   **[Renamed variables for Docker](https://servicenow-staging.fluidtopics.net/access?context=servicenow-custom-actions-for-gitlab&family=yokohama&ft:locale=en-US)**

The environmental variables in the Generic Docker actions for DevOps Change Velocity have been renamed by removing the CI prefix for better clarity.

-   **[Security scan results](https://servicenow-staging.fluidtopics.net/access?context=dev-ops-change-acceleration&family=yokohama&ft:locale=en-US)**

Security scan results on the change record associated to a pipeline execution with a linked package are now displayed in the **Security Summaries** tab.

-   **[Source of commits in SOW](https://servicenow-staging.fluidtopics.net/access?context=create-change-sow&family=yokohama&ft:locale=en-US)**

View the source of commits like pipeline execution, branch, repository, and so on for a change request in the DevOps data section of the Service Operations Workspace.

-   **[Track file changes](https://servicenow-staging.fluidtopics.net/access?context=sc-github&family=yokohama&ft:locale=en-US)**

The **Track file changes** option is now disabled by default when a repository is configured to prevent any potential security risks.

-   **[Close code value for a change request](https://servicenow-staging.fluidtopics.net/access?context=dev-ops-administration&family=yokohama&ft:locale=en-US)**

Two new properties have been added in DevOps Change Velocity, so that you can specify a close code value for a change request based on the change request completion state when the autoCloseChange parameter is enabled.

-   **[Support for MID Server cluster](https://servicenow-staging.fluidtopics.net/access?context=playbook-enter-github-instance-details&family=yokohama&ft:locale=en-US)**

Improve load balancing and failover protection by selecting a MID Server cluster when connecting to a tool instance associated with a MID Server cluster. This configuration enables multiple MID Servers with relevant capabilities to be grouped.

-   **[Improved UX for DevOps Change health scans](https://servicenow-staging.fluidtopics.net/access?context=run-health-scan-check&family=yokohama&ft:locale=en-US)**

Run health scans and analyze findings efficiently in the DevOps Change workspace with an intuitive and user-friendly interface.

-   **[Pipeline association for GitHub Actions](https://servicenow-staging.fluidtopics.net/access?context=sc-github&family=yokohama&ft:locale=en-US)**

When onboarding GitHub Actions pipelines through the App onboarding catalog or the onboarding APIs, now only the selected pipelines are associated with the DevOps app. If no pipeline is selected, all pipelines within the specified repository are associated.

-   **[Tool connection check status](https://servicenow-staging.fluidtopics.net/access?context=devops-reference-error-messages&family=yokohama&ft:locale=en-US)**

If a tool is marked as Disconnected because of a system-generated failure during an unsuccessful connection check, any subsequent successful check automatically updates the connection status to Connected. If you manually disconnect the tool, the tool status remains Disconnected even if there’s a subsequent successful connection check.

-   **[New roles for vulnerability integration](https://servicenow-staging.fluidtopics.net/access?context=installed-with-dev-ops&family=yokohama&ft:locale=en-US)**
    -   The sn\_vul.app\_sec\_manager role is added to the DevOps Tool Owner \[sn\_devops.tool\_owner\] role when the DevOps Vulnerability Integrations plugin \(sn\_devops\_vul\_ints\) is installed.
    -   The sn\_vul\_veracode.configure\_integration role is added to the DevOps Tool Owner \[sn\_devops.tool\_owner\] role when the Vulnerability Response Integration with Veracode plugin \(sn\_vul\_veracode\) is installed.
-   **[Prod deploy commit logic for other step types](https://servicenow-staging.fluidtopics.net/access?context=dev-ops-commits-release&family=yokohama&ft:locale=en-US)**

Update the **sn\_devops.commit\_rel\_change\_step\_type** property to have other step types, like Test or Deploy, use the same commit logic as Prod Deploy.

-   **[Override start and end time of a change request](https://servicenow-staging.fluidtopics.net/access?context=dev-ops-config-change-details&family=yokohama&ft:locale=en-US)**

Set the  **sn\_devops.change\_request.auto\_close\_allow\_override\_start\_time ** and  **sn\_devops.change\_request.auto\_close\_allow\_override\_end\_time ** properties as false to consider the change request start and end time instead of the pipeline’s when the  autoCloseChange  parameter is enabled in a pipeline.

-   **[Node version of DevOps extension](https://servicenow-staging.fluidtopics.net/access?context=config-dev-ops-extensions-azure&family=yokohama&ft:locale=en-US)**

The node version of the ServiceNow DevOps  extension has been upgraded to version 20.x in Azure DevOps.

-   **[Enhanced pipeline governance in GitLab](https://servicenow-staging.fluidtopics.net/access?context=servicenow-custom-actions-for-gitlab&family=yokohama&ft:locale=en-US)**

View change request details like status, sys\_id, priority in the GitLab console when a change request is created in GitLab using Docker image.

-   **[Health scan enhancements](https://servicenow-staging.fluidtopics.net/access?context=run-health-scan-check&family=yokohama&ft:locale=en-US)**
    -   Identify outdated or prolonged discover and import requests using the DevOps -Stale or Long-Running Discover and Import Requests health check.
    -   Verify whether webhooks have been configured correctly for any tracked repository, pipeline, or plan in  GitHub,  GitLab,  Azure DevOps, and  Jenkins using the DevOps webhook configuration analysis health check.
    -   Identify OAuth app configuration issues for GitHub tools in the connected state using the DevOps webhook configuration analysis health check.
    -   Verify if any scheduled job has been configured to run as an invalid or non-admin user.
    -   Navigate to the Findings list from the DevOps Change Workspace home page by selecting  **View all findings ** in the  Health scan findings  widget. 

</td></tr><tr><td>

Zurich

</td><td>

-   **[Support for MID Server cluster](https://servicenow-staging.fluidtopics.net/access?context=playbook-enter-github-instance-details&family=zurich&ft:locale=en-US)**

Improve load balancing and failover protection by selecting a MID Server cluster when connecting to a tool instance associated with a MID Server cluster. This configuration enables multiple MID Servers with relevant capabilities to be grouped.

-   **[Improved UX for DevOps Change health scans](https://servicenow-staging.fluidtopics.net/access?context=run-health-scan-check&family=zurich&ft:locale=en-US)**

Run health scans and analyze findings efficiently in the DevOps Change workspace with an intuitive and user-friendly interface.

-   **[Pipeline association for GitHub Actions](https://servicenow-staging.fluidtopics.net/access?context=sc-github&family=zurich&ft:locale=en-US)**

When onboarding GitHub Actions pipelines through the App onboarding catalog or the onboarding APIs, now only the selected pipelines are associated with the DevOps app. If no pipeline is selected, all pipelines within the specified repository are associated.

-   **[Tool connection check status](https://servicenow-staging.fluidtopics.net/access?context=devops-reference-error-messages&family=zurich&ft:locale=en-US)**

If a tool is marked as Disconnected because of a system-generated failure during an unsuccessful connection check, any subsequent successful check automatically updates the connection status to Connected. If you manually disconnect the tool, the tool status remains Disconnected even if there’s a subsequent successful connection check.

-   **[New roles for vulnerability integration](https://servicenow-staging.fluidtopics.net/access?context=installed-with-dev-ops&family=zurich&ft:locale=en-US)**
    -   The sn\_vul.app\_sec\_manager role is added to the DevOps Tool Owner \[sn\_devops.tool\_owner\] role when the DevOps Vulnerability Integrations plugin \(sn\_devops\_vul\_ints\) is installed.
    -   The sn\_vul\_veracode.configure\_integration role is added to the DevOps Tool Owner \[sn\_devops.tool\_owner\] role when the Vulnerability Response Integration with Veracode plugin \(sn\_vul\_veracode\) is installed.
-   **[Prod deploy commit logic for other step types](https://servicenow-staging.fluidtopics.net/access?context=dev-ops-commits-release&family=zurich&ft:locale=en-US)**

Update the **sn\_devops.commit\_rel\_change\_step\_type** property to have other step types, like Test or Deploy, use the same commit logic as Prod Deploy.

-   **[Override start and end time of a change request](https://servicenow-staging.fluidtopics.net/access?context=dev-ops-config-change-details&family=zurich&ft:locale=en-US)**

Set the  **sn\_devops.change\_request.auto\_close\_allow\_override\_start\_time ** and  **sn\_devops.change\_request.auto\_close\_allow\_override\_end\_time ** properties as false to consider the change request start and end time instead of the pipeline’s when the  autoCloseChange  parameter is enabled in a pipeline.

-   **[Node version of DevOps extension](https://servicenow-staging.fluidtopics.net/access?context=config-dev-ops-extensions-azure&family=zurich&ft:locale=en-US)**

The node version of the ServiceNow DevOps  extension has been upgraded to version 20.x in Azure DevOps.

-   **[Enhanced pipeline governance in GitLab](https://servicenow-staging.fluidtopics.net/access?context=servicenow-custom-actions-for-gitlab&family=zurich&ft:locale=en-US)**

View change request details like status, sys\_id, priority in the GitLab console when a change request is created in GitLab using Docker image.

-   **[Health scan enhancements](https://servicenow-staging.fluidtopics.net/access?context=run-health-scan-check&family=zurich&ft:locale=en-US)**
    -   Identify outdated or prolonged discover and import requests using the DevOps -Stale or Long-Running Discover and Import Requests health check.
    -   Verify whether webhooks have been configured correctly for any tracked repository, pipeline, or plan in  GitHub,  GitLab,  Azure DevOps, and  Jenkins using the DevOps webhook configuration analysis health check.
    -   Identify OAuth app configuration issues for GitHub tools in the connected state using the DevOps webhook configuration analysis health check.
    -   Verify if any scheduled job has been configured to run as an invalid or non-admin user.
    -   Navigate to the Findings list from the DevOps Change Workspace home page by selecting  **View all findings ** in the  Health scan findings  widget. 

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some DevOps Change Velocity features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some DevOps Change Velocity features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate DevOps Change Velocity.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Activate DevOps Change Velocity by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install DevOps Change Velocity by requesting it from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for DevOps Change Velocity we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for DevOps Change Velocity we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for DevOps Change Velocity, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   ****

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for DevOps Change Velocity we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for DevOps Change Velocity we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   Integrate with the Harness orchestration tool to discover Harness pipelines and enable change automation.
-   Detect anomalies and issues in your DevOps Change Velocity instance using health scans.

 See [DevOps Change Velocity](https://servicenow-staging.fluidtopics.net/access?context=devops-landing-page-new&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Improve instance efficiency by skipping step-level pipeline processing.
-   Improve load balancing and failover protection by selecting a MID Server cluster during tool connection.

 See [DevOps Change Velocity](https://servicenow-staging.fluidtopics.net/access?context=devops-landing-page-new&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-yokohama-zurich/rn-combined-intro.md)

