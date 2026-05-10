---
title: DevOps Change Velocity integrations
description: Get an overview of how DevOps Change Velocity integrates with your external DevOps toolchain and the tools supported for this integration.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, DevOps Change Velocity, IT Service Management]
---

# DevOps Change Velocity integrations

Get an overview of how DevOps Change Velocity integrates with your external DevOps toolchain and the tools supported for this integration.

The DevOps Change Velocity integration with external tools is achieved by exposing REST endpoints to receive webhook notifications or direct REST calls from these tools in real-time. Additionally, DevOps Change Velocity enables importing of data from these tools using polling. DevOps API enables integration with any coding, planning, or orchestration tools. For more information, see [DevOps API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/devops-api.md).

## Supported tools

The DevOps Change Velocity application provides connectors by default to connect the following commonly used DevOps tools to import data. If your tool isn’t included in this list, you can manually connect and configure an integration. See [User-created integrations in DevOps Change Velocity](dev-ops-tool-integration.md).

<table id="table_qpj_y3v_shb"><thead><tr><th>

Tool type

</th><th>

Tools and the supported version

</th></tr></thead><tbody><tr><td>

Planning

</td><td>

-   Azure Boards \(Azure DevOps latest cloud version\)
-   Azure DevOps Server \(ver 2022.0.1\)
-   Jira Server and Jira Cloud \(latest cloud version\)
-   ServiceNow Agile Development 2.0
-   GitHub \(latest cloud version\)
-   GitHub Enterprise \(ver 3.7\)
    -   Basic authentication
    -   OAuth
-   Rally \(latest cloud version\)

</td></tr><tr><td>

Coding

</td><td>

-   Azure Repos \(Azure DevOps latest cloud version\)
-   Azure DevOps Server \(ver 2022.0.1\)
-   Bitbucket \(ver 7.19.2 on-premises\)
-   Bitbucket Cloud \(latest cloud version\)
-   GitHub \(latest cloud version\)
-   GitHub Enterprise \(ver 3.7\)
    -   Basic authentication
    -   OAuth
-   GitLab \(ver 13.0.6 for on-premises or latest cloud version\)

</td></tr><tr><td>

Orchestration

</td><td>

-   Azure Pipelines \(Azure DevOps latest cloud version\)

Jobs supported:

    -   Agent job
    -   Agentless \(server\) job
-   Azure DevOps Server \(ver 2022.0.1\)
-   Jenkins \(ver 2.289.1\)

Jobs supported:

    -   Freestyle project
    -   Folder \(default is 3 levels\)
    -   Pipeline
    -   Multibranch Pipeline
-   GitLab \(ver 13.0.6 for on-premises or latest cloud version\)
-   GitHub \(latest cloud version\)
-   GitHub Enterprise \(ver 3.7\)
    -   Basic authentication
    -   OAuth
-   Argo CD \(latest cloud version\)

</td></tr><tr><td>

Repository artifacts

</td><td>

-   JFrog \(ver 7 for on-premises or latest cloud version\)
-   Azure Artifacts \(Azure DevOps latest cloud version\)
-   Azure DevOps Server \(ver 2022.0.1\)

</td></tr><tr><td>

Testing

</td><td>

If any test is run as part of the pipeline executions of the following supported Orchestration pipelines, the information is shown in the test summary-   GitHub \(latest cloud version\)
-   GitHub Enterprise \(ver 3.7\)
    -   Basic authentication
    -   OAuth
-   GitLab \(ver 13.0.6 for on-premises or latest cloud version\)
-   Azure DevOps \(latest cloud version\)
-   Azure DevOps Server \(ver 2022.0.1\)
-   Jenkins \(ver 2.289.1\)

</td></tr><tr><td>

Software Quality

</td><td>

SonarQube \(ver 8.9.6 or latest cloud version\) scans supported on-   Azure DevOps pipelines \(latest cloud version\)
-   Azure DevOps Server \(ver 2022.0.1\)
-   Jenkins \(ver 2.289.1\) pipelines

</td></tr><tr><td>

Feature Flag

</td><td>

Split \(latest cloud version\)

</td></tr><tr><td>

Security

</td><td>

-   Veracode \(latest cloud version\)
-   Checkmarx One \(ver 1.0.17\)
-   Checkmarx SAST \(ver 1.0.16\)

</td></tr></tbody>
</table>## Third-party extensions

Use the ServiceNow extensions to model your pipeline in DevOps and configure branch analysis for tools like SonarQube.

Additional extensions may be required for applications such as Jenkins or Azure DevOps. These extensions are used when ServiceNow DevOps can’t integrate using only the native REST API and push notifications.

-   **Jenkins plugin for ServiceNow DevOps**

    A Jenkins plugin is provided to enable change acceleration so your orchestration tool can communicate and control certain aspects of pipeline executions from within ServiceNow DevOps.

    Install the plugin from the Jenkins Marketplace. Navigate to **Manage Jenkins &gt; System configuration &gt; Plugins** in your Jenkins instance. Search for **ServiceNow DevOps Plugin** and select it, and then select **Install**.

-   **ServiceNow DevOps for Azure DevOps**

    Use the **ServiceNow DevOps** extension on [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=ServiceNow.vss-services-servicenow-devops) if you plan to integrate your Azure DevOps pipeline with ServiceNow DevOps.

    For more information, see [Use the ServiceNow DevOps extension for Azure DevOps and Azure DevOps custom actions](../task/config-dev-ops-extensions-azure.md#).

-   **ServiceNow DevOps custom actions for GitHub Actions**

    Use the **ServiceNow DevOps** custom actions on [GitHub marketplace](https://github.com/marketplace?query=servicenow+devops) if you plan to integrate your GitHub workflows with ServiceNow DevOps.

    For more information, see [GitHub Actions configurations](github-actions-integration-with-devops.md#).


To start integrating DevOps Change Velocity with your toolchain, see [Integrating DevOps Change Velocity with third party tools](integrating-devops-change-with-third-party-tools.md).

**Parent Topic:**[Exploring DevOps Change Velocity](dev-ops-landing-page.md)

**Related topics**  


[Getting started with DevOps Change Velocity](setting-up-devops-change-velocity.md)

