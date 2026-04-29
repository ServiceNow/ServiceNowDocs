---
title: Software Asset Management Foundation plugin software discovery and normalization
description: ServiceNow Discovery is used to automatically populate the Software Installations table so the software can be manually normalized and reconciled.
locale: en-US
release: australia
product: Software Asset Management Foundation plugin
classification: software-asset-management-foundation-plugin
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring Software Asset Management Foundation plugin, Software Asset Management Foundation plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Software Asset Management Foundation plugin software discovery and normalization

ServiceNow Discovery is used to automatically populate the Software Installations table so the software can be manually normalized and reconciled.

The discovery process consists of automatically discovering software used at your organization, which can be done either using ServiceNow Discovery, or using SCCM integration.

For more information, see [Collect software data with either SCCM or Discovery](https://www.servicenow.com/docs/access?context=c_DiscoveryAndSCCMTogether&version=australia&pubname=australia-it-operations-management&section=collect-software-data-sccm-disco&ft:locale=en-US) and [Discovery with Software Asset Management](https://www.servicenow.com/docs/access?context=c_DiscoSWAssetMgmtTableSchema&version=australia&pubname=australia-it-operations-management&ft:locale=en-US).

**Note:** To use Discovery, the [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&version=australia&pubname=australia-it-operations-management&ft:locale=en-US) must be activated.

Discovery uses patterns in the discovery process that can be created or customized. The base system contains a wide range of patterns that cover most industry standard network devices and applications. Software Asset Management Foundation plugin automatically leverages SQL Server, Exchange Server, and Oracle Database Server specifically, but other patterns can be customized for use by Software Asset Management Foundation plugin, if needed.

Discovered software is stored in the Software Installations \[cmdb\_sam\_sw\_install\] table.

**Note:** If you are already running Discovery but have not used a version of ITSM Software Asset Management previously, run the [Migrate Software Asset Management Foundation plugin software installations](../task/t_MigrateSWInstallsSAMF.md) script to copy records from the \[cmdb\_ci\_spkg\] table to the \[cmdb\_sam\_sw\_install\] table, so that any previously discovered software installs are utilized by Software Asset Management Foundation plugin.

When software install records are written to the Software Installations table, a business rule verifies whether the unique combination of the discovered publisher, discovered product, and discovered version already exist in the Discovery Model table.

-   If so, the reference to the discovery model is set in the Software Installations table.
-   If not, a new record is created in the Discovery Model table, and that discovery model reference is set in the Software Installations table.

After discovery, you can [manually normalize](../task/t_EditASoftwareDiscModelSAMF.md) the software discovery model for reconciliation. Normalization status can have two different results:

|Status|Description|
|------|-----------|
|Manually Normalized|A discovery model is manually normalized when key fields in the discovery model are filled in manually.|
|New|The software discovery model has not yet been manually normalized.|

**Parent Topic:**[Exploring Software Asset Management Foundation plugin](exploring-sam-foundation.md)

