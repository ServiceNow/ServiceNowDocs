---
title: Container image discovery
description: The Discovery and Service Mapping Patterns application uses the Scan Container Image pattern to discover Docker images and OS packages data. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-04-17"
reading_time_minutes: 3
keywords: [Trivy tool, Containers, Image, Os packages, Patterns.]
breadcrumb: [Container image scanning for software decomposition, Kubernetes discovery using patterns, Container discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Container image discovery

The Discovery and Service Mapping Patterns application uses the Scan Container Image pattern to discover Docker images and OS packages data. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

For information about performing a container image scan, see [Scan container images](../task/container-image-task.md).

The Scan Container Image pattern supports Aqua Trivy starting with version 0.44.0. The last version validated is 0.68.2.

Starting with Discovery and Service Mapping Patterns version 1.18.0, the Scan Container Image pattern supports scanning container images in the following repositories:

-   Public repositories
-   Self-hosted private repositories
-   Amazon Elastic Container Registry \(Amazon ECR\), both public and private repositories

Starting with version 1.27.0, Discovery and Service Mapping Patterns enables you to control whether to link software packages to containers or only to images. For more information, see [Link software package information to images only](../task/link-software-package-only-image.md).

## Data collected by Discovery for container image scans

Discovery populates the data in the CMDB when running the Scan Container Image pattern.

<table id="table_x24_ywh_fwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Application \[cmdb\_ci\_appl\] table

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the container application.

 The MSSQL application record required name format: ApplicationTableName@containerName

 Example: MSFT SQL Instance@/sql1

</td></tr><tr><td class="sub-head" colspan="2">

Container environment variables \[cmdb\_container\_environment\_variables\] table

</td></tr><tr><td>

Container \[container\]

</td><td>

Name of the container.

</td></tr><tr><td>

Key \[key\]

</td><td>

Name of the Container environment variable.

</td></tr><tr><td>

Value \[value\]

</td><td>

Container environment variable value.

</td></tr></tbody>
</table>## Temporary tables for container image scans

**Note:** If you're using the 1.0.98 version to collect the data, the enriched scripts are supported only with MSSQL.

<table id="table_kkw_yng_mwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Container image scan Status \[sn\_itom\_pattern\_container\_image\_scan\_status\]

</td></tr><tr><td>

Image \[image\]

</td><td>

Name of the container image.

</td></tr><tr><td>

Message \[message\]

</td><td>

Errors or issues with the scanning process.

</td></tr><tr><td>

CI Class \[ci\_class\]

</td><td>

The image CI class based on the image command details.

</td></tr><tr><td>

Discovery status \[discovery\_status\]

</td><td>

The discovery status record of the image scan.

</td></tr><tr><td>

Scan Status \[scan\_status\]

</td><td>

The scan status. The available values are:-   None - The image isn’t scanned yet.
-   In Progress - The image scan is in progress.

**Note:** If one or more images are in progress, the next scan won't trigger.

-   Scanned - The image was scanned successfully.
-   Error - A problem occurred during the image scan. Check the message column for details.
-   Skipped - The image URL isn’t formed properly or isn’t reachable.

</td></tr><tr><td class="sub-head" colspan="2">

Container image OS packages \[sn\_itom\_pattern\_container\_image\_os\_packages\] table

</td></tr><tr><td>

Image \[image\]

</td><td>

Name of the container image.

</td></tr><tr><td>

Package Name \[package\_name\]

</td><td>

Name of the software package.

</td></tr><tr><td>

Package Version \[package\_version\]

</td><td>

Version of the software package.

</td></tr><tr><td>

Package Maintainer \[package\_maintainer\]

</td><td>

Name of the package maintainer.

</td></tr><tr><td class="sub-head" colspan="2">

Container Enrich Scripts \[sn\_itom\_pattern\_container\_enrich\_scripts\]

</td></tr><tr><td>

Active \[active\]

</td><td>

Whether the enrich script state is active.

</td></tr><tr><td>

CI Type \[ci\_type\]

</td><td>

The CI type to which the enrich script is applicable.

</td></tr><tr><td>

Order \[order\]

</td><td>

Execution order of a particular script.

</td></tr><tr><td>

Script \[script\]

</td><td>

The enrich script name.

</td></tr></tbody>
</table>## Relationships

These relationships are created to support the container image discovery.

<table id="table_d3z_vg3_fwb"><thead><tr><th>

CI

</th><th>

relation

</th><th>

CI

</th></tr></thead><tbody><tr><td>

cmdb\_ci\_appl

</td><td>

Runs on::Runs

</td><td>

cmdb\_ci\_oslv\_container

</td></tr><tr><td>

cmdb\_ci\_docker\_container

</td><td>

Extends from

</td><td>

cmdb\_ci\_oslv\_container

</td></tr><tr><td>

cmdb\_ci\_oslv\_container

</td><td>

Extends from

</td><td>

cmdb\_ci

</td></tr><tr><td>

cmdb\_ci\_oslv\_container

</td><td>

Reference only

</td><td>

cmdb\_container\_environment\_variables

</td></tr><tr><td>

container\_enrich\_scripts

</td><td>

Extends from

</td><td>

sys\_metadata

</td></tr><tr><td>

cmdb\_container\_environment

</td><td>

Extends from

</td><td>

cmdb\_key\_value

</td></tr><tr><td>

cmdb\_ci\_db\_mssql\_instance

</td><td>

Runs::Runs on

</td><td>

cmdb\_ci\_docker\_container

</td></tr></tbody>
</table>**Related topics**  


[Docker virtualization](../../discovery/concept/c-docker-virtualization.md)

[Kubernetes discovery using patterns](../concept/kubernetes-discovery.md)

