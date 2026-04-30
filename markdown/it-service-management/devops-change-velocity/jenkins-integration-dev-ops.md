---
title: Jenkins integration with DevOps Change Velocity
description: Connect to your Jenkins instance to discover pipeline definitions and configure real-time notifications or polling to enable change traceability and automation.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integrate, DevOps Change Velocity, IT Service Management]
---

# Jenkins integration with DevOps Change Velocity

Connect to your Jenkins instance to discover pipeline definitions and configure real-time notifications or polling to enable change traceability and automation.

## Jenkins integration overview

DevOps Change Velocity supports Orchestration capability for the Jenkins tool and various kinds of pipeline types like Single Pipeline, Multibranch Pipeline, Folder, and Freestyle project types. For Folder, three levels are supported by default. Integrating Jenkins with DevOps Change Velocity enables you to retrieve the data from your Jenkins pipeline for end-to-end traceability and policy creation for change automation.

## Get started

-   **Onboard Jenkins to DevOps Change velocity**

    Connect your Jenkins instance to DevOps Change Velocity to retrieve data like artifacts, test results, scan results, and so on from your Jenkins pipelines. We recommend that you onboard using Workspace [Onboard Jenkins to DevOps Change Velocity — Workspace](../task/onboard-jenkins-to-devops-change-velocity-workspace.md) for an intuitive experience.

    You can connect to using one or both of the following authentication methods:

    -   Basic authentication, using the DevOps Integration User credentials.

        For more information about the integration user credentials, see [Set up integration user account in DevOps Change Velocity](../task/devops-plybk-set-up-system-accts.md).

    -   Secret token generated during tool connection.
-   **Set up Jenkins plugin to send real-time data**

    Automatically configure Jenkins to send real time notifications for your pipeline executions to DevOps Change Velocity. Real time notifications are ideal to maintain the most up-to-date information, particularly for automating change requests. For more information on setting up the plugin, see [Configure Jenkins plugin](../task/configure-jenkins-plugin.md#).

    **Note:**

    -   If you're using DevOps Config, it’s recommended to connect to Jenkins using basic authentication.
    -   You must ensure that the basic authentication credentials and secret token used are valid.

**Note:** Jenkins also supports testing capabilities with J Unit. [Test tool integration](dev-ops-test-tool-integration.md) lets you view test results in DevOps for Jenkins unit, functional, and performance tests.

Use one of the following options to onboard Jenkins. For a guided experience, use the workspace to onboard a tool. Alternatively, you can use the [Service Catalog](../task/sc-jenkins.md) or [Classic](../task/create-jenkins-tool-dev-ops.md) experience.

-   **[Onboard Jenkins to DevOps Change Velocity — Workspace](../task/onboard-jenkins-to-devops-change-velocity-workspace.md)**  
Connect to your Jenkins instance using the DevOps Change Workspace playbook to discover pipelines.
-   **[Onboard Jenkins to DevOps Change Velocity — Service Catalog](../task/sc-jenkins.md)**  
Connect your Jenkins instance using the ServiceNow Service Catalog to retrieve data like artifacts, test results, scan results, and so on.
-   **[Onboard Jenkins to DevOps Change Velocity — Classic](../task/create-jenkins-tool-dev-ops.md)**  
Connect your Jenkins instance to discover and track your pipelines, and import your orchestration tasks for end to end traceability and change automation.

**Parent Topic:**[Integrating DevOps Change Velocity with third party tools](integrating-devops-change-with-third-party-tools.md)

