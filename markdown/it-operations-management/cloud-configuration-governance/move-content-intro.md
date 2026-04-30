---
title: Moving Cloud Provisioning and Governance content across environments
description: You can move the content in the Cloud Provisioning and Governance application from one environment to the other. For example, develop an application in an environment and then move the application and all its dependencies to another environment for testing or production.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Moving Cloud Provisioning and Governance content across environments

You can move the content in the Cloud Provisioning and Governance application from one environment to the other. For example, develop an application in an environment and then move the application and all its dependencies to another environment for testing or production.

## Content entities that can be moved

The Cloud Provisioning and Governance application consists of code, resources, content, and configurations.

You can move the following content entities across environments:

-   Blueprints
-   Resource blocks
-   Cloud APIs

Use the update sets to move the content entities. Update sets, which are XML files, group all the content into named sets and then moves these sets, as a unit, to other systems for testing or deployment. For information on how system update sets work, see [System update sets](https://www.servicenow.com/docs/access?context=system-update-sets&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) .

## Content entity dependencies

Each of the content entities has some direct dependencies that are automatically moved with the content to the new environment.

The direct dependencies for each of these content entities are:

<table id="table_yk5_ypp_sgb"><thead><tr><th>

Content entity

</th><th>

Dependencies

</th></tr></thead><tbody><tr><td>

Blueprint

</td><td>

-   Resource blocks
-   Cloud APIs
-   MID scripts
-   Resource pools
-   Policies
-   Script includes
-   Cloud scripts

</td></tr><tr><td>

Resource blocks

</td><td>

-   Resource pools
-   Resource operation policies
-   Script includes
-   Cloud APIs
-   Dependant resource blocks
-   MID scripts

</td></tr><tr><td>

Cloud API

</td><td>

MID scripts

</td></tr></tbody>
</table>**Related topics**  


[Move a blueprint from one environment to another](../task/export-updateset-blueprint.md)

[Move a resource block from one environment to the other](../task/export-updateset-rblock.md)

[Move a cloud API from one environment to the other](../task/export-updateset-capi.md)

