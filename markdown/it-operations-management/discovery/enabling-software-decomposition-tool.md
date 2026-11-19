---
title: Enabling container image scanning with Syft scanner
description: Container image scanning with Syft scanner provides visibility into software packages within container images, helping you identify installed software for compliance, licensing, and security purposes without requiring a MID Server.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-operations-management/discovery/enabling-software-decomposition-tool.html
release: yokohama
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-08-13"
reading_time_minutes: 3
keywords: [Syft, container image scanning, software decomposition, Kubernetes Visibility Agent, SBOM, software packages]
breadcrumb: [Configuring Kubernetes Visibility Agent, Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Enabling container image scanning with Syft scanner

Container image scanning with Syft scanner provides visibility into software packages within container images, helping you identify installed software for compliance, licensing, and security purposes without requiring a MID Server.

KVA integrates with the Syft open-source tool to scan container images and discover software packages. This feature provides an alternative to the existing Aqua Trivy integration that requires a MID Server. For customers already using KVA, Syft scanner offers a simpler deployment without additional infrastructure or manual tool installation.

**Note:** For more information about this feature, see the [Software decomposition of container images using Kubernetes Visibility Agent and Syft \[KB3149735\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3149735) article in the Now Support Knowledge Base.

## Benefits of Syft scanner integration

The Syft scanner integration provides the following advantages:

-   No MID Server required
-   No manual installation of scanning tools
-   Automatic integration with KVA Informer
-   Scans container images directly from the Kubernetes cluster
-   Populates the same data model as the Aqua Trivy integration

## Installation method

The Syft scanner is only supported when installing KVA Informer using the Helm chart method. YAML-based installation does not support the Syft scanner feature.

To enable Syft scanner during Helm installation, add the following parameter to the Helm install command:

```
--set runSyftScanner=true
```

For complete installation instructions, see [Install Kubernetes Visibility Agent \(KVA\) Informer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/discovery/cnov-deploy-install.md).

## Enabling container image scanning

After installing the Informer with Syft scanner support, enable container image scanning by setting the following system properties to `true`:

-   **sn\_itom\_pattern.container\_image\_scan** - Enables the container image scanning mechanism
-   **sn\_acc\_visibility.image\_scan\_enabled** - Directs the system to use the Syft scanner in KVA instead of Aqua Trivy on a MID Server

**Note:** You cannot use both scanning methods simultaneously. When **sn\_acc\_visibility.image\_scan\_enabled** is set to `true`, the system uses only the Syft scanner method.

## Informer status fields

When an Informer is configured with Syft scanner support, the following fields appear on the Informer form:

-   **Image Scanner Enabled** - Indicates whether the Informer supports container image scanning \(true or false\)
-   **Image Scan Registries** - Comma-separated list of image registries the Informer can access through credential-less trust relationships \(ecr, acr, google\)

A new UI action **Get Syft Scanner Logs** is available on Informer records that have image scanning enabled. Selecting this action retrieves the Syft scanner logs and attaches them to the Informer record as `k8s_informer_syft.log`.

## Data collected by container image scans

When the Syft scanner successfully scans a container image, the system populates the following fields on the Docker Image CI \[cmdb\_ci\_docker\_image\]:

|Field|Description|
|-----|-----------|
|Operating System \[os\]|Operating system name|
|OS Version \[os\_version\]|Operating system version|
|Architecture \[architecture\]|Processor architecture. Examples: amd64, arm64|
|Size \(bytes\) \[size\_bytes\]|Image size in bytes|
|OS Family \[os\_family\]|Operating system family. Examples: rhel, centos, alpine, azurelinux, windows|
|Image created \[image\_created\_at\]|Timestamp when the image was created|
|Command \[command\]|Default command executed when the container starts|

**Note:** Not all fields are populated for every image. Field availability depends on the image metadata and scan results.

## Software packages

The Syft scanner identifies software packages contained in the container image and creates records in the Container Image OS Packages \[sn\_itom\_pattern\_container\_image\_os\_packages\] table. This table appears as a related list on the Docker Image CI form.

Each software package record includes:

-   Package Name
-   Package Version
-   Package Maintainer

**Note:** Package maintainer and version information depends on the data available in the image. The Syft scanner reports what is present in the image metadata.

## Monitoring scan status

The Container Image Scan Status \[sn\_itom\_pattern\_container\_image\_scan\_status\] table maintains the scan status for each container image. Access this table by navigating to the URL: `<instance>.service-now.com/sn_itom_pattern_container_image_scan_status_list.do`

Possible scan status values:

-   None - Image has not been scanned
-   In Progress - Scan is currently running
-   Scanned - Scan completed successfully
-   Error - Scan failed \(check the Message field for details\)
-   Skipped - Image URL is malformed or unreachable

**Parent Topic:**[Configuring Kubernetes Visibility Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/discovery/cnov-configuring.md)

**Related topics**  


[Container image scanning for software decomposition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/discovery/container-image-concept.md)

