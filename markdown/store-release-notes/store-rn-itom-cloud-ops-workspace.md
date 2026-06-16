---
title: Cloud Discovery Workspace release notes
description: Version history for the Cloud Discovery Workplace application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-cloud-ops-workspace.html
release: store
topic_type: reference
last_updated: "2025-05-01"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Cloud Discovery Workspace release notes

Version history for the Cloud Discovery Workplace application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.7.1 - May 2025**
    -   Fixed:
        -   Improved performance leading lesser loading time for CDW pages.
        -   Data Center Refresh successfully for GCP accounts.
-   **Version 1.7.0 - November 2024**

    Removed: Cloud resources dashboard has been deprecated.

-   **Version 1.6.2 - August 2024**

    Bug fixes.

-   **Version 1.6.1 - May 2024**
    -   Changed: Cloud Operations Workspace is now called Cloud Discovery Workspace.
    -   Removed: Stale CIs widget has been removed.
-   **Version 1.5.0 - November 2023**
    -   New: Download SBOM \(Softare bill of materials\) for discovered docker containers from the record page
    -   Changed:
        -   Updated navigation across k8s resource hierarchies through the updated Kubernetes explorer
        -   All configurable workspace pages meet the WCAG 2.1 AA Reflow requirements
    -   Fixed: This release brings in updated stability of Discovery wizard in creating and editing cloud discovery schedules.
    -   Removed: Support for Utah release is removed with support for new UI layout version 3.0.
-   **Version 1.2.2 - March 2023 \(Tokyo\)**

    Fixed: PRB1595815. CloudDiscoveryScheduleConfig- ScriptInclude file needs to removed from COW Update folder.

-   **Version 1.4.0 - February 2023**
    -   New:
        -   Use the Kubernetes Explorer to navigate and view the Kubernetes resource listings: services, pods, nodes, clusters, and all the docker images.
        -   Assign specific mid or mid-cluster for cloud discovery schedules.
        -   Option to add new service accounts in the Discovery schedule setup navigation experience.
        -   Banners and notifications giving indication for new store releases for Discovery plugins.
        -   On-Prem vs public cloud VM resource count \(over time\) - Evaluate your cloud adoption progress.
    -   Changed: Cloud Resources inventory dashboard has been renamed as Cloud Resources Explorer.
    -   Removed: Tokyo is not supported with this release version owing to UI framework changes - upgrade to Utah release to use this version.
-   **Version 1.2.1 - May 2022**
    -   New:
        -   Cloud Resource inventory dashboard
        -   Google cloud inventory support
    -   Changed: Support for Polaris 'next' experience Dark theme
-   **Version 1.0.7 - February 2022**

    The Cloud Operations Workspace provides a new and rich experience for setting up the cloud discovery schedules and managing your cloud viewing preferences. This app houses Cloud Discovery, which helps to discover the cloud resources. In addition, Cloud Operations Workspace also provides information on the trend of cloud resource growth; thus helping you to ascertain the cloud usage of your organization.


