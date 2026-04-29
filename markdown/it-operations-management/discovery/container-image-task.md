---
title: Scan container images
description: Enable container image scanning using the Aqua Trivy tool.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Container image scanning for software decomposition, Kubernetes discovery using patterns, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Scan container images

Enable container image scanning using the Aqua Trivy tool.

## Before you begin

**Note:** The pattern supports only the Linux operating system and runs on a Linux MID Server.

Verify the following setup:

-   Discovery and Service Mapping Patterns, starting 1.7.0 \(August 2023 store release\).
-   CMDB CI Class Models, starting 1.43.0.
-   Visibility Content, starting 6.7.2.
-   For the container images scan to run successfully, verify that all the MID Servers in your environment are configured for specific capabilities and are not set to **All**. For more information on configuring capabilities, see [MID Server capabilities](https://www.servicenow.com/docs/access?context=mid-server-capabilities&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).
-   MID Server requirements:
    -   8GB RAM with 4GB for the Java Virtual Machine \(JVM\)
    -   MID Server **Capability** configured to **Scan Container Images**
    -   Can access the image repository
-   Aqua Trivy starting 0.44.0 is installed on the MID Server. The last version validated is 0.68.2. For more information on installing Aqua Trivy, see the [Container Image scan feature overview \[KB1218504\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1218504) article in the Now Support Knowledge Base.
-   To collect Docker or Kubernetes container image and environment records, you must first run the Docker or Kubernetes discovery before enabling the Container Image Scan feature. For more information, see [Kubernetes discovery using patterns](../concept/kubernetes-discovery.md) and [Docker virtualization](../../discovery/concept/c-docker-virtualization.md).
-   Starting with Discovery and Service Mapping Patterns version 1.18.0, the Container Image Scan feature also supports the following:
    -   Using a proxy MID Server to scan the container images in the following repositories: public, self-hosted private, and Amazon Elastic Container Registry \(Amazon ECR\) repositories. To use a proxy MID Server, ensure the MID Server proxy parameters are correctly configured. For more information on proxy parameters, see [MID Server parameters](https://www.servicenow.com/docs/access?context=mid-server-parameters&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US). For information on bypassing the proxy MID Server for specific internal or private container registries, see [Configure a proxy bypass for specific internal or private container registries](configure-container-proxy-bypass.md).
    -   Scanning container images in self-hosted private repositories. To scan these repositories, you must create container image repository credentials. For more information, see [Create and test your credentials](https://www.servicenow.com/docs/access?context=t_CreateCredential&version=australia&pubname=australia-platform-security&ft:locale=en-US) and [Container image repository credentials](https://www.servicenow.com/docs/access?context=container-image-repo-credential&version=australia&pubname=australia-platform-security&ft:locale=en-US).
    -   Collecting image records from Amazon ECR in both public and private repositories. To collect these Amazon ECR image records, you must first run the Amazon ECS resource discovery before enabling the Container Image Scan. The AWS cloud service account created for the Amazon ECS resource discovery is also used for the container image scan. For more information about Amazon ECS resource discovery, see [Amazon ECS resource discovery with Patterns](../reference/aws-ecs-fargate-discovery.md).
-   Starting with version 1.27.0, Discovery and Service Mapping Patterns enables you to control whether to link software packages to containers or only to images. For more information, see [Link software package information to images only](link-software-package-only-image.md).
-   Starting with Discovery and Service Mapping Patterns version 1.30.2, you can map MID Servers to specific repositories. Use this option when network access or datacenter location requires specific MID Servers for certain repositories. For more information, see [Map MID Server to container image repository](map-mid-server-container-repository.md).

Role required: admin

## Procedure

1.  Enable the Discovery and Service Mapping Patterns Container Image Scan by setting the system property.

    1.  In the Navigation filter, enter `sys_properties.list`.
    2.  In the **Name** search field, enter `sn_itom_pattern.container_image_scan`.
    3.  Set the value to **true**.
2.  In the URL bar enter: `<instance>.service-now.com/sn_itom_pattern_container_image_scan_status_list.do` to review the scan status of the images.

3.  Select the image record to review the Container Image OS Packages table.


## Result

The Scan Container Image pattern finds the image OS packages and creates application records based on the image CI class. The Container Image OS Packages table is located in the image record. The pattern also creates relationships between the configuration items. For more information on the data collected, see [Container image discovery](../reference/container_image_scan_pattern.md).

**Parent Topic:**[Container image scanning for software decomposition](../concept/container-image-concept.md)

