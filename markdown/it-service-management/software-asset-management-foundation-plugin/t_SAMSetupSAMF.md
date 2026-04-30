---
title: Setting up Software Asset Management Foundation plugin
description: Set up Software Asset Management Foundation plugin before configuration.
locale: en-US
release: zurich
product: Software Asset Management Foundation plugin
classification: software-asset-management-foundation-plugin
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Software Asset Management Foundation plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Setting up Software Asset Management Foundation plugin

Set up Software Asset Management Foundation plugin before configuration.

## Before you begin

Role required: sam\_admin

## About this task

Once you have [requested](t_RequSoftwareAssetMgmtSAMF.md) Software Asset Management Foundation plugin and it has been activated from ServiceNow personnel, complete these steps to set up Software Asset Management Foundation plugin before you begin to use it.

## Procedure

1.  Determine whether you are currently running the ITSM Software Asset Management feature of Asset Management using the [Legacy Software Asset Management plugin](../../asset-management/concept/c_SoftwareAssetManagement.md).

    Check the list of plugins to see if the Software Asset Management \(com.snc.software\_asset\_management\) plugin is active.

    -   If so, complete the [Software Asset Management Foundation plugin migration](../concept/c_SAMMigrationSAMF.md) procedure.

        This step automatically converts and adds new tables, forms and lists, fields and values, and disables deprecated functionality. It also contains manual procedures for you to complete for successful migration.

    -   If not, proceed to the next step.
2.  Determine whether Discovery is activated \(see [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)\).

    Check the list of plugins to see if the Discovery plugin is active.

    -   If so, run the [Migrate Software Asset Management Foundation plugin software installations](t_MigrateSWInstallsSAMF.md) script.

        This step copies records from the \[cmdb\_ci\_spkg\] table to the \[cmdb\_sam\_sw\_install\] table, so that any previously discovered software installs are utilized by the Software Asset Management Foundation plugin.

    -   If not, activate and configure Discovery.

        For more information, see [Discovery](https://www.servicenow.com/docs/access?context=r-discovery&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).

3.  Proceed to [Get started with Software Asset Management Foundation plugin](t_SAMGetStartedSAMF.md) to begin using the Software Asset Management Foundation plugin in your environment.


-   **[Request Software Asset Management Foundation plugin](t_RequSoftwareAssetMgmtSAMF.md)**  
The Software Asset Management Foundation \(com.snc.sams\) plugin must be activated by ServiceNow personnel. This plugin includes demo data.
-   **[Manage a SAM Foundation software suite](../concept/manage-samf-software-suite.md)**  
Create a suite and add the corresponding components to the suite so the rights that your organization owns are counted accurately during reconciliation.
-   **[Customize a Discovery pattern for Software Asset Management Foundation plugin](t_CustomPatternSAMSAMF.md)**  
Software Asset Management Foundation plugin automatically leverages SQL Server, Exchange, and Oracle Database Discovery patterns, but you can perform steps for Software Asset Management Foundation plugin to utilize additional Discovery patterns, if needed.
-   **[Get started with Software Asset Management Foundation plugin](t_SAMGetStartedSAMF.md)**  
Get started with Software Asset Management Foundation plugin to optimize management of software installations in your environment.

**Parent Topic:**[Software Asset Management Foundation plugin](../concept/c_SoftwareAssetMgmtSAMF.md)

