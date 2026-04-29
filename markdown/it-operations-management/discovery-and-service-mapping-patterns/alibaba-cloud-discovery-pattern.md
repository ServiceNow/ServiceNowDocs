---
title: Alibaba Cloud discovery using patterns
description: Discovery and Service Mapping Patterns uses patterns to discover components of the Alibaba Cloud deployment during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Alibaba Cloud, Alibaba Cloud discovery, Alibaba Cloud patterns]
breadcrumb: [Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Alibaba Cloud discovery using patterns

Discovery and Service Mapping Patterns uses patterns to discover components of the Alibaba Cloud deployment during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Verify that the applications are up to date**
    -   Discovery and Service Mapping Patterns
    -   CMDB CI Class Models
    -   Visibility Content
-   **Create Alibaba Cloud credentials**

    For more information, see [Create Alibaba Cloud API Credentials](../../discovery/task/create-alibaba-cloud-api-credentials.md).

-   **Create an Alibaba Cloud service account**

    For more information, see [Set up Alibaba Cloud service accounts](../../discovery/task/set-up-alibaba-cloud-service-account.md).

-   **Schedule an Alibaba Cloud discovery**

    For more information, see [Create an Alibaba Cloud Discovery schedule in Discovery Admin Workspace](../../discovery/task/create-alibaba-schedule-DAW.md).

-   **\(Optional\) Populate Service Account and Logical Datacenter fields in cloud CIs**

    Starting with Discovery and Service Mapping Patterns version 1.30.2, you can improve query performance by populating Service Account and Logical Datacenter fields directly in cloud CIs. For more information, see [Improved query performance with direct field population in CI tables](query-service-account-ldc-fields.md).


## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

-   **[Alibaba Cloud availability zone pattern-based discovery](../reference/alibaba-availability-zone.md)**  
Discovery and Service Mapping Patterns uses the Alibaba - Availability Zone \(LP\) pattern to discover availability zones during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Alibaba Cloud cloud hardware type pattern-based discovery](../reference/alibaba-cloud-hardware-type.md)**  
Discovery and Service Mapping Patterns uses the Alibaba - Cloud Hardware Type \(LP\) pattern to discover cloud hardware types during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Alibaba Cloud cloud OS image pattern-based discovery](../reference/alibaba-cloud-os-image.md)**  
Discovery and Service Mapping Patterns uses the Alibaba - Cloud OS Image \(LP\) pattern to discover cloud OS images during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Alibaba Cloud datacenter pattern-based discovery](../reference/alibaba-datacenter-discovery.md)**  
Discovery and Service Mapping Patterns uses the Alibaba - Datacenter \(LP\) pattern to discover datacenters during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Alibaba Cloud service account pattern-based discovery](../reference/alibaba-service-account-discovery.md)**  
Discovery and Service Mapping Patterns uses the Alibaba - Service Account Validation pattern to discover service accounts during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Alibaba Cloud storage volume pattern-based discovery](../reference/alibaba-storage-volume.md)**  
Discovery and Service Mapping Patterns uses the Alibaba - Storage Volume \(LP\) pattern to discover storage volumes during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Alibaba Cloud virtual machine \(VM\) pattern-based discovery](../reference/alibaba-virtual-machine.md)**  
Discovery and Service Mapping Patterns uses the Alibaba - Virtual Machine \(LP\) pattern to discover VMs during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

**Parent Topic:**[Available cloud discovery patterns](available-patterns-cloud.md)

**Related topics**  


[Discovery for Alibaba Cloud](../../discovery/concept/alibaba-cloud-discovery.md)

