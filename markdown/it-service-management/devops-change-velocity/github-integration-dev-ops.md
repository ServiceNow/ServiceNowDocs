---
title: GitHub integration with DevOps Change Velocity
description: Connect to your GitHub instance to discover repositories, plans, pipeline definitions and configure real-time notifications or polling to enable change traceability and automation.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Integrate, DevOps Change Velocity, IT Service Management]
---

# GitHub integration with DevOps Change Velocity

Connect to your GitHub instance to discover repositories, plans, pipeline definitions and configure real-time notifications or polling to enable change traceability and automation.

## GitHub integration overview

DevOps Change Velocity supports Plan \(Plans\), Code \(Repository\) and Orchestration \(Actions\) capabilities for the GitHub tool.

Both GitHub and GitHub Enterprise are supported.

The following operations are performed as part of integrating GitHub:

-   Connect: Discover repositories, plans, and pipeline definitions by connecting your GitHub instances to DevOps Change Velocity.
-   Configure: Enable sending real-time notifications for commits, work items, and pipelines by automatically creating a Webhook \(push, issues, and workflow\_job\) in GitHub so that this data can be used to create change policies.

Repositories under an organization can also be discovered and configured if you have the following base permissions for the organization \(member privileges\):

-   Discover: Base permission of Read.
-   Configure: Base permission of Admin.

If Base permissions is specified as **No permission** for an organization, repositories under that organization can’t be discovered even if they’re public. The owner of an organization can either select all repositories or specific repositories for an organization and only the selected repositories are discovered. Even if a repository is public, it can’t be discovered unless the owner selects it for an organization.

For repositories under an organization, you must not have the same repository configured in more than one tool on an instance. If the same repository is configured for multiple tools, then data is associated with a random tool as part of notifications events. If you want to configure the same repository in a different tool, you must delete the webhooks created from the first tool, untrack the repository under that tool, and then configure the same repository in the different tool.

## Authentication methods

You can connect to GitHub using one of the following authentication methods:

-   Basic authentication

    If you connect your GitHub instance with basic auth, you can use the custom actions from the GitHub marketplace. GitHub environments aren’t supported for basic auth connection.

-   [OAuth 2.0 credentials](setting-up-github-oauth-dev-ops.md)
    -   If you connect your GitHub instance with OAuth 2.0 credentials for Authorization code, you can use the custom actions from the GitHub marketplace and create secrets to use in workflows. For more information, see [OAuth 2.0 credentials for GitHub Apps - Authorization Code](dev-ops-github-apps-oauth-auth.md#).
    -   If you connect your GitHub instance with OAuth 2.0 credentials for GitHub Apps - JWT, you can use the custom actions from the GitHub marketplace, create secrets to use in workflows, and GitHub environments to deploy to an environment. For more information, see [OAuth 2.0 credentials for GitHub Apps - JWT](dev-ops-github-apps-oath-jwt.md#). For GitHub repositories under an organization, only one organization can be installed per tool \(i.e - One GitHub App can be installed with One GitHub Org and with One GitHub tool\). If you want to add more organizations, you can create separate tools and apps.

**Note:** The OAuth Authorization Code &amp; JWT grant types are supported for GitHub &amp; GitHub Enterprise with MID server.

Custom actions by ServiceNow are available in GitHub Marketplace for the orchestration capability, to push information from Actions \(workflows\) and to pause or resume workflows from DevOps Change Velocity. For more information on custom actions, see [ServiceNow DevOps custom actions from GitHub marketplace](servicenow-devops-custom-actions-from-github-marketplace.md#).

To capture the workflow data in DevOps Change Velocity, you must configure Secrets in your GitHub tool. For more information, see [GitHub Actions configurations](github-actions-integration-with-devops.md#).

There are a few limitations for GitHub Actions support, see [GitHub Actions configurations](github-actions-integration-with-devops.md#).

## Get started

Use one of the following options to onboard GitHub. For a guided experience, use the workspace to onboard a tool. Alternatively, you can use the Service Catalog or Classic experience.

-   **[Onboard GitHub to DevOps Change Velocity — Workspace](../task/playbook-enter-github-instance-details.md)**  
Connect to your GitHub instance using the DevOps Change Workspace playbook to discover, configure, and import repositories, plans, and pipelines.
-   **[Onboard GitHub to DevOps Change Velocity — Service Catalog](../task/sc-github.md)**  
Create, connect, discover, and configure your GitHub instance using the ServiceNow Service Catalog.
-   **[Onboard GitHub to DevOps Change Velocity — Classic](../task/create-github-tool-dev-ops.md)**  
Connect your GitHub instance to discover, configure, and import repositories, plans, and pipelines.

**Parent Topic:**[Integrating DevOps Change Velocity with third party tools](integrating-devops-change-with-third-party-tools.md)

