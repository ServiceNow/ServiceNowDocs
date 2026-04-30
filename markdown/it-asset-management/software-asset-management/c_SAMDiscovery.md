---
title: Software discovery and normalization
description: After you've imported your entitlements, use ServiceNow Discovery or Microsoft SCCM to discover software installations in your environment and transfer that data into the ServiceNow AI Platform.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Explore, Software Asset Management, IT Asset Management]
---

# Software discovery and normalization

After you've imported your entitlements, use ServiceNow Discovery or Microsoft SCCM to discover software installations in your environment and transfer that data into the ServiceNow AI Platform.

![This graphic provides an overview of how to setup either ServiceNow Discovery or Microsoft SCCM.](../image/mmasset0021825software-discovery-and-normalization.svg "Infographic showing setting up of ServiceNow Discovery or Microsoft SCCM")

While you may use Discovery Home for datacenters and Microsoft SCCM for desktop environments, you can integrate other third-party discovery solutions with CMDB to support Software Asset Management. To integrate a different discovery solution, add it manually, or you can download an application, from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home). For more information about integrating a discovery source manually, see the [Customer Success Center](https://www.servicenow.com/success.html).

To learn more about collecting data after you've integrated with both Discovery and SCCM, see [Collect software data with either SCCM or Discovery](https://www.servicenow.com/docs/access?context=c_DiscoveryAndSCCMTogether&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).

## Discovery integration

ServiceNow Discovery is used to automatically populate the Software Installations table so the software can be normalized and reconciled.

**Note:** To use Discovery, the [Discovery plugin](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) must be activated.

Discovery uses patterns in the discovery process that can be created or customized. The base system contains a wide range of patterns that cover most industry standard network devices and applications. The following are some of the base system patterns used by Software Asset Management.

-   Citrix XenApp
-   Citrix XenDesktop,
-   VMware vCenter
-   Microsoft SQL Server
-   Microsoft Exchange Server
-   Oracle Database Server

You can also customize other patterns for Software Asset Management. For more information, see [Create or modify patterns](https://www.servicenow.com/docs/access?context=t_CreatePatternPatDef&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).

Discovered software is stored in the Software Installations \[cmdb\_sam\_sw\_install\] table.

When software install records are written to the Software Installations table, a business rule verifies whether the unique combination of the discovered publisher, discovered product, and discovered version exist in the Discovery Model table.

-   If so, the reference to the discovery model is set in the Software Installations table.
-   If not, a new record is created in the Discovery Model table, and that discovery model reference is set in the Software Installations table.

After discovery, normalization is run.

For more information on Discovery, see [Discovery with Software Asset Management](https://www.servicenow.com/docs/access?context=c_DiscoSWAssetMgmtTableSchema&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).

## SCCM integration

You can use SCCM by itself or with Discovery Home to identify software on your devices.

**Note:** While you may use Microsoft SCCM for discovering software installations in your desktop environments, you can integrate other third-party tools.

Both Microsoft SCCM 2012 v2 and 2016 plugins are certified with Software Asset Management. The corresponding Microsoft SCCM Integration plugin must be installed to integrate Microsoft SCCM with Software Asset Management.

Microsoft SCCM Integration plugins:

-   Integration — Microsoft SCCM 2012 v2 \(com.snc.integration.sccm2012v2\) plugin
-   Integration — Microsoft SCCM 2016 \(com.snc.integration.sccm2016\) plugin

Microsoft SCCM Software Usage plugins:

-   Integration — Microsoft SCCM 2012 v2 Software Usage \(com.snc.samp\_usage\_sccm\) plugin
-   Integration — Microsoft SCCM 2016 Software Usage \(com.snc.samp.usage\_sccm\_2016\) plugin

The Integration — Microsoft SCCM 2016 plugin is compatible with SCCM versions 1606, 1906, 1910, and 2002.

**Important:** These Microsoft SCCM plugins will be deprecated in the Tokyo release. If you are integrating with SCCM for the first time, request and install the Service Graph connector for Microsoft SCCM application from the [ServiceNow Store](https://store.servicenow.com/) instead. If you have already activated one of the Microsoft SCCM plugins on your ServiceNow instance, use the Migration Readiness Tool for Service Graph Connector for SCCM store application to prepare your instance for migration from the Microsoft SCCM plugin to the Service Graph connector. See [Service Graph connector for Microsoft SCCM](https://www.servicenow.com/docs/access?context=cmdb-integration-sccm&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for more information on the Service Graph connector.

For more information on SCCM and how to import your data into your instance, see [Microsoft SCCM software usage](sccm-software-usage.md).

## Normalization

The normalization process compares the discovered publisher, discovered product, and discovered version and edition values against the ServiceNow repository of normalized equivalents. Matches are added to the corresponding normalized fields \(publisher, product, version, and edition\) of the Discovery Model table. The normalized fields are then used to reconcile entitlements purchased and to compute license positions.

For example, the discovered publisher Microsoft Corp could be normalized to Microsoft for the normalized publisher field.

The normalization process also looks for pattern matches between discovered fields and normalized values, and updates the normalized fields accordingly.

If certain software discovery models share similar discovered field values, the Software Asset Management application normalizes them using wide-net normalization principles, which reduces the need for the Content Service team to create separate normalization rules for each product.

**Note:** Only certain software products are eligible for wide-net normalization. These software products are determined by the Content Service team.

A scheduled job runs to pull in normalized content and pattern updates daily, but you can change the frequency that the schedule job is run. When there are changes to a normalization rule, applicable normalized and partially normalized Discovery models are renormalized with the updated values.

Evaluate suggestions to normalize discovery models that were manually normalized using the [Normalization Suggestions](../task/view-norm-suggestions-sam.md) feature. Suggestions are automatically identified if there is a difference between the updated normalization content and your content. Because the content from the updates contains the most up-to-date information, using the content provided helps to keep your software installs accurate.

You can opt in to the [Software Asset Management Content Service](c_SAMContentService.md) that enables you to provide missed and not fully normalized software discovery models to ServiceNow for research. New content and rules created are provided back to customers to continually improve software normalization.

## Benefits of normalization

-   Normalization creates a definitive list of the discovered software in your organization. Organizations need a thorough inventory of its installed software whether for software audit readiness or IT operations. Without normalization, your organization will be challenged with multiple names for the same publisher, which requires a substantial effort to rationalize and dilutes the accuracy and value of the reports you run.
-   Normalization improves the accuracy and efficiency of reconciliation for your software entitlements. By using the normalized values in the discovery models to map against the software entitlements it has acquired, resulting in more accurate reconciliation results. This makes it easier to plan for and complete software audits knowing that the counts are accurate and that they match the entitlement records.
-   The normalization process allows standardizing installation data from multiple discovery tools.

-   **[Normalization suggestions for discovery models](normalization-suggestions.md)**  
Normalization suggestions are created for all manually normalized discovery models. You can accept or reject these suggestions.
-   **[Normalization of discovery models using machine learning](ml-learning-sam.md)**  
Use machine learning to improve your normalization rates in real time by normalizing your unrecognized discovered software.
-   **[Duplicate software installations in the Software Asset Management application](deduplicating-software-installations-sam.md)**  
Duplicate software installation are created when you discover software installations with the same publisher, product, version, and edition through multiple discovery sources.

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

