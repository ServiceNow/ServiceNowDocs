---
title: DevOps Change Velocity release notes
description: The ServiceNow DevOps Change Velocity application improves visibility into your DevOps data in a single system, automates and accelerates change processes, and helps you gain insights to measure the performance of your DevOps environment. DevOps Change Velocity was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 8
---

# DevOps Change Velocity release notes

The ServiceNow® DevOps Change Velocity application improves visibility into your DevOps data in a single system, automates and accelerates change processes, and helps you gain insights to measure the performance of your DevOps environment. DevOps Change Velocity was enhanced and updated in the Xanadu release.

## DevOps Change Velocity highlights for the Xanadu release

-   Leverage DevOps data for change automation by configuring Change Management features from the Service Operations Workspace Admin Center.
-   Benefit from accessibility improvements to create a configurable workspace that supports Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA conformance.

See [DevOps Change Velocity](https://www.servicenow.com/docs/access?context=devops-landing-page-new&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US) for more information.

## Important information for upgrading DevOps Change Velocity to Xanadu

If you are an upgrading customer, you must run the **ReConfigure Bitbucket Server Repositories for PullRequest** job to re-configure your existing Bitbucket Server or Bitbucket Data Center repositories so that pull request records can be imported. You can navigate to **All &gt; System Definition &gt; Scheduled Jobs** to search for this job and run it.

**Important:** DevOps Change Velocity is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Xanadu release

-   **[Change Management in SOW Admin Center](https://www.servicenow.com/docs/access?context=manage-admin-console-sow-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Configure Change Management features from the Service Operations Workspace Admin Center to increase change efficiency, accelerate change approvals, drive data-driven risk analysis, and leverage DevOps data for change automation.

-   **[OAuth 2.0 authentication for Azure DevOps \(ADO\)](https://www.servicenow.com/docs/access?context=set-up-azure-devops-oauth-2-0-credential&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Use OAuth 2.0 authentication to connect your Azure DevOps tool with DevOps Change Velocity ensuring a more secure authentication method.

-   **[OAuth 2.0 authentication for Jira Cloud](https://www.servicenow.com/docs/access?context=create-jira-tool-dev-ops&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Use OAuth 2.0 authentication to connect your Jira Cloud tool with DevOps Change Velocity ensuring a more secure authentication method.

-   **[Bitbucket Cloud tool integration with ServiceNow](https://www.servicenow.com/docs/access?context=bitbucket-integration-dev-ops&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Integrate the Bitbucket Cloud coding tool with DevOps Change Velocity to connect, discover, import, and process real-time repository events in DevOps Change Velocity.

-   **[DevOps Change Workspace UI for simplified creation of custom tool integration with planning, coding and orchestration capabilities](https://www.servicenow.com/docs/access?context=create-a-tool-integration-from-the-devops-change-workspace&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Integrate a new custom tool across planning, coding and orchestration capabilities with basic know-how of ServiceNow using an intuitive DevOps Change Workspace UI. It offers easy navigation to the ServiceNow Platform for defining transformer or adapter rules, or integrate the ability to do so within the Workspace wherever applicable, and embeds necessary documentation links and tooltips to support self-service.

-   **[Import based evidence collection](https://www.servicenow.com/docs/access?context=import-based-evidence-collection-for-orchestration-capability&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Improve instance efficiency by skipping step-level pipeline processing for accelerated change management and evidence collection for GitHub Actions and Azure DevOps \(ADO\) orchestration tools.


## Changed in this release

-   **[Reflow for configurable workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    DevOps Change Configurable workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. For more information, see the [Accessibility information](devops-rn.md#devops-rn-accessibility) section that follows.

-   **[DevOps data in change request](https://www.servicenow.com/docs/access?context=create-change-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    View, add, and edit DevOps data in a manually created change request in Service Operations Workspace for a unified change request experience in both DevOps Change Workspace and Service Operations Workspace.

-   **[Enhancements to DevOps Model change](https://www.servicenow.com/docs/access?context=devops-change-multimodel&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**
    -   In-product guidance enables you to leverage DevOps models and easily create DevOps changes without disruption of your change process.
    -   To make the Change - DevOps – Implement flow of the DevOps model more suitable for DevOps changes, change tasks are no longer automatically created.
    -   The new Change – DevOps – Update execution state flow in the DevOps model means you no longer have to activate the DevOps Change Request Manual Approval flow to send a callback to the third-party orchestration tool.
    -   Fast-track your change process by using a new DevOps Simplified change model, which doesn’t contain the Assess state. Change approval for this model is based on the DevOps Simplified Model Change policy.
-   **[Branch details for artifacts and packages](https://www.servicenow.com/docs/access?context=using-dev-ops-release-change&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Branch details from pipeline executions are now available for artifacts and packages for better tracking.

-   **[Create lists](https://www.servicenow.com/docs/access?context=add-new-list-in-list-module&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Option to create customized lists added to the Changes, Tools, and Administration modules in the DevOps Change Workspace.

-   **[Jira Server connection using API key](https://www.servicenow.com/docs/access?context=create-jira-tool-dev-ops&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Connect to your Jira Server using API key authentication rather than basic authentication.

-   **[GitHub Actions reruns](https://www.servicenow.com/docs/access?context=github-actions-integration-with-devops&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Re-running failed GitHub jobs will now use the existing change request created for the failed jobs instead of creating new change requests.

-   **[Generalized Docker Container solution to support any orchestration tool](https://www.servicenow.com/docs/access?context=servicenow-custom-actions-for-gitlab&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Use the generalized and extensible Docker Container solution to integrate any orchestration tool with DevOps Change Velocity for invoking pipeline actions like change request creation and collecting relevant DevOps data without having to rely on tool specific plugins or extensions.

-   **[Simplified onboarding of planning tools that are not supported in the base system](https://www.servicenow.com/docs/access?context=onboard-gitlab-to-devops-change-velocity-workspace&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Integrate planning tools that are not supported in the base system by leveraging transformer rules. GitLab Issues is now available as one of the planning tools and is built leveraging this new approach so you can discover plans, import work items, and configure webhooks for work items \(issues\) in GitLab.

-   **[Enhanced manual DevOps change creation experience](https://www.servicenow.com/docs/access?context=create-change-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Add work items data in a manually created DevOps change request in  Service Operations Workspace  for  ITSM.

-   **[Default BitBucket branch property](https://www.servicenow.com/docs/access?context=dev-ops-administration&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Specify the default Bitbucket branch name that must be used to create an import request in the **sn\_devops.bitbucket\_default\_branch** property.

-   **[Additional scans for DevOps Health Scan Content pack](https://www.servicenow.com/docs/access?context=run-health-scan-check&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Additional set of proactive checks focused on problems that tend to occur before or after an upgrade along with identifying configuration issues like plugin and version incompatibilities, or pipelines that chronically fail, have been added.

-   **[Import pull-request records for Bitbucket Server or Bitbucket Data Center](https://www.servicenow.com/docs/access?context=devops-wkspc-bitbucket-tool-conn&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Import pull-request records for Bitbucket Server or Data Center for improved insights and efficiency.

-   **[Change request creation with errors in DevOps data retrieval for Harness pipelines](https://www.servicenow.com/docs/access?context=change-request-creation-with-devops-data-retrieval-errors&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Enable change request creation even if there is an error in retrieving the DevOps data for a Harness pipeline.

-   **[Branch name filter](https://www.servicenow.com/docs/access?context=create-devops-change-request-manual&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Search for build numbers by the branch name while associating DevOps data to a change request in the Service Operations Workspace \(SOW\) or Classic UI.

-   **[Test summary name in GitHub Actions](https://www.servicenow.com/docs/access?context=servicenow-devops-custom-actions-from-github-marketplace&version=xanadu&pubname=xanadu-it-service-management&section=servicenow-devops-test-report-custom-action&ft:locale=en-US)**

    The servicenow-devops-test-report custom action in GitHub now includes an optional test-summary-name parameter to specify the test summary results name.

-   **[Token based authentication for Rally](https://www.servicenow.com/docs/access?context=configure-webhooks-for-rally-manually&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Configure webhooks for Rally using token based authentication instead of using the integration username and password.

-   **[Renamed variables for Docker](https://www.servicenow.com/docs/access?context=servicenow-custom-actions-for-gitlab&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    The environmental variables in the Generic Docker actions for DevOps Change Velocity have been renamed by removing the CI prefix for better clarity.

-   **[Security scan results](https://www.servicenow.com/docs/access?context=dev-ops-change-acceleration&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Security scan results on the change record associated to a pipeline execution with a linked package are now displayed in the **Security Summaries** tab.

-   **[Source of commits in SOW](https://www.servicenow.com/docs/access?context=create-change-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    View the source of commits like pipeline execution, branch, repository, and so on for a change request in the DevOps data section of the Service Operations Workspace.

-   **[Track file changes](https://www.servicenow.com/docs/access?context=sc-github&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    The **Track file changes** option is now disabled by default when a repository is configured to prevent any potential security risks.

-   **[Close code value for a change request](https://www.servicenow.com/docs/access?context=dev-ops-administration&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Two new properties have been added in DevOps Change Velocity, so that you can specify a close code value for a change request based on the change request completion state when the autoCloseChange parameter is enabled.

-   **[Support for MID Server cluster](https://www.servicenow.com/docs/access?context=playbook-enter-github-instance-details&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Improve load balancing and failover protection by selecting a MID Server cluster when connecting to a tool instance associated with a MID Server cluster. This configuration enables multiple MID Servers with relevant capabilities to be grouped.

-   **[Improved UX for DevOps Change health scans](https://www.servicenow.com/docs/access?context=run-health-scan-check&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Run health scans and analyze findings efficiently in the DevOps Change workspace with an intuitive and user-friendly interface.

-   **[Pipeline association for GitHub Actions](https://www.servicenow.com/docs/access?context=sc-github&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    When onboarding GitHub Actions pipelines through the App onboarding catalog or the onboarding APIs, now only the selected pipelines are associated with the DevOps app. If no pipeline is selected, all pipelines within the specified repository are associated.

-   **[Tool connection check status](https://www.servicenow.com/docs/access?context=devops-reference-error-messages&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    If a tool is marked as Disconnected because of a system-generated failure during an unsuccessful connection check, any subsequent successful check automatically updates the connection status to Connected. If you manually disconnect the tool, the tool status remains Disconnected even if there’s a subsequent successful connection check.

-   **[New roles for vulnerability integration](https://www.servicenow.com/docs/access?context=installed-with-dev-ops&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**
    -   The sn\_vul.app\_sec\_manager role is added to the DevOps Tool Owner \[sn\_devops.tool\_owner\] role when the DevOps Vulnerability Integrations plugin \(sn\_devops\_vul\_ints\) is installed.
    -   The sn\_vul\_veracode.configure\_integration role is added to the DevOps Tool Owner \[sn\_devops.tool\_owner\] role when the Vulnerability Response Integration with Veracode plugin \(sn\_vul\_veracode\) is installed.

## Activation information

Activate DevOps Change Velocity by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Accessibility improvements**

    Accessibility improvements were completed to create a configurable workspace that supports WCAG 2.1 Level AA conformance.

-   **Reflow**

    The Configurable Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

    This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) for details.


## Related ServiceNow applications and features

-   **[Performance Analytics](https://www.servicenow.com/docs/access?context=pa-overview&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

    ServiceNow® Performance Analytics is an in-platform process optimization solution to create management dashboards, report on KPIs and metrics, and answer key business questions. The application helps improve quality and reduces the costs of service delivery.

-   **[Change Management](https://www.servicenow.com/docs/access?context=c_ITILChangeManagement&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    The ServiceNow® Change Management application provides a systematic approach to control the life cycle of all changes, facilitating beneficial changes to be made with minimum disruption to IT services.

-   **Agile Development**

    The ServiceNow® Agile Development application helps you deliver software projects more efficiently by managing and tracking software development life cycles using an iterative, incremental, and flexible approach.

-   **[Risk Management](https://www.servicenow.com/docs/access?context=grc-risk-overview&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    The ServiceNow® Governance, Risk, and Compliance Risk Management application helps you continuously monitor and identify high-impact risks, improve your risk-based decision-making, and reduce reaction time effectively. The application also provides structured workflows for the management of risk assessments, risk indicators, and risk issues.


**Parent Topic:**[IT Service Management release notes](../it-service-management/it-service-management-rn-landing.md)

