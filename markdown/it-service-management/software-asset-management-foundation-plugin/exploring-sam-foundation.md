---
title: Exploring Software Asset Management Foundation plugin
description: Starting with the Zurich release, we have enhanced the Software Asset Management Foundation plugin application's user interface to make it more user-friendly and intuitive, allowing you to better manage your software installations.
locale: en-US
release: zurich
product: Software Asset Management Foundation plugin
classification: software-asset-management-foundation-plugin
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Software Asset Management Foundation plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Exploring Software Asset Management Foundation plugin

Starting with the Zurich release, we have enhanced the Software Asset Management Foundation plugin application's user interface to make it more user-friendly and intuitive, allowing you to better manage your software installations.

You can use the new Software Asset Management Foundation plugin user interface, referred to as Software Asset Workspace or continue using the classic Software Asset Management Foundation plugin framework.

The Software Asset Management Foundation plugin application's core functionality remains the same in both the user interfaces.

## Using the Software Asset Workspace

Once you request and activate the Software Asset Management Foundation plugin \(com.snc.sams\), you need to activate the Software Asset Workspace \(sn\_sam\_workspace\) store application too.

**Note:** Once you activate the workspace plugin, you cannot revert to the classic Software Asset Management Foundation plugin application.

For detailed information on configuring and using the Software Asset Workspace, refer to [Configuring Software Asset Management Foundation plugin workspace](configuring-samf-plugin-workspace.md) and [Using Software Asset Management Foundation plugin workspace](using-samf-workspace.md).

## Using the classic Software Asset Management Foundation plugin application

To continue using the classic Software Asset Management Foundation plugin application, just activate the Software Asset Management Foundation plugin \(com.snc.sams\) plugin.

If you later decide to use the Software Asset Workspace, you need to activate the Software Asset Workspace \(sn\_sam\_workspace\) store application.

For detailed information on configuring and using the classic Software Asset Management Foundation plugin application, refer to [Configuring the classic Software Asset Management Foundation plugin](samf-plugin-configuration.md) and [Using Software Asset Management classic](https://www.servicenow.com/docs/access?context=using-sam-classic&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US).

-   **[Software Asset Management Foundation plugin roles](../reference/r_SAMRolesSAMF.md)**  
Software Asset Management Foundation plugin adds the following roles.
-   **[Software Asset Management Foundation plugin software discovery and normalization](c_SAMDiscoverySAMF.md)**  
ServiceNow Discovery is used to automatically populate the Software Installations table so the software can be manually normalized and reconciled.
-   **[Software Asset Management Foundation plugin discovery models and software installations](c_DiscoveryModelsSAMF.md)**  
Software discovery models are automatically created during discovery so you can manually normalize the software installed in your environment.
-   **[Software Asset Management Foundation plugin software reconciliation for compliance](c_SAMReconciliationSAMF.md)**  
Automated license reconciliation keeps license positions accurate and up to date without manual calculations. Reconciliation runs weekly or on demand.

**Parent Topic:**[Software Asset Management Foundation plugin](c_SoftwareAssetMgmtSAMF.md)

