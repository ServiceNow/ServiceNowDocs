---
title: Integrating your pipeline in DevOps Config
description: Integrate your Argo CD, Azure DevOps, or Jenkins pipeline with DevOps Config to interact with your data model.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/devops-family/devops-config-integrations.html
release: australia
product: DevOps \(Family\)
classification: devops-family
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [DevOps Config, IT Service Management]
---

# Integrating your pipeline in DevOps Config

Integrate your Argo CD, Azure DevOps, or Jenkins pipeline with DevOps Config to interact with your data model.

**Important:** Starting with the Washington D.C. release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

Validate application and infrastructure details against your organization policies, and commit config data the same way software code is committed to a code repository.

Configuration data is pulled in your CI/CD pipeline to deploy not just a code for an application, but all the related configuration with that code as well.

**Note:** Pipeline integration requires plugin installation. See [Configure your pipeline in DevOps Config](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-family/devops-config-set-up-pipeline.md) for installation requirements.

## DevOps Config and DevOps Change Acceleration

With the DevOps Change Velocity change control feature, a change request is created as part of the pipeline for DevOps Config configuration changes.

Set up change acceleration in your pipeline.

-   **Argo CD**
-   **Azure DevOps**

    Using the `ServiceNow-DevOps-Server-Change-Acceleration` Azure DevOps task.

-   **Jenkins**

    Using the `snDevOpsChange` Jenkins action.


In DevOps Change Velocity, navigate to **DevOps** &gt; **Orchestrate** &gt; **Pipeline Change Requests** to view and approve DevOps change requests created by DevOps Config changes.

See [Accelerating your DevOps change process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/dev-ops-change-acceleration.md) for more information regarding the DevOps Change Acceleration feature.

