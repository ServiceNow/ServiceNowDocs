---
title: Uploading and viewing your SBOM files in the SBOM Workspace
description: The SBOM applications enable you to upload files and view details for entities, component inventories, license information and other details in the Software Bill of Materials Workspace.
locale: en-US
release: zurich
product: SBOM Core
classification: sbom-core
topic_type: concept
last_updated: "2025-09-09"
reading_time_minutes: 2
breadcrumb: [Software Bill of Materials, Unified Security Exposure Management, Security Operations]
---

# Uploading and viewing your SBOM files in the SBOM Workspace

The SBOM applications enable you to upload files and view details for entities, component inventories, license information and other details in the Software Bill of Materials Workspace.

## Overview of uploading SBOM files

You can upload your software bill of material files via an API or manually. View the files that you import as entities, which are inventories of the third-party component libraries used in your software, including any transitive dependencies.

-   [Uploading Software Bill of Materials files using a REST API](vr-sbom-preparing-upload.md).

    The Upload API is used for uploading and ingesting an SBOM file \(CycloneDX/SPDX\) into your instance.

-   [Upload Software Bill of Materials files manually](../task/vr-sbom-ingest.md).

    Upload software bill of materials files manually. The method you use to upload your files depends on whether you have the SBOM Core or SBOM Response applications installed.

-   [Uploading Software Bill of Materials for DevOps SBOM files](vr-sbom-uploading-devops.md).

    Generate and upload SBOM files for software throughout its continuous integration and continuous deployment development cycles.

-   Classify and resolve component licenses in the License administration module.

    Review [classify](../task/vr-sbom-classify-license.md), and [resolve](../task/vr-sbom-assign-license.md) \(assign\) license information for the components you upload in your SBOM files according to your internal or regulatory policies. You can match your components to licenses and determine your overall license compliance to see your potential risk exposure to banned, restricted, or missing licenses.

-   [Viewing reports and dashboards in the Software Bill of Materials workspace](vr-sbom-viewing-data-overview.md)

    Vulnerability analysts and managers can view uploaded software bill of materials files and important data in records, data visualizations, as well as enhanced vulnerability intelligence and license information the Software Bill of Materials \(SBOM\) Workspace.

    **Note:** You must install SBOM Response if you want to view the data visualizations on the landing \(Home\) page of the workspace.


