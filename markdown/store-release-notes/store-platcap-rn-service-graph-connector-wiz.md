---
title: Service Graph Connector for Wiz release notes
description: Version history for the Service Graph Connector for Wiz on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-service-graph-connector-wiz.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Service Graph Connector for Wiz release notes

Version history for the Service Graph Connector for Wiz on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.5.0 - March 2026**

    Fixed: Fixed the issue that was causing partial payloads in delta pulls when a resource was created and deleted in a very short time.

-   **Version 1.4.0 - November 2025**
    -   New:
        -   Added Gateway Data source that brings AWS Egress Only Internet Gateway and AWS VPN Gateway information.
        -   Support for OCI cloud resources:
            -   Subscription: OCI Compartment
            -   Region: OCI Region
            -   Firewall: Network Security Group and OCI Security List
            -   Virtual Machine: OCI Compute Instance
        -   Support for Alibaba cloud resources:
            -   Subscription: Alibaba Account
            -   Region: Alibaba Region
            -   Virtual Machine: Alibaba ECS Instance
        -   Support for vSphere cloud resources:
            -   Subscription: vSphere Datacenter
            -   Region: vSphere Datacenter
            -   Virtual Machine: vSphere Virtual Machine
        -   Flexibility to drop Scale set VMs
        -   Flexibility to by-pass server creation and mapped VM to existing server records
    -   Fixed:
        -   Migrated data from Hardware Type \(cmdb\_ci\_compute\_template\) to Cloud Hardware Type \(cmdb\_ci\_cloud\_hardware\_type\) table through "sn\_itom\_pattern.use a single hardware type for cloud data centers" system property.
        -   Removed container-pod relationship and created container-cluster relationship instead
        -   Updated Dynamo DB object\_id to ARN
        -   Mapped cluster\_id of AWS Cloud Database cluster with ARN
        -   Mapped object\_id of AWS Compute Instance Group with ARN
        -   Mapped object\_id of AWS Cloud Gateway with gateway id
        -   Fixed Container ID from docker container
        -   Fixed the server classification defect
        -   Mapped vm\_instance\_id for Azure VMs to uuid
        -   Mapped object\_id of AWS Cloud Public IP Address with providerUniqueId attribute
-   **Version 1.3.0 - May 2025**
    -   New:
        -   Support for Azure Scale Set VM and AWS Autoscale.
        -   Container data for AWS and Azure.
        -   Support for Kubernetes Clusters.
    -   Fixed:
        -   Fixed Object ID to match ARN in uniformity with SGC for AWS.
        -   Updated Dynamo DB name mapping with name attribute instead of externalID.
        -   Minor fixes in VM-compute instance group relation condition in VM-ETL.
        -   Removed the active check field from the script execution script.
        -   Updated Kubernetes Clusters IDs according to SGC for GCP.
-   **Version 1.2.0 - February 2025**
    -   Fixed:
        -   Bug fixes
        -   Performance enhancements
        -   Resolved an incorrect relationship between Server and Virtual Machine
-   **Version 1.1.0 - August 2024**
    -   New: Added support for Google Cloud Platform \(GCP\) resources.
    -   Fixed: Fixed partial payload for the SG-Wiz-Network-Interface data source.
-   **Version 1.0.2 - May 2024**
    -   The Service Graph Connector for Wiz is a fast lane to cloud security value.
    -   Wiz employs agentless, read-only scanning via API to get visibility to your cloud including AWS, Azure, and the Google Cloud Platform, to which it adds industry-leading security insights.
    -   The ServiceNow Service Graph Connector for Wiz harvests those details and insights, harmonizes them with other sources of cloud data, and makes all that intelligence accessible to our trusted workflows for incident response and service management, IT operations, and--of course--Security Operations.

