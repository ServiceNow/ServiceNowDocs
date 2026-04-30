---
title: Bring your own license or subscription to the public cloud
description: Bring your own license \(BYOL\) support enables you to determine the license compliance of your Microsoft and Oracle software products across hybrid infrastructures. Bring your own subscription \(BYOS\) support enables you to determine the license compliance of your Red Hat Enterprise Linux \(RHEL\) software products across hybrid infrastructures.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Explore, Software Asset Management, IT Asset Management]
---

# Bring your own license or subscription to the public cloud

Bring your own license \(BYOL\) support enables you to determine the license compliance of your Microsoft and Oracle software products across hybrid infrastructures. Bring your own subscription \(BYOS\) support enables you to determine the license compliance of your Red Hat Enterprise Linux \(RHEL\) software products across hybrid infrastructures.

When organizations move to the public cloud, existing on-premise perpetual licenses are carried over to the cloud using BYOL. Existing on-premise subscription licenses are also carried over to the cloud using BYOS. BYOL and BYOS help improve license optimization, as organizations must pay only for infrastructure costs.

The Software Asset Management application supports BYOL for Microsoft and Oracle software products and BYOS for RHEL software products as follows:

**Note:** `The Supported infrastructure type column in the following table applies to Infrastructure as a Service (IaaS) models only.`

<table id="table_dh3_w2x_cbc"><thead><tr><th>

Product

</th><th>

Product edition

</th><th>

BYOL or BYOS

</th><th>

Supported cloud providers

</th><th>

Supported service model

</th><th>

Supported infrastructure type

</th></tr></thead><tbody><tr><td>

Microsoft SQL Server

</td><td>

All editions

</td><td>

BYOL

</td><td>

-   AWS
-   Microsoft Azure
-   Google Cloud Platform \(GCP\)

</td><td>

Infrastructure as a Service \(IaaS\)

</td><td>

Shared and dedicated

</td></tr><tr><td>

Microsoft Windows Server

</td><td>

All editions

</td><td>

BYOL

</td><td>

-   AWS
-   Microsoft Azure
-   Google Cloud Platform \(GCP\)

</td><td>

Infrastructure as a Service \(IaaS\)

</td><td>

Shared and dedicated

</td></tr><tr><td>

Oracle Database

</td><td>

-   Oracle Database Standard Edition
-   Oracle Database Standard Edition One
-   Oracle Database Standard Edition 2
-   Oracle Database Enterprise Edition

</td><td>

BYOL

</td><td>

-   AWS
-   Microsoft Azure

</td><td>

-   AWS: Infrastructure as a Service \(IaaS\) and Platform as a Service \(PaaS\)

**Note:** In AWS, the IaaS model refers to the Amazon Elastic Computing \(EC2\) web service, while the PaaS model refers to the Amazon Relational Database Service \(RDS\).

-   Microsoft Azure: Infrastructure as a Service \(IaaS\)

</td><td>

Shared and dedicated

</td></tr><tr><td>

Oracle Weblogic Server

</td><td>

-   Oracle WebLogic Server Standard Edition
-   Oracle WebLogic Server Enterprise Edition

</td><td>

BYOL

</td><td>

-   AWS
-   Microsoft Azure

</td><td>

Infrastructure as a Service \(IaaS\)

</td><td>

Shared and dedicated

</td></tr><tr><td>

Red Hat Enterprise Linux Server

</td><td>

All editions

</td><td>

BYOS

</td><td>

-   AWS
-   Microsoft Azure
-   Google Cloud Platform \(GCP\)

</td><td>

Infrastructure as a Service \(IaaS\)

</td><td>

Shared

</td></tr></tbody>
</table>BYOL and BYOS support on the Software Asset Management application help you:

-   Discover perpetual and subscription-based software licenses automatically across on-premise and cloud environments, such as AWS, Microsoft Azure, and GCP.
-   Determine the license compliance of the following software products across your hybrid infrastructure:
    -   Microsoft SQL Server
    -   Microsoft Windows Server
    -   Oracle Database
    -   Oracle WebLogic Server
    -   Red Hat Enterprise Linux Server
-   Provide advanced support for optimization through Cloud Special Rights, such as dual use rights, edition flexibility, and unlimited virtualization.
-   Perform remediation when your software is out of compliance.

![Flowchart for BYOL and BYOS, starting with ServiceNow Discovery and ending with remediation.](../image/byol.png "Bring your own license or subscription flow")

## Prerequisites

Before you can begin determining the license compliance of software across your hybrid infrastructures, you must complete the following prerequisites:

-   Activate the Discovery \(com.snc.discovery\) plugin on your ServiceNow instance.

    See [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) for detailed instructions.

