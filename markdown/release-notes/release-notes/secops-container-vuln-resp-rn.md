---
title: Container Vulnerability Response release notes
description: The ServiceNow Container Vulnerability Response application brings security and IT together to enable you to remediate your most critical vulnerabilities more quickly and efficiently. Container Vulnerability Response was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-06"
reading_time_minutes: 6
---

# Container Vulnerability Response release notes

The ServiceNow® Container Vulnerability Response application brings security and IT together to enable you to remediate your most critical vulnerabilities more quickly and efficiently. Container Vulnerability Response was enhanced and updated in the Australia release.

## Container Vulnerability Response highlights for the Australia release

-   The AWS Integration for Security Exposure Management supports integrations with AWS Inspector and AWS Security Hub.
-   If you're currently using Container Vulnerability Response and you want to upgrade to Unified Security Exposure Management \(USEM\), see [Unified Security Exposure Management \(USEM\) notes](secops-sem-rn.md) for more information about USEM and the Unified Security Exposure Management migration.
-   Import container image vulnerability data from the Wiz scanners into container vulnerable items \(CVITs\) with the Vulnerability Response Integration with Wiz.
-   With the sn\_vul\_container.vulnerability\_analyst or sn\_vul\_container.vulnerability\_admin role, create container remediation tasks manually in the Vulnerability Manager Workspace.
-   With the role sn\_vul\_container.remediation\_owner, create container remediation tasks manually in the IT Remediation Workspace.

