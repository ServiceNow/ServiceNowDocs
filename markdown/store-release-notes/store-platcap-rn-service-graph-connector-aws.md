---
title: Service Graph Connector for AWS release notes
description: Version history for the Service Graph Connector for AWS application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-service-graph-connector-aws.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 8
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\) version history release notes, ServiceNow Store - ServiceNow AI Platform Capabilities version history release notes, ServiceNow Store version history release notes]
---

# Service Graph Connector for AWS release notes

Version history for the Service Graph Connector for AWS application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.15.0 - September 2026**
    -   New:
        -   Instance Metadata Service Version 2 \(IMDS v2\) is supported for the discovery of Kubernetes resources.
        -   The primary IP address is populated in the imported Server records.
        -   Imported AWS compute resources include operating system domain details.
        -   RDS allocated storage capacity information for AWS RDS database resources is populated in the cloud database table.
        -   The lookback time window isn’t applied when processing service accounts.
        -   Amazon FSx file system resources are discovered and imported into the CMDB.
    -   Changed: The response status \(Status field\) of the AWS account API is now mapped to the new account state \(State field\).
    -   Fixed:
        -   Resolved the issue with the aws\_lookback\_time\_in\_days connection property. Imports now follow the configured lookback window. \(PRB2035571\)
        -   The aws\_lookback\_time\_in\_days connection property is now updated only after a full scheduled data import.\(PRB2060818\)
        -   Resolved the issue where the ListAccounts API call didn’t handle the deprecation of the Status field, which could cause account imports to fail.\(PRB2072899\)
        -   The Is Virtual attribute is populated in the Server records created by Get Inventory imports.\(PRB2032947\)
        -   The AWS organization is set as the parent for the Amazon Redshift cluster records that are created by the scheduled import.\(PRB2057788\)
        -   Version data is populated for the operating system record in the Software Installation table. \(PRB2067866\)
        -   Resolved the issue where the EKS Cluster data source returned an error when the enableDbConfigLoad property is set to true.\(PRB2057785\)
        -   Flow execution contexts are created for Get Inventory imports.\(PRB2063614\)
        -   The CloudFormation templates \(CFT\) used by the connector are updated to the latest versions available in SGC Central.\(PRB2071071\)
        -   Resolved the issue where duplicate server records were created because the GetS3Object transform overwrote the Name field.\(PRB2071695\)
        -   Resolved the issue where the isLastImport function in AwsRemovalUtil only checked whether schedule imports were queued. The final import is now detected correctly.\(PRB2060827\)
        -   Resolved the issue where the EKS ETL transformation failed for pod payloads that contained no volume mounts. Such payloads are now transformed successfully.\(PRB2030530\)
        -   Server records aren’t created for AWS Systems Manager \(SSM\) managed instances.\(PRB2032936\)
        -   Resolved the issue where an EKS full schedule import didn’t import EKS data when the sn\_aws\_integ.eks\_document\_processing\_time property is set to 100.\(PRB2071475\)
        -   The deprecated Status field is removed from the ETL mapping for the SG-AWS-Service-Account data source. \(PRB2039925\)
-   **Version 2.14.0 - June 2026**
    -   New:
        -   Implemented new licensing model changes for Docker container.
        -   Implemented AutoScaling groups resource type.
    -   Fixed:
        -   Resolved a test connection failure in SG-AWS version 2.13.0 that prevented successful connectivity validation.
        -   Resolved the issue where duplicate data was added to the staging table when the enableDbConfigLoad property is set to true.
        -   Resolved the issue where duplicate records were created due to inconsistent Object ID values for generic resources.
