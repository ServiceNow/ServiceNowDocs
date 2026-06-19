---
title: Configuring DevOps Config
description: The DevOps engineer role installs and sets up DevOps Config, which is used to validate config data \(committed by developers, or app engineers\) before deployment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/devops-family/setting-up-devops-config-validation.html
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

**Important:** Starting with the Washington D.C. release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

\[Omitted image "devops-config-setup-config.png"\] Alt text: DevOps Config setup configuration flow

<table id="table_wyt_bty_wtb"><thead><tr><th>

Data validation configuration tasks

</th><th>

\(Optional\) Advanced configuration tasks to extend the use of the data model

</th></tr></thead><tbody><tr><td>

1. [Install DevOps Config](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-family/install-devops-config.md).

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

2. [Create an application in DevOps Config](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-family/create-app-devops-config.md).

 Create an application to set up the entity, and link between ServiceNow products.

</td><td>

N/A

</td></tr><tr><td>

3. [Create a deployable in DevOps Config](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-family/cdm-deployable-define.md).

 Create a deployable to define the environments to deploy the configuration data for your application \(typically Dev, Test, and Production\).

</td><td>

Extend the use of the data model by using [components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-family/cdm-component-define.md) and [collections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-family/cdm-collection-define.md) for a deployable in DevOps Config.

</td></tr><tr><td>

4. [Upload your configuration data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-family/cdm-upload-process.md).

 Upload your configuration data from each tool source to DevOps Config by creating and running an import script.

</td><td>

Upload configuration data depending on use case.

</td></tr><tr><td>

5. [Define policies in DevOps Config](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-family/devops-config-define-policies.md).

 Define policies to run for validation of config data using default DevOps Config policies.

</td><td>

Administrate the full life cycle of PaCE policies and create your own.

</td></tr><tr><td>

6. [Map policies to a deployable](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-family/cdm-deployable-map-policy-to.md).

 Map policies to a deployable to run for validation of config data.

</td><td>

Extend the use of the data model by mapping policies to components and collections in DevOps Config.

</td></tr><tr><td>

7. [Define exporters in DevOps Config](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-family/devops-config-define-exporters.md).

 Define exporters to export config data to your pipeline using default DevOps Config exporters.

</td><td>

-   Export config data for use by your deployment tools downstream in your CI/CD pipeline.
-   Extend the use of the data model by [creating a custom exporter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-family/cdm-exporter-create-custom.md).

</td></tr><tr><td>

8. [Configure your pipeline in DevOps Config](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-family/devops-config-set-up-pipeline.md).

 Configure your pipeline to interact with your data model.

 Use DevOps Config [Azure DevOps pipeline tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-family/devops-config-azure-integration.md) and [Jenkins pipeline actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-family/devops-config-jenkins-integration.md) to integrate your pipeline with DevOps Config.

</td><td>

N/A

</td></tr><tr><td>

9. [Run validation in DevOps Config](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-family/devops-config-run-validation.md).

 Run validation and review the results.

</td><td>

N/A

</td></tr></tbody>
</table>