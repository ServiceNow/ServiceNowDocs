---
title: Exploring DevOps Config
description: Use DevOps Config to store and manage all of your config data as a single source of truth. You can also use DevOps Config to validate your config data before deployment, and resolve conflicts in deployed config data.
locale: en-US
release: zurich
product: DevOps \(Family\)
classification: devops-family
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [DevOps Config, IT Service Management]
---

# Exploring DevOps Config

Use DevOps Config to store and manage all of your config data as a single source of truth. You can also use DevOps Config to validate your config data before deployment, and resolve conflicts in deployed config data.

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

Watch this short video to see how config data snapshots in DevOps Config can help you identify issues caused by unintended config data changes.

DevOps Config investigation with config data

Use root cause analysis of configuration-related outages or alerts to quickly identify and resolve unintended config data changes, also known as configuration "drift." Compare current and past versions of intended config data changes attached to change requests, and roll back to the desired state when needed.

For more information, see [Investigate an alert that involves a change to config data](../../configuration-data-management/task/cdm-d2a-investigate-cfg-changes.md).

![DevOps Config Use Cases for applications and Infrastructure as Code](../image/devops-config-explore.png)

## Manage your configuration data

DevOps Config becomes the single source of truth for your configuration data, rather than the source tool. A consolidated model manages and secures config data across multiple sources with role-based access control.

Although DevOps Config prevents non-compliant changes by validating your configuration data before deployment, security of the configuration data can't be enforced if the data is kept at the source and not stored in DevOps Config.

-   Workflow

    DevOps Config manages all your data in one location, validates it as it's written, and exports, when needed.

-   DevOps Engineer persona

    Use DevOps Config and DevOps Config API to manage and validate configuration data. Thus, enabling DevOps teams to release at a faster speed, ensuring that no risky or non-compliant changes are introduced in production.

    Use automated gates in a CI/CD pipeline or deployment script so that a deployment is stopped if any change to the application or infrastructure configuration is deemed risky or non-compliant.

    Manage DevOps Config as more policies are added and more exporters are defined.


## Validate your configuration data

DevOps Config acts as a test tool by automatically validating your configuration data before deployment to prevent non-compliant changes, while ensuring adherence to policy frameworks.

Validation before deployment occurs by executing policies on the configuration data. The DevOps Config Policy content pack includes generic policies that check for standard issues, but can be customized based on use case.

-   Workflow

    When configuration data is changed or added, DevOps Config runs policies on the configuration data that's stored across multiple sources, validates it, and returns the outcome.

    In the pipeline, the decision on whether to deploy is made, and the configuration data is retrieved from the source \(Git, for example\) to deploy.

-   App Engineer \(or IT infrastructure owner\) persona

    Use DevOps Config to validate configuration data. Thus, making sure no risks are introduced and that all changes are compliant with company policies before any changes are applied in a production environment.

    Since the tool integrates with the existing toolset, there's no change to the way work is done and there are no new tools to learn. Changes made to configuration data are validated in the background, and when the outcome is reported, action can be taken.


-   **[DevOps Config and DevOps Change Velocity](devops-config-devops-change.md)**  
DevOps Change Velocity collects data from all of your DevOps tools, providing visibility across the entire lifecycle of deployment, while DevOps Config manages and validates your DevOps configuration data.
-   **[Using an app in DevOps Config](devops-config-app.md)**  
When you create an app in DevOps Config, not only is it the container for the config data of the application, but the application model you choose links DevOps Config with other ServiceNow products, including DevOps Change Velocity.
-   **[DevOps Config powered by CDM and PaCE](devops-config-capabilities.md)**  
DevOps Config uses Configuration Data Management and Policy as Code Engine platform capabilities to manage configuration data and policies.
-   **[DevOps Config terms](../reference/devops-config-terms.md)**  
These are some of the common DevOps Config terms.

**Parent Topic:**[DevOps Config](devops-config-landing-page.md)

