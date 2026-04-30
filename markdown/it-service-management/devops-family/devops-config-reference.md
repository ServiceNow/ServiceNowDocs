---
title: DevOps Config reference
description: DevOps Config reference content.
locale: en-US
release: zurich
product: DevOps \(Family\)
classification: devops-family
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [DevOps Config, IT Service Management]
---

# DevOps Config reference

DevOps Config reference content.

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

-   **[Update the associations for a deployable](../../configuration-data-management/task/cdm-deployable-update.md)**  
Update the name and description of a deployable as well as its associations with applications and other items. This procedure is optional.
-   **[Types of configuration data supported by DevOps Config](../concept/config-data-devops-config.md)**  
DevOps Config stores configuration data of every layer of the IT stack in a centralized location.
-   **[CDM data model](../../configuration-data-management/reference/cdm-data-model.md)**  
The CDM data model is a standardized data structure that supports the broader life cycle of software delivery — automation, quality validation, and CSDM. CDM imports existing config data, validates it using policies that you define, and exports valid config data to your organization's existing DevOps pipeline to implement applications, services, and infrastructure.
-   **[APIs and DevOps Config](devops-config-cdm-api.md)**  
You can use DevOps Config and CDM APIs to access your config data.
-   **[DevOps Config roles](devops-config-roles.md)**  
DevOps Config uses these roles.
-   **[How encrypted data is handled](../../configuration-data-management/concept/cdm-secrets-managing.md)**  
By default, encrypted values appear in all views as `*******`. Only users with the CDM Secrets \[sn\_cdm.cdm\_secrets\] role can view, create, update, and delete encrypted values in config data. The system validates and exports encrypted data appropriately.
-   **[Domain separation and DevOps Config](../concept/devops-config-domain-separation.md)**  
Domain separation is unsupported for DevOps Config. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
-   **[Default DevOps Config policies](devops-config-default-policies.md)**  
The DevOps Config Policy content pack contains a set of default DevOps Config policies to validate your configuration data.
-   **[Default DevOps Config exporters](devops-config-default-exporters.md)**  
The DevOps Config Exporter content pack contains a set of default DevOps Config exporters of data that can be used as input for further deployment and provisioning activities.

**Parent Topic:**[DevOps Config](../concept/devops-config-landing-page.md)

