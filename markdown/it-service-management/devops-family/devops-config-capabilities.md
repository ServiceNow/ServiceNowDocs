---
title: DevOps Config powered by CDM and PaCE
description: DevOps Config uses Configuration Data Management and Policy as Code Engine platform capabilities to manage configuration data and policies.
locale: en-US
release: zurich
product: DevOps \(Family\)
classification: devops-family
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Explore, DevOps Config, IT Service Management]
---

# DevOps Config powered by CDM and PaCE

DevOps Config uses Configuration Data Management and Policy as Code Engine platform capabilities to manage configuration data and policies.

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

## DevOps Config platform capabilities

![DevOps Config capabilities](../image/devops-config-capabilities.png)

-   **Configuration Data Management \(CDM\)**

    CDM is one of two main capabilities in the DevOps Config product. The CDM plugin manages application and/or infrastructure configuration data within the ServiceNow AI Platform.

    CDM consists of the backend tables and logic that handles all aspects of an application configuration data model. The workspace pages that users interact with to manage their data model are also managed by this plugin.

    The CDM Context Menu Component plugin is a sub-component of the CDM plugin. It provides the context \(for example, three dot\) menu for the node list pane in the Config Data tab for an application.

-   **Policy as Code Engine \(PaCE\)**

    PaCE is the second main capability in the DevOps Config product. It provides a robust policy engine that uses a policy script \(written in javascript\) to evaluate a snapshot of configuration data and verifies compliance.

    PaCE provides of a comprehensive versioning system so users can audit their policy changes over time. It also contains a test playground to evaluate potential policy script changes before going live with user configuration data.


## DevOps Config core application

-   **DevOps Config**

    DevOps Config is the main application for the DevOps Config product.

    The DevOps Config application consists of the workspace that connects users into their data model to manage their config data per application, manage policies to validate their config data, and review the health of their application configuration data.

    The Insights dashboard widgets lets users gain insights on their configuration data acumen, and build better habits in managing their configuration data.


## DevOps Config content packs

-   **DevOps Config Exporter Content Pack \(Optional\)**

    The DevOps Exporter Content Pack is an optional plugin that contains curated exporters that the DevOps Config team created and that users can leverage out-of-the-box to export the config data from their snapshots as they see fit.

-   **DevOps Config Policy Content Pack \(Optional\)**

    The DevOps Config Policy Content Pack is an optional plugin that contains curated policies that the DevOps Config team created and that users can leverage out-of-the-box so they can get to validating their config data right away.


**Note:** if users install either of these optional plugins first, they will get DevOps Config and all Dependencies plugins automatically installed as well.

## DevOps Config dependencies

![DevOps Config dependencies](../image/devops-config-dependencies.png)

These plugins are installed with core DevOps Config applications. They are critical to DevOps Config and do not function properly without them.

-   **CMDB CI Class Models**

    CDM leverages the CMDB CI Class Models plugin to connect aspects of user application configuration data model to the ServiceNow AI Platform CMDB.

    Applications are linked to an Application Model, which is part of the Build phase of the Common Service Data Model \(CSDM\). Similarly, deployables are linked to an Application Service, which is part of the Operations phase of the CSDM.

    The link between DevOps Config and the CSDM is critical for solving problems that may arise across a user software factory.

    For example, an operator is able to trace the cause for an alert for a particular CI, to a configuration change, to an application service \(of which that CI is a part\). This can reduce mean time to resolution, or MTTR, from hours to minutes.

-   **PA Premium**

    Performance Analytics \(PA\) Premium plugin is leveraged by the DevOps Config Insights plugin to allow for more than 180 days of reporting data for all DevOps Config Insights widgets.

-   **Expanded Model and Asset Classes**

    The Expanded Model and Asset Classes Store application adds enterprise model and asset classes that extend out-of-the-box product model and asset classes within the Configuration Management Database \(CMDB\) class hierarchy.

    These extensions include class descriptions, identification rules, identifier entries, and dependent relationships.


**Parent Topic:**[Exploring DevOps Config](devops-config-getting-started.md)

