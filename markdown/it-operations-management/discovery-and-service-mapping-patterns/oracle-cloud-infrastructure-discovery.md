---
title: Oracle Cloud Infrastructure \(OCI\) discovery
description: ServiceNow Discovery uses the Oracle Cloud Infrastructure \(OCI\) discovery patterns to provide real-time elasticity for enterprise applications by combining Oracle autonomous services, integrated security, and cloud compute. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-cloud-infrastructure-discovery.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 6
keywords: [Patterns]
breadcrumb: [Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Oracle Cloud Infrastructure \(OCI\) discovery

ServiceNow Discovery uses the Oracle Cloud Infrastructure \(OCI\) discovery patterns to provide real-time elasticity for enterprise applications by combining Oracle autonomous services, integrated security, and cloud compute. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

Starting with version 1.29.0, Discovery and Service Mapping Patterns supports the discovery of OCI GovCloud accounts.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Prerequisites

-   **Verify that the following applications are installed**

    Verify that the following applications are installed and up to date:

    -   Cloud Access Interface \(starting from version 1.0.0\)
    -   Visibility Content
    -   CMDB CI Class Models
    -   Discovery and Service Mapping Patterns
-   **Configure Oracle API credentials**

    Ensure that your OCI credentials are configured and that your private and public keys are converted to the RSA format. For more information, see [Create Oracle API credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/create-oracle-api-credentials.md).

-   **Create OCI service account**

    For more information, see [Create OCI service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/create-oci-service-accounts.md).

-   **Create a cloud discovery schedule**

    To run a cloud discovery at scale, see [Create an OCI Discovery schedule in Discovery Admin Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/create-oci-schedule-DAW.md).

    Create a discovery schedule to run LDCs on.

    1.  Navigate to **Discovery** &gt; **Discovery Schedules**.
    2.  Select **Cloud Discovery**.
    3.  In the **Provider** field, select **OCI**. Fill in the form to create an account or select an existing one. For more information, see [Create OCI service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/create-oci-service-accounts.md).
    4.  On the **Select Datacenters** page, filter which LDCs you want to run the discovery.
    5.  When you're finished, navigate to the **Create Schedule** page and select **Finish and Run**.
-   **\(Optional\) Populate Service Account and Logical Datacenter fields in cloud CIs**

    Starting with Discovery and Service Mapping Patterns version 1.30.2, you can improve query performance by populating Service Account and Logical Datacenter fields directly in cloud CIs. For more information, see [Improved query performance with direct field population in CI tables]().


## Verify the REST API permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

-   **[OCI active datacenter pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-active-datacenter-pattern.md)**  
Discovery and Service Mapping Patterns finds the datacenters \(regions\) that your tenancy is subscribed to in your OCI environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[OCI Autonomous DB pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-autonomous-db-pattern.md)**  
Discovery and Service Mapping Patterns finds Autonomous Databases \(DB\) in your OCI environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[OCI availability domain pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-availability-domain-pattern.md)**  
Discovery and Service Mapping Patterns finds OCI availability domains in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[OCI cloud hardware type pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-cloud-hardware-type-pattern.md)**  
Discovery and Service Mapping Patterns finds OCI cloud hardware types \(called shapes in OCI\) in your Cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[OCI datacenter pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-datacenter-pattern.md)**  
Discovery and Service Mapping Patterns finds all datacenters \(regions\) that are available in OCI. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[OCI DB Home pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-db-home-pattern.md)**  
Discovery and Service Mapping Patterns finds Database Homes \(DB Homes\) in your OCI environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[OCI fault domain pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-fault-domain-pattern.md)**  
Discovery and Service Mapping Patterns finds OCI fault domains in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[OCI network pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-network-pattern.md)**  
Discovery and Service Mapping Patterns finds OCI Virtual Cloud Networks \(VCN\) in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[OCI NIC attachment pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-nic-attachment-pattern.md)**  
Discovery and Service Mapping Patterns finds OCI virtual network interface cards \(VNICs\) attachment records in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[OCI NIC pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-nic-pattern.md)**  
Discovery and Service Mapping Patterns finds OCI virtual network interface cards \(VNICs\) in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[OCI OS image pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-os-image-pattern.md)**  
Discovery and Service Mapping Patterns finds OCI OS images on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[OCI storage attachment pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-storage-attachment-pattern.md)**  
Discovery and Service Mapping Patterns finds storage attachments \(volume attachments\) in your OCI environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[OCI storage volume pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-storage-volume-pattern.md)**  
Discovery and Service Mapping Patterns finds OCI storage volumes in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[OCI sub account pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-sub-account-pattern.md)**  
Discovery and Service Mapping Patterns finds sub accounts \(compartments\) in your OCI environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[OCI subnet pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-subnet-pattern.md)**  
Discovery and Service Mapping Patterns finds OCI subnets in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[OCI virtual machine pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-vm-pattern.md)**  
Discovery and Service Mapping Patterns finds OCI virtual machines \(VMs\) in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Oracle Exadata cloud as a service pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-exadata-pattern.md)**  
Discovery and Service Mapping Patterns finds Oracle Exadata resources in your OCI environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

**Parent Topic:**[Available cloud discovery patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/available-patterns-cloud.md)

