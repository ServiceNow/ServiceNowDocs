---
title: Cloud Exposure View release notes
description: The ServiceNow Cloud Exposure View is a module that is supported by Unified Security Exposure Management. The Cloud Exposure View module provides a single location for cloud security teams to monitor and act on all their cloud-related security findings from multiple vendors across their cloud environments. The Cloud Exposure View is new in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-03-05"
reading_time_minutes: 4
---

# Cloud Exposure View release notes

The ServiceNow® Cloud Exposure View is a module that is supported by Unified Security Exposure Management. The Cloud Exposure View module provides a single location for cloud security teams to monitor and act on all their cloud-related security findings from multiple vendors across their cloud environments. The Cloud Exposure View is new in the Zurich release.

## Cloud Exposure View highlights for the Zurich release

-   Monitor and act on all your cloud-related security findings from multiple vendors across your cloud environments.
-   Configure widgets that display interactive visualizations and filter assets by category for findings, assets, and exceptions.
-   View panels that link you to lists for more details about your findings.
-   View aggregated security data imported from third-party vendors.
-   Aggregated data from the Cloud Exposure View can be viewed in the Unified Cloud workspace that is supported by ITOM Cloud Accelerate. See [ITOM Cloud Accelerate release notes](../it-operations-management/itom-cloud-accelerate-rn.md) for more information.

See Exploring Cloud Exposure View for more information.

**Important:** Unified Cloud workspace is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New Cloud Exposure View features

-   **[Enhancements to the Wiz Vulnerability Response Integration](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**
    -   The Universally Unique Identifier \(UUID\) that identifies detections for the Wiz Host Vulnerability integration will be mapped to a detection key.

        **Note:** This enhancement is supported for new customers only.

        For existing customers, the detection key for the Wiz Host Vulnerability integration is created using the combination of vulnerability, asset\_id, and proof.

    -   Added the source\_id column to the Container Image Finding table \(sn\_vul\_container\_image\_findings\) and mapped the id attribute from the Wiz import to this field on findings records.

        **Note:** Perform a full import after upgrading to view the enhancement on container image findings, container image, and container image vulnerabilities records.

    -   The image repository name format for new and existing discovered container images has been updated to align with the discovery format. The supported format is registry/repository. A separate finding is created for a repository present in each registry.
    -   Appended all repositories that are associated with an image to the Repository field on the Discovered Container Image \[sn\_vul\_container\_image\] table, which can help you see images from specific repositories.
    -   You can configure the **First** parameter for the Wiz Asset Integration to help you resolve 504 errors. You can reduce the page size if you are having memory issues or generating errors. The default value is 500.
    -   The default integration instance parameter for configuring finding keys for the Container Vulnerability Integration includes src\_ci, vulnerability, package, image\_layer, and image\_repository.
-   ****

    The Cloud Exposure View module provides a single location for cloud security teams to monitor and act on all their cloud-related security findings from multiple vendors across their cloud environments.

    -   Configure widgets that display interactive visualizations and filter assets by category for findings, assets, and exceptions.
    -   View panels with links on a single page that direct you to the following detailed lists:
        -   Needs Attention
        -   Cloud resources with active findings
        -   Top Accounts/Assets by Risk
        -   Toxic combinations
        -   Compliance scores
    -   View aggregated security data imported from third-party vendors.
    See [Unified Security Exposure Management release notes](secops-sem-rn.md) for more information about Unified Security Exposure Management.


## Important upgrade information for Cloud Exposure View

The Cloud Exposure View is a workspace in the Cloud Security for Cloud Workspace application that is supported by the Unified Security Exposure Management application. Unified Security Exposure Management \(USEM\) and the Cloud Security for Cloud Workspace applications are required. USEM is available to all customers who are entitled to Vulnerability Response. See [Unified Security Exposure Management release notes](secops-sem-rn.md) for more information.

## Activation information

Install the required applications by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Unified Security Exposure Management \(USEM\)](https://www.servicenow.com/docs/access?context=unified-security-exposure-management-landing-page&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Unified Security Exposure Management \(USEM\) is a platform that brings together infrastructure, application, container, and configuration exposures into one unified experience.

-   **[Wiz Vulnerability Response Integration](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Import vulnerability and compliance data from Wiz scanners into your ServiceNow® AI Platform instance to help you get deeper insights into your cloud infrastructure risks. These integrations provide you with a comprehensive assessment of your overall cloud security posture and help you drive remediation actions directly from your instance.


**Parent Topic:**[Security Operations release notes](security-operations-rn-landing.md)

