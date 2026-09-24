---
title: Combined DevOps Change Velocity release notes for upgrades from Zurich to Brazil
description: Consolidated page of all release notes for DevOps Change Velocity from Zurich to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-brazil/brazil-zurich-devopschangevelocity-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 10
breadcrumb: [Products combined by family]
---

# Combined DevOps Change Velocity release notes for upgrades from Zurich to Brazil

Consolidated page of all release notes for DevOps Change Velocity from Zurich to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family DevOps Change Velocity release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading DevOps Change Velocity to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for DevOps Change Velocity.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Rally authentication with OAuth 2.0](https://www.servicenow.com/docs/access?context=setting-up-rally-oauth-2-0-credentials-for-devops&family=zurich&ft:locale=en-US)**

Authenticate a Rally tool connection using OAuth 2.0 credentials to strengthen your tool security.

-   **[GitHub Data Residency support](https://www.servicenow.com/docs/access?context=playbook-enter-github-instance-details&family=zurich&ft:locale=en-US)**

Connect to GitHub Enterprise Server with data residency controls to keep your organization's code and data in your preferred geographic location.


 -   **[Import based evidence collection](https://www.servicenow.com/docs/access?context=import-based-evidence-collection-for-orchestration-capability&family=zurich&ft:locale=en-US)**

Improve instance efficiency by skipping step-level pipeline processing for accelerated change management and evidence collection for GitHub Actions, Azure DevOps \(ADO\), GitLab and  Jenkins orchestration tools.


</td></tr><tr><td>

Australia

</td><td>

-   **[Rally authentication with OAuth 2.0](https://www.servicenow.com/docs/access?context=setting-up-rally-oauth-2-0-credentials-for-devops&family=australia&ft:locale=en-US)**

Authenticate a Rally tool connection using OAuth 2.0 credentials to strengthen your tool security.

-   **[GitHub Data Residency support](https://www.servicenow.com/docs/access?context=playbook-enter-github-instance-details&family=australia&ft:locale=en-US)**

Connect to GitHub Enterprise Server with data residency controls to keep your organization's code and data in your preferred geographic location.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Rally authentication with OAuth 2.0](https://www.servicenow.com/docs/access?context=setting-up-rally-oauth-2-0-credentials-for-devops&family=brazil&ft:locale=en-US)**

Authenticate a Rally tool connection using OAuth 2.0 credentials to strengthen your tool security.

-   **[GitHub Data Residency support](https://www.servicenow.com/docs/access?context=playbook-enter-github-instance-details&family=brazil&ft:locale=en-US)**

Connect to GitHub Enterprise Server with data residency controls to keep your organization's code and data in your preferred geographic location.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing DevOps Change Velocity features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Jira authentication with 3LO](https://www.servicenow.com/docs/access?context=connect-a-jira-tool-using-oauth-2-0-with-3lo&family=zurich&ft:locale=en-US)**

Authenticate a Jira tool connection using OAuth 2.0 with three-legged OAuth \(3LO\) to enable secure, delegated access to your Jira account.

-   **[Bitbucket Cloud basic authentication using API token with scopes](https://www.servicenow.com/docs/access?context=bitbucket-integration-dev-ops&family=zurich&ft:locale=en-US)**

Connect to Bitbucket Cloud using Basic Auth by providing the email address and API token with the required scopes for your Bitbucket Cloud account as app password has been deprecated by Bitbucket.


 -   **[Enhanced JFrog integration with DevOps Change Velocity](https://www.servicenow.com/docs/access?context=devops-jfrog-connect-workspace&family=zurich&ft:locale=en-US)**

Gather JFrog evidence seamlessly and create change records automatically using the improved JFrog integration with DevOps Change Velocity.

-   **[Bearer authentication in JFrog](https://www.servicenow.com/docs/access?context=devops-jfrog-connect-workspace&family=zurich&ft:locale=en-US)**

Connect to JFrog using the secure bearer token authentication to comply with JFrog’s updated security policies.

-   **[HTTP proxy for Docker](https://www.servicenow.com/docs/access?context=servicenow-custom-actions-for-gitlab&family=zurich&ft:locale=en-US)**

Connect to DevOps Change Velocity through HTTP proxy settings using environment variables in your Docker deployment for instances that run a proxy server.

-   **[Health scan enhancements](https://www.servicenow.com/docs/access?context=run-health-scan-check&family=zurich&ft:locale=en-US)**
    -   Identify any callback processing issues in your instance.
    -   Identify any access control rule \(ACL\) that is incorrectly associated with a role in your instance.
    -   Verify whether all DevOps tables are present in your instance and confirm whether all metadata in sys\_\* tables is present.
    -   Verify whether all DevOps roles in your instance contain all expected roles, including inherited roles.
-   **[Auto close without Change Management - State Model \[Legacy\] plugin](https://www.servicenow.com/docs/access?context=dev-ops-change-acceleration&family=zurich&ft:locale=en-US)**

Change requests can now be auto-closed without requiring you to install the Change Management - State Model \[Legacy\] plugin.


 -   **[Prod deploy commit logic for other step types](https://www.servicenow.com/docs/access?context=dev-ops-commits-release&family=zurich&ft:locale=en-US)**

Update the **sn\_devops.commit\_rel\_change\_step\_type** property to have other step types, like Test or Deploy, use the same commit logic as Prod Deploy.

-   **[Override start and end time of a change request](https://www.servicenow.com/docs/access?context=dev-ops-config-change-details&family=zurich&ft:locale=en-US)**

Set the  **sn\_devops.change\_request.auto\_close\_allow\_override\_start\_time ** and  **sn\_devops.change\_request.auto\_close\_allow\_override\_end\_time ** properties as false to consider the change request start and end time instead of the pipeline’s when the  autoCloseChange  parameter is enabled in a pipeline.

-   **[Node version of DevOps extension](https://www.servicenow.com/docs/access?context=config-dev-ops-extensions-azure&family=zurich&ft:locale=en-US)**

The node version of the ServiceNow DevOps  extension has been upgraded to version 20.x in Azure DevOps.

-   **[Enhanced pipeline governance in GitLab](https://www.servicenow.com/docs/access?context=servicenow-custom-actions-for-gitlab&family=zurich&ft:locale=en-US)**

View change request details like status, sys\_id, priority in the GitLab console when a change request is created in GitLab using Docker image.

-   **[Health scan enhancements](https://www.servicenow.com/docs/access?context=run-health-scan-check&family=zurich&ft:locale=en-US)**
    -   Identify outdated or prolonged discover and import requests using the DevOps -Stale or Long-Running Discover and Import Requests health check.
    -   Verify whether webhooks have been configured correctly for any tracked repository, pipeline, or plan in  GitHub,  GitLab,  Azure DevOps, and  Jenkins using the DevOps webhook configuration analysis health check.
    -   Identify OAuth app configuration issues for GitHub tools in the connected state using the DevOps webhook configuration analysis health check.
    -   Verify if any scheduled job has been configured to run as an invalid or non-admin user.
    -   Navigate to the Findings list from the DevOps Change Workspace home page by selecting  **View all findings ** in the  Health scan findings  widget. 

 -   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


 -   **[Support for MID Server cluster](https://www.servicenow.com/docs/access?context=playbook-enter-github-instance-details&family=zurich&ft:locale=en-US)**

Improve load balancing and failover protection by selecting a MID Server cluster when connecting to a tool instance associated with a MID Server cluster. This configuration enables multiple MID Servers with relevant capabilities to be grouped.

-   **[Improved UX for DevOps Change health scans](https://www.servicenow.com/docs/access?context=run-health-scan-check&family=zurich&ft:locale=en-US)**

Run health scans and analyze findings efficiently in the DevOps Change workspace with an intuitive and user-friendly interface.

-   **[Pipeline association for GitHub Actions](https://www.servicenow.com/docs/access?context=sc-github&family=zurich&ft:locale=en-US)**

When onboarding GitHub Actions pipelines through the App onboarding catalog or the onboarding APIs, now only the selected pipelines are associated with the DevOps app. If no pipeline is selected, all pipelines within the specified repository are associated.

-   **[Tool connection check status](https://www.servicenow.com/docs/access?context=devops-reference-error-messages&family=zurich&ft:locale=en-US)**

If a tool is marked as Disconnected because of a system-generated failure during an unsuccessful connection check, any subsequent successful check automatically updates the connection status to Connected. If you manually disconnect the tool, the tool status remains Disconnected even if there’s a subsequent successful connection check.

-   **[New roles for vulnerability integration](https://www.servicenow.com/docs/access?context=installed-with-dev-ops&family=zurich&ft:locale=en-US)**
    -   The sn\_vul.app\_sec\_manager role is added to the DevOps Tool Owner \[sn\_devops.tool\_owner\] role when the DevOps Vulnerability Integrations plugin \(sn\_devops\_vul\_ints\) is installed.
    -   The sn\_vul\_veracode.configure\_integration role is added to the DevOps Tool Owner \[sn\_devops.tool\_owner\] role when the Vulnerability Response Integration with Veracode plugin \(sn\_vul\_veracode\) is installed.

</td></tr><tr><td>

Australia

</td><td>

-   **[Jira authentication with 3LO](https://www.servicenow.com/docs/access?context=connect-a-jira-tool-using-oauth-2-0-with-3lo&family=australia&ft:locale=en-US)**

Authenticate a Jira tool connection using OAuth 2.0 with three-legged OAuth \(3LO\) to enable secure, delegated access to your Jira account.

-   **[Bitbucket Cloud basic authentication using API token with scopes](https://www.servicenow.com/docs/access?context=bitbucket-integration-dev-ops&family=australia&ft:locale=en-US)**

Connect to Bitbucket Cloud using Basic Auth by providing the email address and API token with the required scopes for your Bitbucket Cloud account as app password has been deprecated by Bitbucket.


 -   **[Enhanced JFrog integration with DevOps Change Velocity](https://www.servicenow.com/docs/access?context=devops-jfrog-connect-workspace&family=australia&ft:locale=en-US)**

Gather JFrog evidence seamlessly and create change records automatically using the improved JFrog integration with DevOps Change Velocity.

-   **[Bearer authentication in JFrog](https://www.servicenow.com/docs/access?context=devops-jfrog-connect-workspace&family=australia&ft:locale=en-US)**

Connect to JFrog using the secure bearer token authentication to comply with JFrog’s updated security policies.

-   **[HTTP proxy for Docker](https://www.servicenow.com/docs/access?context=servicenow-custom-actions-for-gitlab&family=australia&ft:locale=en-US)**

Connect to DevOps Change Velocity through HTTP proxy settings using environment variables in your Docker deployment for instances that run a proxy server.

-   **[Health scan enhancements](https://www.servicenow.com/docs/access?context=run-health-scan-check&family=australia&ft:locale=en-US)**
    -   Identify any callback processing issues in your instance.
    -   Identify any access control rule \(ACL\) that is incorrectly associated with a role in your instance.
    -   Verify whether all DevOps tables are present in your instance and confirm whether all metadata in sys\_\* tables is present.
    -   Verify whether all DevOps roles in your instance contain all expected roles, including inherited roles.
-   **[Auto close without Change Management - State Model \[Legacy\] plugin](https://www.servicenow.com/docs/access?context=dev-ops-change-acceleration&family=australia&ft:locale=en-US)**

Change requests can now be auto-closed without requiring you to install the Change Management - State Model \[Legacy\] plugin.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some DevOps Change Velocity features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some DevOps Change Velocity features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Zurich

</td><td>

-   **Activation information**

Install DevOps Change Velocity by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


**Important:** DevOps Change Velocity is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install DevOps Change Velocity by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


**Important:** DevOps Change Velocity is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Install DevOps Change Velocity by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=brazil&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for DevOps Change Velocity we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Zurich

</td><td>

-   **Accessibility information**
    -   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for DevOps Change Velocity we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Zurich

</td><td>

-   Improve visibility into your DevOps data in a single system.
-   Automate the change workflow and approval decisions to increase change velocity while ensuring governance and control.
-   Track the progress of your work items, commits, artifacts, builds, and releases using the change requests to lend additional transparency and provide a single source of truth to all the personas involved.

 See [DevOps Change Velocity](https://www.servicenow.com/docs/access?context=devops-landing-page-new&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Improve visibility into your DevOps data in a single system.
-   Automate the change workflow and approval decisions to increase change velocity while ensuring governance and control.
-   Track the progress of your work items, commits, artifacts, builds, and releases using the change requests to lend additional transparency and provide a single source of truth to all the personas involved.

 See [DevOps Change Velocity](https://www.servicenow.com/docs/access?context=devops-landing-page-new&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

-   Improve visibility into your DevOps data in a single system.
-   Automate the change workflow and approval decisions to increase change velocity while ensuring governance and control.
-   Track the progress of your work items, commits, artifacts, builds, and releases using the change requests to lend additional transparency and provide a single source of truth to all the personas involved.

 See [DevOps Change Velocity](https://www.servicenow.com/docs/access?context=devops-landing-page-new&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-zurich-brazil/rn-combined-intro.md)