See [Container Vulnerability Response](https://www.servicenow.com/docs/access?context=cvr-landing&version=australia&pubname=australia-security-management&ft:locale=en-US) for more information.

**Important:** Container Vulnerability Response is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Container Vulnerability Response to Australia

Enhancements to Container Vulnerability Response permit you to see enriched container vulnerability data on data imports from your third-party scanners. After you upgrade, you must perform a full import to view the features on discovered container image, container image finding, and container vulnerable item records that are described in the following New in the Australia release section.

If you're currently using Container Vulnerability Response, and you do not intend to upgrade to Unified Security Exposure Management \(USEM\), install a version below v30.x of Container Vulnerability Response and for upgrades to supported third-party integration applications.

For more information about the released versions of the Container Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Australia release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.

## New in the Australia release

-   **[Enhancements to Container Vulnerability Response](https://www.servicenow.com/docs/access?context=exploring-cvr&version=australia&pubname=australia-security-management&ft:locale=en-US)**

    The image repository name format for new and existing discovered container images in the Container Vulnerability Response application has been updated to align with the discovery format. Perform a complete import to view the registry/repository enhancements on existing and new records.

    -   The registry/repository format is supported for all third-party integrations including the [Vulnerability Response integration with Palo Alto Networks Prisma Cloud Compute](https://www.servicenow.com/docs/access?context=pcc-integration&version=australia&pubname=australia-security-management&ft:locale=en-US) and [Vulnerability Response Integration with Wiz](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=australia&pubname=australia-security-management&ft:locale=en-US) third-party integrations.
    -   Appended all repositories that are associated with an image to the Repository field on records on the Discovered Container Image \[sn\_vul\_container\_image\] table, which can help you see images from specific repositories.
    -   The default integration instance parameter for configuring finding keys for the Container Vulnerability Integration includes src\_ci, vulnerability, package, image\_layer, and image\_repository.
    Added the source\_id column to the Container Image Finding \[sn\_vul\_container\_image\_findings\] table. Mapped the id attribute from imports to the Source id field on findings records for all third-party integrations including the Vulnerability Response Integration with Palo Alto Networks Prisma Cloud Compute and [Vulnerability Response Integration with Wiz](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=australia&pubname=australia-security-management&ft:locale=en-US) third-party integrations.

-   **[AWS Integration for Security Exposure Management](https://www.servicenow.com/docs/access?context=aws-integration-for-security-exposure-management-overview&version=australia&pubname=australia-security-management&ft:locale=en-US)**

    The AWS Integration for Security Exposure Management supports integrations with the following AWS services:

    -   AWS Inspector is an automated vulnerability management service that continuously scans EC2 instances, ECR container images, and Lambda functions for software vulnerabilities \(CVEs\) and unintended network exposure. The Vulnerability Response integration with AWS Inspector imports host and container vulnerability findings from AWS Inspector.
    -   AWS Security Hub is a security service that is used to centralize and update security checks across AWS accounts. It provides a unified view of security alerts and compliance status by integrating with various AWS services. The Vulnerability Response integration with AWS Security Hub imports host, container vulnerabilities, and misconfigurations from AWS Security Hub.
-   **[Unified Microsoft Defender Integration for Security Exposure Management](https://www.servicenow.com/docs/access?context=ms-defender-sem&version=australia&pubname=australia-security-management&ft:locale=en-US)**

    The Microsoft Defender for Cloud and Microsoft Defender Threat and Vulnerability Management \(MS TVM\) plugins are now consolidated into a single plugin: Microsoft Defender Integration for Security Exposure Management. This consolidation deprecates the standalone Microsoft Defender for Cloud plugin. The unified plugin also introduces container image vulnerability ingestion from Microsoft Defender for Cloud, creating Container Vulnerable Items on your instance. A guided migration path is available to transfer existing data from the deprecated applications to the unified plugin.

-   **[Configure Image Vulnerability keys for Container Vulnerability Response CVIT creation](https://www.servicenow.com/docs/access?context=cvr-configuring-findings-key-granularity&version=australia&pubname=australia-security-management&ft:locale=en-US)**

    Configure records on the Configure Image Vulnerability Keys \[sn\_vul\_container\_image\_vulnerability\_keys\] table in your ServiceNow AI Platform® instance for the Image Vulnerability Keys that create container vulnerable items \(CVIT\)s.

    -   The Universally Unique Identifier \(UUID\) provided by Wiz is now mapped as the detection key for the Wiz Host Vulnerability integration.
    -   AWS ECS \(Elastic Container Service\) and AWS EKS \(Elastic Kubernetes Service\) environments are supported.
    -   Cluster and Service are supported for AWS ECS environments.
    -   Namespace, Registry, and Service are supported for AWS EKS environments.
    -   Choose either Scanner \(third-party scanners\) or Discovery \(Configuration Management Database \(CMDB\)\) as sources for data import for AWS ECS and AWS EKS.

        **Note:**

        If you choose **Discovery** as the data source, the Populate image relationships scheduled job runs daily to pre-import cluster and service details, and you should schedule your third-party integration runs at least 4 hours after this scheduled job is completed to verify that the pre-import data is available. This job is activated by default, but you must set the schedule so it runs before your scheduled third-party integration runs.

        For new customers only: The system property, sn\_vul\_container.image\_relationship\_mapping\_months sets the number of previous months \(1-12\) that you want your third-party integration to look for container image updates when processing relationship mappings. This data is used to filter images by the sys\_updated\_on field. The default setting is three months. After you configure the integration run, relationship mapping is created for images which have been scanned in the last 90 days and present in discovered container images.

    -   Column labels on the Container Vulnerable item \[sn\_vul\_container\_image\_vulnerable\_item\] table are updated to support the scanner and discovery options, depending on your choice on the Configure Image Vulnerability Keys configuration page:
        -   Cluster \(Scanner\) Namespace \(scanner\), and Service \(scanner\) for scanner data
        -   Cluster \(Discovery\), Namespace \(Discovery\) and Service \(Discovery\) for Discovery

## Deprecated features

-   The Path Column in the Container Image Package \[sn\_vul\_container\_image\_package\] table for the Vulnerability Response Integration with Palo Alto Networks Prisma Cloud Compute and [Vulnerability Response Integration with Wiz](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=australia&pubname=australia-security-management&ft:locale=en-US) third-party integrations. Path tracking has been moved to the Path Column on the Container Image Finding \[sn\_vul\_container\_image\_findings\] table to support accurate and consistent path and image association.

    If you use these integrations you must refer to the Path column available on the Container Image Finding \[sn\_vul\_container\_image\_findings\] table.

-   The Missing Assets \[sn\_vul\_wiz\_missing\_asset\] table used for storing assets imported by the backfill integrations for the [Vulnerability Response Integration with Wiz](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=australia&pubname=australia-security-management&ft:locale=en-US) is deprecated. If you're currently using the Vulnerability Response with Wiz integrations, after updating to version 1.1, you must backdate any of your existing Wiz primary integrations by three days and run them. See more information about the Wiz integration at [SecOps articles on the Security Operations Community](https://www.servicenow.com/community/secops-articles/announcement-wiz-integration-with-servicenow-secops/ta-p/3325055).

## Activation information

Install Container Vulnerability Response and third-party integrations by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Security Operations release notes](security-operations-rn-landing.md)

