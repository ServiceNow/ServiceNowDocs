---
title: Discovery store applications release notes
description: The ServiceNow Discovery store applications provide a unified, connected view of your entire IT infrastructure. See the following sections for release notes by version.Discover new Oracle, Red Hat, IBM, and AWS resources, with updates to OCI, Kubernetes, and AWS active datacenter discovery.ACC-Visibility September 2026 adds package discovery, custom software filter rules, license key verification, and software categorization for improved inventory control.The September release introduces life cycle management for service accounts, IP addresses, and tags.The September release includes updates to the mapping of RDS allocated storage capacity information and operating system domain and the import of primary IP address for Server. This release also includes the discovery of Amazon FSx file system resources and introduces IMDS v2 support for the discovery of Kubernetes resources.The September release includes updates to patch job discovery, operating system domain mapping, import of MAC address for Network Adapter, and deep discovery jobs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/discovery-store-apps-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 10
breadcrumb: [ITOM Visibility release notes, IT Operations Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Discovery store applications release notes

The ServiceNow® Discovery store applications provide a unified, connected view of your entire IT infrastructure. See the following sections for release notes by version.

## About Discovery store applications

-   Discovery and Service Mapping Patterns: 12 Oracle and 7 Red Hat application patterns, AWS Marketplace and IBM Flash Storage patterns, Cisco Nexus Virtual Routing and Forwarding \(VRF\) discovery, and Oracle Wallet support on Windows.
-   Cloud Service Graph Connectors:
    -   Service Graph Connector for AWS
    -   Service Graph Connector for GCP
    -   Service Graph Connector for Microsoft Azure
-   The Agent Client Collector for Visibility Content \(ACC-VC\) helps you perform effective discovery across on-premise and remote environments.
-   ITOM Content Service: 101 classifiers from publishers including Oracle, IBM, Microsoft, Apache Software Foundation, SAP, Dell EMC, Red Hat, BMC Software, and others.

See the following documentation for more information:

-   [Discovery patterns used by ITOM Visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/c_MappingPatternsCustomization.md)
-   [Service Graph Connector for AWS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/cmdb-integration-aws-sg.md)
-   [Service Graph Connector for Microsoft Azure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/cmdb-integration-azure.md)
-   [Service Graph Connector for GCP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/sgc-cmdb-integration-gcp.md)
-   [ITOM Content Service candidates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/itom-content-service-classifiers.md)

## Activation and other requirements

-   **Activation information**

    Install the applications by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[ITOM Visibility release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/itom-visibility-rn.md)

## Discovery and Service Mapping Patterns version 1.35.0

Discover new Oracle, Red Hat, IBM, and AWS resources, with updates to OCI, Kubernetes, and AWS active datacenter discovery.

### What's new

-   **[New patterns for resource discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/c_MappingPatternsCustomization.md)**

    Discover the following resources:

    -   [IBM Flash System storage servers, pools, volumes, network adapters, fibre channel ports, and controllers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/ibm-flash-system-pattern.md)
    -   [AWS Marketplace products \(product type: AMI and SaaS\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/aws-marketplace-pattern.md)
    -   [AWS Linux Server CIs \(cloud discovery\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/aws-linux-server-pattern.md)
    -   [AWS Windows Server CIs \(cloud discovery\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/aws-windows-server-pattern.md)
    -   [Oracle OCI hardware types \(shapes\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/oracle-cloud-hardware-type-pattern.md)
    -   [Oracle Access Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/oracle-access-manager-pattern.md)
    -   [Oracle Coherence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/oracle-coherence-pattern.md)
    -   [Oracle Enterprise Manager Management Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/oracle-oem-oms-pattern.md)
    -   [Oracle Forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/oracle-forms-pattern.md)
    -   [Oracle HTTP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/oracle-http-server-pattern.md)
    -   [Oracle Internet Directory Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/oracle-oid-server-pattern.md)
    -   [Oracle Node Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/oracle-node-manager-pattern.md)
    -   [Oracle Reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/oracle-reports-pattern.md)
    -   [Oracle Siebel CRM Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/oracle-siebel-crm-server-pattern.md)
    -   [Oracle Siebel Gateway Name Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/oracle-siebel-gateway-pattern.md)
    -   [Oracle TNS Listener](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/oracle-tns-listener-pattern.md)
    -   [Oracle Unified Directory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/oracle-unified-directory-pattern.md)
    -   [Red Hat 389 Directory Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/red-hat-389-directory-server-pattern.md)
    -   [Red Hat JBoss Enterprise Application Platform Host Controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/red-hat-jboss-eap-hc-pattern.md)
    -   [Red Hat JBoss Enterprise Application Platform Server on UNIX](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/red-hat-jboss-eap-server-unix-pattern.md)
    -   [Red Hat JBoss Enterprise Application Platform Server on Windows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/red-hat-jboss-eap-server-pattern.md)
    -   [Red Hat Podman](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/red-hat-podman-pattern.md)
    -   [Red Hat Single Sign-On Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/red-hat-sso-server-pattern.md)
    -   [Red Hat WildFly Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/red-hat-wildfly-server-pattern.md)
-   **[OCI UK Sovereign Cloud support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/create-oci-service-accounts.md)**

    Discover Oracle OCI UK Sovereign Cloud accounts by configuring a UK Sovereign Cloud datacenter URL when creating an OCI service account.

-   **[Cisco Nexus Virtual Routing and Forwarding discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/network-router-patterns.md)**

    Discover Virtual Routing and Forwarding \(VRF\) instances on Cisco Nexus switches using the "Network Switch" and "Network Router" patterns.

-   **[Kubernetes MID Server cluster high availability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/kubernetes-discovery.md)**

    Discover Kubernetes clusters using a MID Server cluster instead of a single MID Server for high availability and load balancing. Set up using a MID Server cluster by configuring the `sn_itom_pattern.k8s_midserver` property to a MID Server cluster name.

-   **[Oracle Wallet for Oracle Database discovery Windows support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/oracle-wallet-authentication.md)**

    Discover Oracle Databases on Windows using Oracle Wallet instead of storing applicative credentials on the ServiceNow AI Platform. Enable Oracle Wallet authentication by setting the **glide.discovery.oracle\_wallet\_authentication** property to **true**.

-   **[Kubernetes large-payload discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/kubernetes-discovery.md)**

    Discover Kubernetes clusters using the "Kubernetes Cluster - Per-Namespace LP" pattern to handle large cluster payloads.


### What's changed

-   **[AWS active datacenter discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/exclude-aws-resource-ldc-discovery.md)**

    AWS discovery now uses the Resource Explorer API instead of the Config API to determine whether a datacenter region is active or passive. Use the `mid.cloud.discovery.sonar.exclude_resource_types` property to exclude specific resource types when evaluating a region's status.

-   **[OCI virtual machine BYOL discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/oracle-vm-pattern.md)**

    The "Oracle OCI - Virtual Machine \(LP\)" pattern now discovers the Windows license type for OCI virtual machines \(VMs\), including Bring Your Own License \(BYOL\) and License Included.

-   **[Service Account and Logical Datacenter job full resync](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/configure-sa-ldc-full-resync.md)**

    The **Populate SA and LDC IN CMDB** job supports a full resync to reprocess all configuration item \(CI\) records. Configure the **sn\_itom\_pattern.populate\_saldc\_full\_resync** system property when service accounts or logical datacenters have incorrect or corrupted values for a CI.


## Agent Client Collector for Visibility Content version 2.0.3

ACC-Visibility September 2026 adds package discovery, custom software filter rules, license key verification, and software categorization for improved inventory control.

### What's new

-   **[Discover portable software installed by package managers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/accvc-package-discovery.md)**

    Discover software on endpoints that isn't discoverable by traditional checks and policies.

-   **[Create a custom filter rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/create-custom-filter-rule.md)**

    Create a custom software filter rule to exclude irrelevant entries from Discovery in your Software Asset Management \(SAM\) inventory.

-   **[Configure a license key discovery rule and write a parser script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/configure-license-key-rule.md)**

    Verify software legitimacy by creating license keys on your Windows, Linux and macOS devices.

-   **[Categorize software](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/acc-software-categorization.md)**

    Use software categorization to group discovered software packages into business-relevant categories. Software categorization helps you avoid manually tagging software and provides administrative teams with an efficient inventory of software records.


## Service Graph Connector for Microsoft Azure version 1.18.0

The September release introduces life cycle management for service accounts, IP addresses, and tags.

### What's new

-   **Life cycle management for service accounts, IP addresses, and tags**

    Life cycle management is supported for service accounts, IP addresses, and tags.

-   **SNK delimiter and key structure migration for CI identification**

    Updated SNK delimiter and key structure migration are used for Azure CI identification.

-   **Operating system domain mapping**

    Operating system domain is mapped for imported Azure virtual machines.

-   **Naming alignment with Cloud Discovery patterns**

    Azure datacenter \(location\) names are aligned with the naming used by Cloud Discovery patterns.

-   **Classification of Azure virtual desktop instances**

    Azure virtual desktop instances are classified correctly even when their power state is off. Powered-down VDI resources are now correctly classified and included in imports.

-   **Logical datacenter relationship**

    Managed database, multi workspace, and NIC are now related to their logical datacenter.

-   **Import of Azure Microsoft SQL managed instances**

    Azure Microsoft SQL managed instances are imported into the CMDB.

-   **Import of multiple log analytics workspaces for a hardware connection**

    Multiple log analytics workspaces can be imported for a single hardware connection.


### What's changed

-   ****

    Resolved the issue where the connector uses a database view that breaks when sys\_object\_source is moved to a gateway database.

-   ****

    Resolved the issue where a `Found multiple dependent relation items` error occurs when resources are moved between Azure datacenters.

-   ****

    Resolved the issue where the Disk Space field isn’t populated with the correct size during hardware import. The error occurred because the temporary disk size \(returned in megabytes\) was written to the hardware template without being converted to gigabytes.

-   ****

    Duplicate network interface card \(NIC\) CIs are created after SNK updates.

-   ****

    The Install status and Disk Space fields are now populated with RTE mappings for the Server class and the Computer class.

-   ****

    The Install status is now correctly updated for scale set virtual machines.

-   ****

    Resolved the issue where the operational\_status of a virtual machine CI reverts from Retired to Deployed after the virtual machine is deleted because the ETL transform script reads only the provisioning state and doesn’t check the change type.

-   ****

    Relationships are now created from Kubernetes Clusters and Azure Functions for service accounts.

-   ****

    Resolved the issue where software removal responses that were returned as `modified` created new CIs, resulting in duplicate records.

-   ****

    Resolved the issue where the hardware consolidation job and its underlying database view join filter on `PoweredState = ON`, which excludes powered-off virtual machines and can lead to incorrect data when the import runs outside business hours.

-   ****

    CIDR information is now correctly populated.

-   ****

    Resolved the issue where a datacenter is incorrectly marked as Passive when it contains only resource groups with no resources.


### What's deprecated or removed

-   **Field mapping for properties.privateEndpointConnections**

    The field mapping for properties.privateEndpointConnections is removed from Azure Functions.

-   **WMIC utility**

    The connector doesn’t depend on the deprecated WMIC utility when running commands on Windows hosts.


## Service Graph Connector for AWS version 2.15.0

The September release includes updates to the mapping of RDS allocated storage capacity information and operating system domain and the import of primary IP address for Server. This release also includes the discovery of Amazon FSx file system resources and introduces IMDS v2 support for the discovery of Kubernetes resources.

### What's new

-   **IMDS v2 support for discovery of Kubernetes resources**

    Instance Metadata Service Version 2 \(IMDS v2\) is supported for the discovery of Kubernetes resources.

-   **Primary IP address for server records**

    The primary IP address is populated in the imported server records.

-   **Operating system domain for AWS compute resources**

    Imported AWS compute resources include operating system domain details.

-   **RDS allocated storage capacity information for AWS RDS database resources**

    RDS allocated storage capacity information for AWS RDS database resources is populated in the cloud database table.

-   **Lookback time for service accounts**

    The lookback time window isn’t applied when processing service accounts.

-   **Amazon FSx file system resources**

    Amazon FSx file system resources are discovered and imported into the CMDB.


### What's changed

-   **New account state for AWS account API**

    The response status \(Status field\) of the AWS account API is now mapped to the new account state \(State field\).

-   **aws\_lookback\_time\_in\_days connection property**

    Resolved the issue with the aws\_lookback\_time\_in\_days connection property. Imports now follow the configured lookback window.

-   **aws\_lookback\_time\_in\_days connection property updated after full data load**

    The aws\_lookback\_time\_in\_days connection property is now updated only after a full scheduled data import.

-   **ListAccounts API call handles deprecated Status field**

    Resolved the issue where the ListAccounts API call didn’t handle the deprecation of the Status field, which could cause account imports to fail.

-   **Is Virtual attribute populated in Server records**

    The Is Virtual attribute is populated in the Server records created by Get Inventory imports.

-   **AWS organization set as parent for Amazon Redshift cluster records**

    The AWS organization is set as the parent for the Amazon Redshift cluster records that are created by the scheduled import.

-   **Version data populated for operating system record**

    The version data is populated for the operating system record in the Software Installation table.

-   **EKS Cluster data source**

    Resolved the issue where the EKS Cluster data source returned an error when the enableDbConfigLoad property is set to true.

-   **Flow execution contexts created for Get Inventory imports**

    Flow execution contexts are created for Get Inventory imports.

-   **Updated CloudFormation templates**

    The CloudFormation templates \(CFT\) used by the connector are updated to the latest versions available in SGC Central.

-   **GetS3Object transform doesn't overwrite names or create duplicate records**

    Resolved the issue where duplicate server records were created because the GetS3Object transform overwrote the Name field.

-   **isLastImport function in AwsRemovalUtil**

    Resolved the issue where the isLastImport function in AwsRemovalUtil only checked whether schedule imports were queued. The final import is now detected correctly.

-   **EKS ETL transformation for pod payloads with no volume mounts**

    Resolved the issue where the EKS ETL transformation failed for pod payloads that contain no volume mounts. Such payloads are now transformed successfully.

-   **Server records for AWS SSM-managed instances**

    Server records aren’t created for AWS Systems Manager \(SSM\) managed instances.

-   **EKS full scheduled import**

    Resolved the issue where an EKS full scheduled import didn’t import EKS data when the sn\_aws\_integ.eks\_document\_processing\_time property is set to 100.

-   **Status field removed from ETL mapping for SG-AWS-Service-Account data source**

    The deprecated Status field is removed from the ETL mapping for the SG-AWS-Service-Account data source.


## Service Graph Connector for GCP version 1.14.0

The September release includes updates to patch job discovery, operating system domain mapping, import of MAC address for Network Adapter, and deep discovery jobs.

### What's new

-   **Patch job discovery**

    Patch job discovery doesn’t depend on the deprecated WMIC utility. Patch data is collected on Windows hosts where the WMIC utility is removed or deactivated.

-   **MAC address details added in Network Adapter records**

    MAC address details are populated in the imported Network Adapter records.

-   **Mapping of operating system domain details**

    Operating system domain details are mapped during imports.

-   **Automatic retry of failed assets during batch API calls**

    Assets that fail during a batch API call are excluded and retried automatically.

-   **Lookback time for service accounts**

    The lookback time window isn’t applied when processing service accounts.


### What's changed

-   **Deep discovery jobs on GCP VM instances**

    Deep discovery jobs in the SG-GCP upgrade packages on GCP VM instances are now successful during discovery.

-   **Relationship created between cloud database and region**

    A relationship is created between cloud database and region.


