---
title: Manage licenses for Microsoft Visual Studio
description: Manage your Visual Studio subscriptions with the Software Asset Management publisher pack for Microsoft. Verify license compliance and detect unlicensed installations. Reduce licensing costs by identifying subscriptions that are allocated but aren’t being used.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Manage licenses for Microsoft Visual Studio

Manage your Visual Studio subscriptions with the Software Asset Management publisher pack for Microsoft. Verify license compliance and detect unlicensed installations. Reduce licensing costs by identifying subscriptions that are allocated but aren’t being used.

## Before you begin

Set up ServiceNow [Discovery](https://www.servicenow.com/docs/access?context=r-discovery&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) to find Microsoft software installations on your network. By using Discovery, you can view license compliance information by comparing your purchased licenses with actual installations.

You must set up the environment on the Configuration Management Database \(CMDB\) before you begin. Setting up of development, production, or test environment helps Software Asset Management Professional to apply licenses correctly. You should use the  Environment field  on the configuration item \(CI\).

Role required: sam\_admin

## About this task

Visual Studio subscriptions enable developers to download, install, configure, and use most Microsoft software products on any number of devices or virtual machines without having to purchase individual rights. Individual rights aren’t required if the software is deployed only in development or test environments. Use the Microsoft Publisher Pack to manage Visual Studio licensing and reduce compliance risks.

To access the advantages of Visual Studio Standard subscriptions, you must maintain active Microsoft Software Assurance. These benefits enable you to use a range of Microsoft products, including SQL Server, Windows Server for development and testing purposes only.

First, set up software models and entitlements to track your Visual Studio subscriptions. Then, run reconciliation and view the License Workbench to manage license compliance.

## Procedure

1.  [Import software entitlements](view-entitlement-import-errors.md) for your Visual Studio subscriptions.

    **Important:** Fill in the **Publisher part number** column on the entitlement import template to automatically create software models for Visual Studio and all included software \(suite components\). You can look up publisher part numbers in the Software Product Definition table \[samp\_sw\_product\_definition\]. If you fill in the **Publisher part number** field, **Publisher**, **Product**, **Version**, **Edition**, **Platform**, and **Language** aren’t required because the publisher part number provides that information.

    When the import is complete, software models and entitlements are automatically created for your Visual Studio subscriptions. The Visual Studio software models are automatically populated with Suite Components and Downgrade Rights.

    You can also create software entitlements manually. For details, see [Create entitlements in workspace](create-entitlements-workspace.md).

    **Important:** You can view your software models in both the Software Asset Management classic application and the Software Asset Workspace.

2.  Add product install conditions to your Visual Studio software models that apply across all software models including downgrades and editions.

    Install conditions define where the software can be installed. For Visual Studio, installing the software anywhere that is not a development or test environment is a violation of the Microsoft license agreement. Install conditions are used during reconciliation. When you run reconciliation, any Microsoft software installed on production, disaster recovery, or other environments aren't covered by your Visual Studio licenses. These products are considered unlicensed installations unless they’re covered by another Microsoft license.

    For details on adding product install conditions, see [Create product install conditions](create-product-install-condition.md).

    You can add filter conditions to the Product install condition field to limit installations to your development or test environments. For example, you could use the conditions `Installed on contains dev` or `Installed on contains test`.

3.  Add user allocations to your Visual Studio entitlements.

    You can import user allocations using an import set and transform map. Import into the User Allocation \[alm\_entitlement\_user\] table. In the transform map, map the **Assigned to** field to the User table \[sys\_user\]. Use the **Asset tag** field from the entitlement record to link the allocations to the correct entitlements. For the coalesced value, use a two-attribute coalesce on the entitlement and the user.

    For more information, see [Import sets](https://www.servicenow.com/docs/access?context=import-sets-landing-page&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

    Additionally, you can change the inference percent of the Visual Studio software models. The inference percent specifies what percentage of the components must be installed for the suite. It can be 0% in most cases. Also, verify that the Visual Studio community edition is free. For more details on adding inference percent and product licensability at the edition level, see [Create a software model in the Software Asset Workspace](create-swmodels-workspace.md).


## What to do next

Run a reconciliation to view your Visual Studio license compliance. Reconciliation runs weekly or on demand. Reconciliation compares your purchased Visual Studio rights recorded in software entitlements with actual installations found by Discovery. To view reconciliation results in a simplified workbench view, navigate to **Software Asset** &gt; **Reconciliation** &gt; **License Workbench**. For more information, see [Software reconciliation for compliance](../concept/c_SAMReconciliation.md).

**Parent Topic:**[Software Asset Management publisher pack for Microsoft](../concept/microsoft-publisher-pack.md)

