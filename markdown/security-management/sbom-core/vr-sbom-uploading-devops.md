---
title: Uploading Software Bill of Materials for DevOps SBOM files
description: Generate and upload Software Bill of Materials SBOM files for software throughout its continuous integration and continuous deployment development cycles.
locale: en-US
release: yokohama
product: SBOM Core
classification: sbom-core
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Uploading and viewing your SBOM files in the SBOM Workspace, Software Bill of Materials, Unified Security Exposure Management, Security Operations]
---

# Uploading Software Bill of Materials for DevOps SBOM files

Generate and upload Software Bill of Materials SBOM files for software throughout its continuous integration and continuous deployment development cycles.

## DevOps and SBOM files

SBOM files can be generated at multiple stages throughout the software continuous integration and continuous deployment \(CI/CD\) development life cycle. Most software development operations \(DevOps\) in organizations use some type of CI/CD process to help them identify and prevent costly bugs that might surface after the release. Throughout the CI/CD pipeline, DevOps can generate SBOM files and pro-actively check for vulnerabilities and at-risk components. These checks can help organizations achieve better software quality and avoid costly maintenance later. Generating SBOM files is critical for successfully implementing and automating accurate build assessments during the CI/CD development.

Uploading SBOM files from development pipelines is supported starting with the following versions of the SBOM applications.

|Application|Supported versions|
|-----------|------------------|
|Data Model for SBOM|v3.0, v2.0|
|SBOM Core|v5.0, v4.0, v3.0|
|SBOM Response|v5.0, v4.0, v3.2, 3.1|

## Use cases

Generating SBOM files and sending them via the SBOM Upload API as part of the DevOps build pipeline can provide counts for the following to determine whether the pipeline should succeed or fail:

-   Added components
-   removed components
-   Vulnerabilities information
-   Package information \(abandoned/stale components\)

DevOps policies and rules for the success or failure of a pipeline may be defined by the vulnerability counts and stale and abandoned component count thresholds that are received from the SBOM Status API.

For a failed pipeline, DevOps users can access information about the failed build in their ServiceNow® instance to help them better understand the root cause and origin of the vulnerabilities.

See [Uploading Software Bill of Materials files using a REST API](vr-sbom-preparing-upload.md) for more information about \(POST\) and \(GET\) parameters and URLs for the Upload and Status APIs.

## Domain Separation

All the tables in the SBOM applications are domain separated.

