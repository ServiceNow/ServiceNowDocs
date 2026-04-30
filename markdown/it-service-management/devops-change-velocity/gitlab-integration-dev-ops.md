---
title: GitLab integration with DevOps Change Velocity
description: Connect to your GitLab instance to discover plans, repositories, and pipeline definitions and configure real-time notifications or polling to enable change traceability and automation.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integrate, DevOps Change Velocity, IT Service Management]
---

# GitLab integration with DevOps Change Velocity

Connect to your GitLab instance to discover plans, repositories, and pipeline definitions and configure real-time notifications or polling to enable change traceability and automation.

## GitLab integration overview

Versions supported:

-   On premises - base version 13.x and above
-   GitLab Cloud

DevOps Change Velocity supports Plan \(Issues\), Code \(Repository\) and Orchestration \(Pipelines\) capabilities for the GitLab tool. In case of pipelines, only basic pipelines are supported but not the multi-project ones.

-   **Connect**: Discover plans, repositories, and pipeline definitions by connecting your GitLab instances to DevOps Change Velocity.
-   **Configure**: Enable sending real-time notifications for commits, pipelines, and work items by automatically creating a webhook in GitLab so that this data can be used to create change policies.

**Note:** If you are upgrading to version 5.0.0 from a previous release, you must re-configure your tool to receive GitLab Issues \(planning\) related events.

Trigger events required for code capability:

-   Push events
-   Tag push events
-   Comments
-   Merge request events

Trigger events required for orchestration capability:

-   Job events
-   Pipeline events

Trigger events required for planning capability:

-   Issues events
-   Confidential issues events

## Key points

-   A pipeline must be run and completed at least once before enabling change control.
-   If a manual job in GitLab is canceled, or times out before completion, the corresponding change remains in **Open** state until the change request approval process is completed manually.
-   Pipeline discovery is limited to the first 100 results using the project search filter. To discover additional pipelines, modify the search filter \(which appears when you select **Discover**\) to expand the results for the discovery request.
-   Milestone discovered from a GitLab plan is displayed as release version in ServiceNow DevOps Change Velocity.
-   Repositories or pipelines created or updated after the project has already been discovered and configured are tracked manually.
-   JUnit test type integration is supported for GitLab. GitLab unit test reports support test reports only in the JUnit report format. You can convert different test types to JUnit and persist it. For detailed information, see [Unit test reports](https://docs.gitlab.com/ee/ci/testing/unit_test_reports.html) and [Unit test report examples](https://docs.gitlab.com/ee/ci/testing/unit_test_report_examples.html).
-   [Test tool integration](dev-ops-test-tool-integration.md) lets you view test results in DevOps for GitLab unit, functional, and performance tests.
-   Pipeline reruns are not supported.

## Get started

Use one of the following options to onboard GitLab. For a guided experience, use the workspace to onboard a tool. Alternatively, you can use the Service Catalog or Classic experience.

-   **[Onboard GitLab to DevOps Change Velocity — Workspace](../task/onboard-gitlab-to-devops-change-velocity-workspace.md)**  
Connect to your GitLab instance using the DevOps Change Workspace playbook to discover plans, repositories, and pipelines.
-   **[Onboard GitLab to DevOps Change Velocity — Service Catalog](../task/sc-gitlab.md)**  
Create, connect, discover, and configure your GitLab instance using the ServiceNow Service Catalog.
-   **[Onboard GitLab to DevOps Change Velocity — Classic](../task/create-gitlab-tool-dev-ops.md)**  
Create an GitLab tool record in DevOps Change Velocity to connect, discover, and import GitLab tool data.

**Parent Topic:**[Integrating DevOps Change Velocity with third party tools](integrating-devops-change-with-third-party-tools.md)