-   Request and install the Discovery and Service Mapping Patterns application from the [ServiceNow Store](https://store.servicenow.com/).

    See [Discovery patterns used by ITOM Visibility](https://www.servicenow.com/docs/access?context=c_MappingPatternsCustomization&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) for more information on Discovery and Service Mapping patterns.

-   Migrate cloud discoveries from Cloud API \(CAPI\) probes to pattern-based discovery.

    See [CAPI to Pattern Migration: Procedure for switching from CAPI-based Cloud Discovery to pattern-based Cloud Discovery \[KB0827153\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0827153) for detailed instructions.

-   Request and install the CMDB CI Class Models application from the [ServiceNow Store](https://store.servicenow.com/).

    See [CMDB CI Class Models store app](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for more information on the CMDB CI Class Models application.

-   Request and install the Cloud Cost Management application from the [ServiceNow Store](https://store.servicenow.com/).

    The Cloud Cost Management application is required for discovering the license types of software in your Microsoft SQL Server deployments on AWS. See [Cloud Insights application](../../cloud-insights/reference/cloud-insights-landing-page.md) for more information on the Cloud Cost Management application.


## BYOL and BYOS discovery

With BYOL and BYOS, the ServiceNow® Discovery application locates and identifies licensable software in both your on-premise and cloud environments using Discovery and Service Mapping patterns. The Discovery application uses Amazon AWS Cloud, Microsoft Azure Cloud, and Google Cloud discovery patterns to discover the following resources for software in cloud environments:

-   Cloud provider
-   Virtual machine details
-   Service model type, such as IaaS or PaaS
-   Host infrastructure type for IaaS, such as shared or dedicated
-   License type, such as BYOL, BYOS, or License Included
-   Software that is installed on the virtual machine

**Note:** The Amazon AWS Cloud, Microsoft Azure Cloud, and Google Cloud discovery patterns are included in the Discovery and Service Mapping Patterns store application. For more information on Amazon AWS Cloud discovery patterns, see [Amazon AWS Cloud components discovery using patterns](https://www.servicenow.com/docs/access?context=data-discovered-aws-patterns&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US). For more information on Microsoft Azure Cloud discovery patterns, see [Microsoft Azure Cloud components discovery using patterns](https://www.servicenow.com/docs/access?context=azure-cloud-discovery-patterns&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US). For more information on Google Cloud discovery patterns, see [Google Cloud Platform \(GCP\) resource inventory discovery with Patterns](https://www.servicenow.com/docs/access?context=gcp-resource-inventory-discovery&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) and [Google Cloud Platform \(GCP\) Organization discovery with Patterns](https://www.servicenow.com/docs/access?context=google-gcp-organization-discovery&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).

Resources for your discovered software are populated and stored in corresponding Configuration Management Database \(CMDB\) tables, including the Host \[cmdb\_ci\_cloud\_host\] and Serverless Hardware \[cmdb\_ci\_serverless\_hardware\] tables, on your ServiceNow instance.

The Software Asset Management application then determines the license types of your discovered software by using Discovery or Cloud Cost Management \(CCM\) data, depending on the software product and cloud provider.

License type determination varies by product and cloud environment, as shown in the following table.

|Product|AWS|Microsoft Azure|GCP|
|-------|---|---------------|---|
|Microsoft Windows Server|Automatic|Automatic|Automatic|
|Microsoft SQL Server|CCM or manual|Automatic|Manual|
|Oracle Database|Automatic|Manual|None|
|Oracle WebLogic Server|Manual|Manual|None|
|Red Hat Enterprise Linux Server|Automatic|Automatic|Automatic|

The Software Asset Management application identifies and applies license types by using the following methods.

-   **Automatic determination using key-value pairs**

    For supported products, the Software Asset Management application automatically determines license types by generating key-value pairs. These key-value pairs are stored in the Key Values \[cmdb\_key\_value\] table. Each key-value pair consists of a **Key** in the **&lt;_software-product_&gt;\_License\_Type\_automatic** format and a **Value** of either **License Included**, **BYOL**, or **BYOS**.

-   **Manual specification using key-value pairs**

    When automatic determination isn't supported, you must manually specify license types by creating key-value pairs in the Key Values \[cmdb\_key\_value\] table with a **Key** of `*software-product*_Server_License_Type` and a **Value** of either `License Included` or `BYOL`. For example, Oracle WebLogic Server requires a key of `Oracle_WebLogic_Server_License_Type`. After you create the key-value pairs, the specified license types apply to the associated configuration items \(CIs\).

-   **Cloud Cost Management–based determination**

    For Microsoft SQL Server on AWS, the Software Asset Management application can determine license types by using billing records from the Cloud Cost Management application.


**Note:** If you do not manually specify a license type for a software product when required, the Software Asset Management application does not license the installation due to insufficient information.

You can use these key-value pairs to determine whether the associated software licenses are using the BYOL, BYOS, or License Included licensing model. The BYOL and BYOS licensing models include license purchasing options such as Azure Hybrid Benefit. The License Included licensing model includes license purchasing options such as Pay As You Go \(PAYG\), SPOT, and On Demand. With the License Included licensing model, the cloud provider is responsible for managing licenses.

**Note:** For Oracle Database, support for the BYOL and License Included licensing models is based on the cloud provider and Oracle Database version that you're using.

-   AWS RDS \(PaaS\): The BYOL licensing model is supported on Oracle Database Standard Edition, Standard Edition One, Standard Edition 2, and Enterprise Edition. The License Included licensing model is supported on only Oracle Database Standard Edition 2.
-   AWS EC2 \(IaaS\): Only the BYOL licensing model is supported.
-   Microsoft Azure \(IaaS\): Only the BYOL licensing model is supported.

## Software reconciliation for BYOL and BYOS license compliance

After your discovered software is marked as BYOL, BYOS, or License Included, reconciliation runs on the software that is marked as BYOL or BYOS. You can then use the resulting information to determine the software compliance across your hybrid infrastructure.

BYOL and BYOS licensing rules can differ for the same software products across different cloud providers. For example, Windows Server has different licensing rules on AWS and on Microsoft Azure. These rules must be combined with existing on-premise rules so that you can determine the complete license compliance position of each software product across your hybrid infrastructures. Microsoft offers special rights for products that are deployed on AWS vs Microsoft Azure, such as dual use rights, edition flexibility, and unlimited virtualization. For more information on licensing rules, see [Licensing rules for BYOL and BYOS](../reference/byol-license-rules.md).

The Software Asset Management application automatically reconciles these rules and provides an accurate license position report that can be viewed in the License usage view of the Software Asset Workspace.

-   You can view BYOL license rights for your Microsoft software products in the Microsoft publisher overview of the Software Asset Workspace. For more information on the Microsoft publisher overview, see [Publisher overview for Microsoft in the Software Asset Workspace](../reference/publisher-overview-microsoft.md).
-   You can view BYOL license rights for your Oracle software products in the Oracle publisher overview of the Software Asset Workspace. You can also view information about your Oracle Database server deployments across hybrid infrastructures, based on the agreement type, in the Oracle DB Server Deployments per Agreement report. For more information on the Oracle publisher overview, see [Publisher overview for Oracle in the Software Asset Workspace](../reference/publisher-overview-oracle.md). For more information on the Oracle DB Server Deployments per Agreement report, see the [Oracle DB Server Deployments per Agreement report](../reference/oracle-server-agreement.md).
-   You can view BYOS license rights for your RHEL software products in the Red Hat publisher overview of the Software Asset Workspace. For more information on the Red Hat publisher overview, see [Publisher overview for Red Hat in the Software Asset Workspace](../reference/publisher-overview-red-hat.md).

## Cloud-based remediation options

To remediate non-compliance for cloud installations, the Software Asset Management application provides the following remediation options:

-   **Remove Unlicensed Installs - Cloud**

    The **Remove Unlicensed Installs - Cloud** remediation option removes all cloud installations that are unlicensed for the associated software product.

    When you select the **Remove Unlicensed Installs - Cloud** remediation option, removal candidates that follow the regular remediation workflow are created. After the removal candidates reach the **Awaiting Revocation** state, you can uninstall the cloud installations from your cloud provider and then mark the removal candidates as complete.

-   **Optimize vCPU**

    The **Optimize vCPU** remediation option provides vCPU sizing optimizations based on the core count and core thread count. This remediation option is applicable only to Oracle Database Per Processor licenses on AWS RDS \(PaaS\). That Per Processor licensing is based on the number of vCPUs on which you install or run an Oracle database.

    For more information on AWS core counts and core thread counts, see [Configuring the processor for a DB instance class](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.DBInstanceClass.html#USER_ConfigureProcessor).


-   **[Microsoft Windows and SQL Server infrastructure details reports](../reference/azure-byol-realized-savings-report.md)**  
You can use the Microsoft Windows and SQL Server infrastructure details reports to gain visibility into the SQL Server and Windows Server deployments and infrastructure for different cloud providers including Microsoft Azure, AWS, and GCP.
-   **[Core infrastructure suite \(CIS\) support for BYOL](cis-byol.md)**  
Use your on-premise CIS entitlements to license Windows Server installations on cloud platforms such as AWS and Microsoft Azure.

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

