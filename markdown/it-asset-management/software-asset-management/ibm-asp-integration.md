---
title: Authorized SAM Provider \(ASP\) integrations for IBM
description: You can track and manage IBM licenses in both VMware vSphere environments and IBM LPAR infrastructures by integrating the Software Asset Management publisher pack for IBM with Software Asset Management providers that are authorized to participate in the IBM Client Value Acceleration \(CVA\) Program. With these integrations, you can track and manage IBM licensing directly without having to integrate with the IBM License Metric Tool \(ILMT\) or BigFix Inventory.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Authorized SAM Provider \(ASP\) integrations for IBM

You can track and manage IBM licenses in both VMware vSphere environments and IBM LPAR infrastructures by integrating the Software Asset Management publisher pack for IBM with Software Asset Management providers that are authorized to participate in the IBM Client Value Acceleration \(CVA\) Program. With these integrations, you can track and manage IBM licensing directly without having to integrate with the IBM License Metric Tool \(ILMT\) or BigFix Inventory.

The CVA Program is an invitation-only license verification program that allows clients who contract with Authorized SAM Providers \(ASPs\) to report on their IBM license usage independently. For more information on the CVA Program, see [CVA Program Verification](https://www.ibm.com/about/software-licensing/verification/cva_program).

**Important:** As of January 1, 2025, IBM has withdrawn its IBM Authorized SAM Provider \(IASP\) Program and replaced it with the CVA Program. If you are an existing IASP Program user, contact your IBM representative to upgrade to the new CVA agreement and migrate to the CVA Program.

The IBM publisher pack supports integrations with the following ASPs:

-   Anglepoint \(through the Anglepoint Elevate platform\)
-   Deloitte
-   EY
-   KPMG

To integrate with an ASP, you must request and install the IBM License Compliance for Software Asset Management application from the ServiceNow® Store. This application provides the core functionality and license metrics that are required for tracking and managing IBM licensing directly. If you are integrating with Anglepoint, you must also request and install Anglepoint's IBM Licensing for Software Asset Management application from the ServiceNow® Store. This application enables you to store IBM software information from Anglepoint.

After you install the necessary applications, you must retrieve the IBM software discovery catalog from the ASP that you are integrating with. This catalog, which is maintained separately by each ASP, is a centralized repository of IBM software information that discovery tools, such as the ServiceNow® Discovery application, can use to identify the IBM software that is discovered in your environment. After you retrieve the catalog, you must upload it to your ServiceNow instance.

On successful upload, you can use the ServiceNow Discovery application to run a discovery for your IBM software. The Discovery application uses the uploaded catalog to identify any IBM software that is discovered in your environment. It then sends this data to the ASP for comprehensive software classification and bundling.

After your discovered IBM software is properly classified and bundled, the ASP sends this data back to your ServiceNow® instance. The Software Asset Management application can then use the processor value unit \(PVU\), resource value unit \(RVU\), and virtual processor core \(VPC\) license metrics to reconcile this data so that you can track your IBM software usage and optimize your licensing costs. For more information on the PVU and RVU license metrics, see [IBM processor value unit \(PVU\) and resource value unit \(RVU\) licenses](ibm-pvu-rvu-licensing.md). For more information on the VPC license metric, see [IBM virtual processor core \(VPC\) licenses](ibm-virtual-processor-core-licensing.md).

## Prerequisites

Before you can integrate the IBM publisher pack with an ASP, you must complete the following prerequisites:

-   Complete all prerequisites for participating in the CVA Program. For more information on these prerequisites, refer to the How it works section of [CVA Program Verification](https://www.ibm.com/about/software-licensing/verification/cva_program).
-   Request and install the IBM License Compliance for Software Asset Management application from the ServiceNow® Store. See [Request the IBM License Compliance for Software Asset Management application for Authorized Software Asset Management Provider \(ASP\) integrations](../task/request-ibm-license-compliance-sam-application.md) for detailed instructions.
-   Enable the **Use ServiceNow Software Asset Management and Discovery for IBM license compliance** \(**com.snc.samp.ibm.use\_samp\_ibm\_licensing**\) Software Asset Management property. See [Software Asset Management properties](../reference/sam-properties.md) for more information on this property.
-   Activate the Discovery \(com.snc.discovery\) plugin on your ServiceNow instance. See [Request Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/t_ActivateTheDiscoveryPlugin.md) for detailed instructions.
-   Activate the File-based Discovery \(com.snc.discovery.file\_based\_discovery\) plugin on your ServiceNow instance. See [File-based Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/file-based-discovery.md) for more information on file-based Discovery.
-   Request and install the Discovery and Service Mapping Patterns application from the [ServiceNow Store](https://store.servicenow.com/). See [Discovery patterns used by ITOM Visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/c_MappingPatternsCustomization.md) for more information on Discovery and Service Mapping patterns.
-   If you want to use domain separation for the integration, activate the Domain Support - Domain Extensions Installer \(com.glide.domain.msp\_extensions.installer\) plugin on your ServiceNow instance. See [Domain separation plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-plugin.md) for detailed instructions.
-   Download the IBM software discovery catalog from the ASP.
-   If you want to track and manage IBM licensing in public cloud environments, configure one or more for the following services to automatically scan for and update the CMDB with cloud infrastructure changes every 30 minutes:
    -   For public clouds hosted by AWS, configure the AWS Config service. See [Configure the AWS Config service to send event notifications to the ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/aws-config-service-cloud-mgt.md) for detailed instructions.
    -   For public clouds hosted by Microsoft Azure, configure the Microsoft Azure Alert service. See [Configure the Microsoft Azure Alert service to auto-update the CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/microsoft-azure-alert-driven-discovery.md) for detailed instructions.
    -   For public clouds hosted by Google Cloud Platform \(GCP\), configure the Google Cloud Logging service. See [Configure the Google Cloud Logging service to auto-update the CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/gcp-stackdriver-service.md) for detailed instructions.

If you are integrating the IBM publisher pack with Anglepoint, you must also complete these additional prerequisites:

-   Request and install Anglepoint's IBM Licensing for Software Asset Management application from the ServiceNow® Store. See [Request Anglepoint's IBM Licensing for Software Asset Management application](../task/request-anglepoint-application.md) for detailed instructions.
-   Set up the Anglepoint Elevate platform.

-   **[Virtualization technologies and public cloud platforms supported by IBM Authorized SAM Provider \(ASP\) integrations](supported-virtualization-technologies-iasp-integrations.md)**  
IBM ASP integrations support IBM licensing in VMware vSphere environments and IBM LPAR infrastructures.These integrations also support IBM licensing in public cloud environments that are owned and managed by AWS, Microsoft Azure, and Google Cloud Platform \(GCP\).
-   **[Licensing for IBM Cloud Paks](licensing-ibm-cloud-paks.md)**  
When you integrate the Software Asset Management publisher pack for IBM with Software Asset Management providers that are authorized to participate in the IBM Client Value Acceleration \(CVA\) Program, the Software Asset Management application supports licensing rules for IBM Cloud Paks.
-   **[IBM reconciliation for IBM Authorized SAM Provider \(ASP\) integrations](ibm-reconciliation-iasp-integrations.md)**  
IBM reconciliation keeps your IBM license positions accurate and up-to-date without requiring manual calculations. Reconciliation runs weekly or on-demand.
-   **[Setting up an IBM Authorized SAM Provider \(ASP\) integration](setting-up-anglepoint-integration.md)**  
Before you can integrate the Software Asset Management publisher pack for IBM with an Authorized SAM Provider \(ASP\), complete the setup process.
-   **[Creating a connection for the Anglepoint integration](creating-connection-anglepoint-elevate-platform.md)**  
If you are integrating the Software Asset Management publisher pack for IBM with Anglepoint, you can create a connection between your ServiceNow instance and the Anglepoint Elevate platform to transfer licensing data for your IBM software products.
-   **[View the daily aggregated peak usage of your IBM software products](../task/view-daily-aggregated-peak-usage-ibm-products.md)**  
View the highest daily sub-capacity and full capacity Processor Value Unit \(PVU\), Resource Value Unit \(RVU\), and Virtual Processor Core \(VPC\) usage for your IBM software products based on the edition, license metric, and region of each product.
-   **[View devices with the highest daily usage of your IBM software products](../task/view-daily-high-water-mark-usage-ibm-products.md)**  
View the breakdown for the highest daily usage of your IBM software products by physical host based on both the edition and license metric of each product.
-   **[View product classifications for your IBM components](../task/view-product-classifications-ibm-components.md)**  
View the product classifications for all IBM components that are installed in your environment. These product classifications enable you to track and manage licensing for your IBM components.
-   **[Specify the virtual machine managers \(VMMs\) for which you are tracking IBM licenses](../task/specify-vm-managers-anglepoint-integration.md)**  
Specify the virtual machine managers \(VMMs\), such as VMware vCenter Servers and IBM Hardware Management Consoles \(HMCs\), for which you want to track IBM licenses. You can track licenses for IBM software that is discovered within these specified VMMs only.
-   **[Deduplicating IBM software installations](deduplicating-ibm-software-installations.md)**  
To manage your IBM licenses, you can integrate the IBM publisher pack with an Authorized SAM Provider \(ASP\), IBM License Metric Tool \(ILMT\), or BigFix Inventory. If you are switching between an ASP integration and either an ILMT or BigFix Inventory integration, you can deduplicate software installations that have the same edition, version, and language but are discovered through different sources.
-   **[Enable IBM reconciliation for specific domains](../task/enable-domain-recon-anglepoint-integration.md)**  
If you are using domain separation for the integration between the Software Asset Management publisher pack for IBM and an Authorized SAM Provider \(ASP\), enable IBM reconciliation only for specific domains.
-   **[Verify the meta data for your IBM hosts](../task/verify-ibm-device-meta-data.md)**  
To improve the accuracy of your IBM license calculations, verify the meta data for the physical hosts that your IBM software is installed on. Update any meta data that is incorrect or out of date.

**Parent Topic:**[Software Asset Management publisher pack for IBM](ibm-publisher-pack.md)