-   **Version 2.13.0 - March 2026**
    -   Changed:
        -   The SG-AWS-RunPowerShellScript data source now uses Get-CimInstance commands instead of WMIC for Windows Server 2025 discovery.
        -   Resource type-based parallelism is used instead of account-based for parallel loading, improving performance for large-scale environments.
    -   Fixed:
        -   The CreateServiceNowUser.yml file loads in AWS cloud discovery without script errors.
        -   The SG-AWS-Organization pattern correctly retrieves Organization Account details.
        -   The AWS-Tags data source handles large datasets.
        -   EC2 to Storage Volume relationships are populated correctly in the CMDB.
        -   The performance of generic resource import is improved for large data loads.
        -   SSM-GetS3Object data collection enables consistent Running Processes refresh on servers.
        -   The SG-AWS-EKS-FULL scheduled import job loads all EKS data without transformation errors.
        -   Server name is updated when EC2 privateDnsName value changes.
        -   The SG-AWS-EKS-FULL job loads EKS data without the "String object would exceed maximum permitted size" error.
        -   Service Account is retired correctly during record removal.
        -   SgGetInventoryDataSourceUtils definition is now available.
        -   The Image-Id datasource no longer has cross-account access by assuming roles.
        -   Service Account credential mapping is removed.
        -   The performance of the SendCommand datasource is improved.
-   **Version 2.12.1 - October 2025**

    Fixed

    -   Duplicate SQL instances: Resolved an issue where duplicate MSFT SQL instances and application CI relationships were created via the SG-AWS integration.
    -   Record removal logs: Fixed inconsistent return values that caused undefined counts in the logs generated by the record removal utility.
    -   Generic tag SNK: Corrected the Source Native Key \(SNK\) for generic tag resources.
    Changed: Restricted menu items: Added admin-restricted AWS menu items to the Service Graph Connectors application menu.

-   **Version 2.11.0 - August 2025**
    -   New: AWS tag ingestion: Added support for the ingestion of tags for AWS Generic Resources using the SGC-AWS data source.
    -   Changed:
        -   Updated the sys\_id of the YAML on the AWS Create connection page in SGC Central.
        -   Enhanced CMDB discovery for numerous AWS classes:
            -   Service Account, Cloud Subnet, Cloud Resource, Security Group, Hardware Template, Docker Container, and Docker Images
            -   Network, NIC, Images, Storage Mapping, and VM Instance
            -   DynamoDB, Endpoint Vnic, IP Address, and Kubernetes Clusters
            -   Cloud Gateway, Cloud Hardware Type, Cloud LB, and Cloud Object Storage
            -   Availability Zone and Cloud DB
-   **Version 2.10.1 - May 2025**
    -   New:
        -   Introduced support for Amazon Redshift database.
        -   Implemented IMDSv2 support for security compliance.
    -   Changed:
        -   Improved Server Record Accuracy with IP-based discovery when deep discovery is enabled.
        -   Modified the table mappings for the Cloud OS image for improved flexibility in managing cloud OS images.
    -   Fixed: Updated the server record to use the server hostname for the name attribute, preventing merge issues caused by IP address reuse.
-   **Version 2.9.0 - February 2025**
    -   New:
        -   Introduced multi-threading for faster deletion of most Configuration Items \(CIs\).
        -   Optimized oversized payloads to improve performance and reduce loading time.
        -   Enhanced SendCommand functionality to automatically populate critical database attributes into corresponding CIs in the CMDB.
        -   Aligned with Cloud Discovery for comprehensive hardware type information in the CMDB.
    -   Changed: Upgraded the netstat command functionality for compatibility with various Linux distributions.
-   **Version 2.8.0 - October 2024**

    New: Addressed the gap for missing life cycle management of configuration items \(CIs\).

-   **Version 2.7.1 - September 2024**

    Fixed: SGC Central - AWS EKS EC2 resources page was updated.

-   **Version 2.7.0 - August 2024**
    -   New:
        -   Enabled parallel loading feature for SG-AWS-Tags and SG-AWS-Image-Private data sources.
        -   Added relationship between availability zones and virtual machines.
        -   Implemented support for VPC and subnet sharing across service accounts.
    -   Fixed:
        -   Fixed an issue in multi-instance setups where EC2, VPC, or subnet configuration items \(CIs\) were marked as retired after upgrading the connector to version 2.6.0 or later versions.
        -   Added the mapping of the Fully Qualified Domain Name \(FQDN\) value to the fqdn field.
        -   Added an appropriate error message in the diagnostic results when a test fails due to an incorrect AWS region configuration property.
        -   Fixed inconsistency between the "State" and "Install Status" fields.
        -   Fixed application of the SG-AWS-EC2 post-script changes for the existing multi-instance records.
