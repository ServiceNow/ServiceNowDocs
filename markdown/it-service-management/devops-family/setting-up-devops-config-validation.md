---
title: Configuring DevOps Config
description: The DevOps engineer role installs and sets up DevOps Config, which is used to validate config data \(committed by developers, or app engineers\) before deployment.
locale: en-US
release: australia
product: DevOps \(Family\)
classification: devops-family
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [DevOps Config, IT Service Management]
---

# Configuring DevOps Config

The DevOps engineer role installs and sets up DevOps Config, which is used to validate config data \(committed by developers, or app engineers\) before deployment.

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

![DevOps Config setup configuration flow](../image/devops-config-setup-config.png)

<table id="table_wyt_bty_wtb"><thead><tr><th>

Data validation configuration tasks

</th><th>

\(Optional\) Advanced configuration tasks to extend the use of the data model

</th></tr></thead><tbody><tr><td>

1. [Install DevOps Config](../task/install-devops-config.md).

 Install DevOps Config application, content packs, and pipeline plugins.

 -   DevOps Config application.
-   \(Optional\) DevOps Config Policy content pack.
-   \(Optional\) DevOps Config Exporter content pack.
-   \(Optional\) Pipeline integration with DevOps Config.
    -   Argo CD plugin for ServiceNow DevOps
    -   ServiceNow DevOps extension for Azure DevOps.
    -   Jenkins plugin for ServiceNow DevOps.

</td><td>

N/A

</td></tr><tr><td>

2. [Create an application in DevOps Config](../task/create-app-devops-config.md).

 Create an application to set up the entity, and link between ServiceNow products.

</td><td>

N/A

</td></tr><tr><td>

3. [Create a deployable in DevOps Config](../../configuration-data-management/task/cdm-deployable-define.md).

 Create a deployable to define the environments to deploy the configuration data for your application \(typically Dev, Test, and Production\).

</td><td>

Extend the use of the data model by using [components](../../configuration-data-management/task/cdm-component-define.md) and [collections](../../configuration-data-management/task/cdm-collection-define.md) for a deployable in DevOps Config.

</td></tr><tr><td>

4. [Upload your configuration data](../../configuration-data-management/concept/cdm-upload-process.md).

 Upload your configuration data from each tool source to DevOps Config by creating and running an import script.

</td><td>

Upload configuration data depending on use case.

</td></tr><tr><td>

5. [Define policies in DevOps Config](../task/devops-config-define-policies.md).

 Define policies to run for validation of config data using default DevOps Config policies.

</td><td>

[Administrate the full life cycle of PaCE policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/policy-as-code-engine-pace/pace-managing-policies.md) and create your own.

</td></tr><tr><td>

6. [Map policies to a deployable](../../configuration-data-management/task/cdm-deployable-map-policy-to.md).

 Map policies to a deployable to run for validation of config data.

</td><td>

Extend the use of the data model by mapping policies to components and collections in DevOps Config.

</td></tr><tr><td>

7. [Define exporters in DevOps Config](../task/devops-config-define-exporters.md).

 Define exporters to export config data to your pipeline using default DevOps Config exporters.

</td><td>

-   Export config data for use by your deployment tools downstream in your CI/CD pipeline.
-   Extend the use of the data model by [creating a custom exporter](../../configuration-data-management/task/cdm-exporter-create-custom.md).

</td></tr><tr><td>

8. [Configure your pipeline in DevOps Config](devops-config-set-up-pipeline.md).

 Configure your pipeline to interact with your data model.

 Use DevOps Config [Azure DevOps pipeline tasks](devops-config-azure-integration.md) and [Jenkins pipeline actions](devops-config-jenkins-integration.md) to integrate your pipeline with DevOps Config.

</td><td>

N/A

</td></tr><tr><td>

9. [Run validation in DevOps Config](../task/devops-config-run-validation.md).

 Run validation and review the results.

</td><td>

N/A

</td></tr></tbody>
</table>