-   **Version 2.6.1 - May 2024**
    -   New:
        -   SG-AWS-Software-Inventory data sourcememory improvements
        -   Performance improvement for fetching tags
        -   The connector now avoids calling the SG-AWS-SendCommanddata source when the details for the S3 buckets are not populated
    -   Fixed:
        -   FixedHardware consolidation data source functionality for multi-instance connections
        -   Fixed the diagnostic tool for testing the S3 bucket setup
        -   Fixed empty software names causing partial payload in the SG-AWS-Software-Inventory data source
-   **Version 2.4.0 - February 2024**
    -   New:
        -   Added support for additional attributes in Cloud organization Unit, Cloud organization, Cloud Service Account, and Account Tags for ITOM Cloud Account Management.
        -   Populated reference to "Configuration Item" in the Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]table for all VMs.
    -   Fixed:
        -   Fixed the 'beyond the size limit' issue raised by the Flow Designer action for Software Inventory and EKS.
        -   Fixed data inconsistencies for EKS.
-   **Version 2.3.0 - November 2023**
    -   New:
        -   Added ability to populate the generic cloud resources without CMDB classes to the Cloud Resource \[cmdb\_ci\_cmp\_resource\] table.
        -   Added database deep discovery for virtual machines \(VMs\) to fetch metadata such as MySQL version numbers for databases in the EC2 instances.
        -   Implemented bringing your own license \(BYOL\) that updates the license type in the Key Value \[cmdb\_key\_value\] table to analyze licenses.
        -   Optimized deletion strategy.
        -   Added support for handling retired CIs in EKS components \(pods, services, volumes, and so on.\)
        -   Scoped IAM permissions and fixed S3 permissions following least privilege principles.
    -   Fixed:
        -   Fixed the infinite loop issue in the SG-AWS-Software-Inventory data source .
        -   Fixed the in-use status from SG-AWS-Network-Interface data source not mapping to the In Use column in the Cloud Mgmt Network Interface \[cmdb\_ci\_nic\] table.
-   **Version 2.2.1 - September 2023**
    -   Fixed:
        -   Populate Name for Kubernetes Namespace records.
        -   Fixed the relationship between Cloud Management N/W Interface and virtual machines.
        -   If database name isn't set in AWS then use objectid to map name in the Cloud Database.
-   **Version 2.2.0 - August 2023**
    -   New:
        -   Added Elastic Kubernetes Service \(EKS\)discovery
        -   Added ability to populate EC2 hostname via sendcommand
        -   The STS AssumeRole API is now called only for accounts that are associated with the AWS Config aggregator and not for all member accounts
-   **Version 2.1.0 - July 2023**

    Fixed: Issues related to support AWS GovCloud regions.

-   **Version 2.0.0 - May 2023**
    -   New:
        -   Added support for multi-organization \(multi-instance\)
        -   Single or standalone account support
        -   AWS key rotation
        -   Server classification
    -   Changed: Performance improvement on the deleted resources and the Tag API
-   **Version 1.6.1 - December 2022**
    -   Fixed:
        -   Handle the throttling error on calling Config and List API.
        -   Fix the ListAccounts error when ServiceNow user is created in a designated account.
        -   Handle the duplicate records created with cloud discovery.
        -   DescribeImage API wasn't handling the large payload.
        -   Fixed Software inventory empty import records when the central aggregator isn't setup.
-   **Version 1.5.0 - August 2022**
    -   Fixed:
        -   Remove designated account dependency on the management account.
        -   Added missing CIs attributes.
        -   Optimized performance.
-   **Version 1.4.2 - June 2022**
    -   New: Get the list of accounts from designated accounts by setting up IAM permissions that are necessary to go to the management account.
    -   Fixed:
        -   Fixed missing hardware and server attributes
        -   Optimized sendCommand processing
-   **Version 1.4.1 - May 2022**
    -   New:
        -   Add Serial Number in to cmdb\_ci\_server
        -   Add Process Info and relate it to cmdb\_ci\_server
        -   Add TCP connections to cmdb\_ci\_server
        -   Add Cloud Formation Template \(CFT\) to include SSM Document for SG-AWS-RunShellScript, SG-AWS-RunPowerShellScript
        -   Update serviceNow user CFT script to include privileges for SSM SendCommand, S3 access.

